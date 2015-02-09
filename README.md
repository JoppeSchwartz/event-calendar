# &lt;event-calendar&gt;

> Custom calendar polymer components with support for events display.

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

2. Import one or more Custom Elements: 

    ```html
    <link rel="import" href="bower_components/event-calendar/dist/calendar-month.html">
    ```

    ```html
    <link rel="import" href="bower_components/event-calendar/dist/calendar-week.html">
    ```

    ```html
    <link rel="import" href="bower_components/event-calendar/dist/calendar-day.html">
    ```

3. Start using it!

    ```html
    <calendar-month curDate="2015-2-10"></calendar-month>
    ```

## Options

Attribute     | Options     | Default      | Description
---           | ---         | ---          | ---
`foo`         | *string*    | `bar`        | Lorem ipsum dolor.

## Methods

Method        | Parameters   | Returns     | Description
---           | ---          | ---         | ---
`unicorn()`   | None.        | Nothing.    | Magic stuff appears.

## Events

Event         | Description
---           | ---
`onsomething` | Triggers when something happens.

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

* To test your project, start the development server and open `http://localhost:8000`.

    ```sh
    $ grunt server
    ```

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
