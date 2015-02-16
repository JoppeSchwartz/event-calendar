# &lt;event-calendar&gt;

> Custom calendar polymer component with support for events display. Supports monthly, weekly, daily, and list views.

## Demo

[Check it live!](http://JoppeSchwartz.github.io/event-calendar)

## Install

Install the component using [Bower](http://bower.io/):

```sh
$ bower install event-calendar --save
```

Or [download as ZIP](https://github.com/JoppeSchwartz/event-calendar/archive/master.zip).

## Usage

1. Import Web Components' polyfill:

    ```html
    <script src="bower_components/webcomponentsjs/webcomponents.min.js"></script>
    ```

2. Import the event-calendar component:

    ```html
    <link rel="import" href="bower_components/event-calendar/dist/event-calendar.html">
    ```

3. Start using it!

    ```html
    <calendar-month curDate="2015-2-10" header view="month"></calendar-month>
    ```

## Options

Attribute     | Options     | Default          | Description
---           | ---         | ---              | ---
`curDate`     | *Moment*    | moment() [today] | Current date for the calendar; it should be a Moment object or Moment-compatible string (see below)
`header`			| [none]			| [none]			     | If present, the calendar will display a header
`view`				| "month", "week", "day", "list" | "month" | Controls which view the calendar displays
`startHour`	  | *integer*   |	0 (midnight)     | The starting hour of each day to display in week and day views
`events`      | *array*     | []               | Array of events to display on the calendar (see below) 


## Dates and Moments
This component uses the [Moment](http://momentjs.com/) library to handle dates and times. Therefore, the `curDate` attribute and the dates and times associated with events are represented as Moment objects. When passing date and time values in, one should construct a moment instance to do so. E.g., if one has a string date, pass `moment(datestring)`.

## Displaying Calendar Events
To display events, set the `events` attribute to an array of objects, each of which has the following form:

```javascript
{
    start: [Moment],
    end:   [Moment],
    title: [string],
    venue: [string]
}
```
As with `curDate`, the `start` and `end` members must be Moment objects or compatible . 


## DOM Events

Event                  | Description
---                    | ---
`event-calendar-error` | Fires when an malformed event is passed to the calendar

## Styling the calendar
The calendar may be styled using the usual Polymer CSS helpers like `/deep/`. For instance, you can format the header as follows:
```css
event-calendar /deep/ .header {
	background-color: #330033;
	color: #ffffcc;
}
```
and change the color of the current day in the month view like so:

```css
event-calendar /deep/ .dayBoxToday {
	background-color: #ffffcc;
}
```

The currently supported style classes are:
CSS Class					| Description
---								| ---
`header`					| header for all views; can be overridden with a view-specific class
`monthHeader`			| header for month view
`weekHeader`			| header for week view
`dayHeader`				| header for day view and days within week view
`listHeader`			| header for list view 
`dayBoxToday`			| cell for today in the month view
`dayBoxCurrent`   | cell for the currently selected date in month view
`event`						| event display style

If you want more fine-grained control over style, you can reference classes and elements within specific calendar views, e.g. `calendar-month /deep/ event`.

## Development

In order to run it locally you'll need to fetch some dependencies and a basic server setup.

* Install [Bower](http://bower.io/) & [Grunt](http://gruntjs.com/):

    ```sh
    $ [sudo] npm install -g bower grunt-cli
    ```

* Install local dependencies:

    ```sh
    $ bower install && npm install
    ```

* To test your project, start the development server.

    ```sh
    $ grunt server
    ```
This should open a browser displaying the demo page at address `http://localhost:8000`. To run the unit tests, open `http://localhost:8000/test/index.html`.

* To build the distribution files before releasing a new version.

    ```sh
    $ grunt build
    ```

* To provide a live demo, send everything to `gh-pages` branch.

    ```sh
    $ grunt deploy
    ```

## Contributing

1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -m 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request :D

## History

For detailed changelog, check [Releases](https://github.com/JoppeSchwartz/event-calendar/releases).

## License

[MIT License](http://opensource.org/licenses/MIT)
