# &lt;kwc-app&gt;

> A component providing a template to create quickly a single page application

This component needs the use of [app-router](https://github.com/erikringsmuth/app-router).
It will listen on click for all links and change the behavior as a pushstate (for internal links only).

## Install

Install the component using [Bower](http://bower.io/):

```sh
$ bower install kwc-app --save
```

Or [download as ZIP](https://github.com/successk/kwc-app/archive/master.zip).

## Usage

1 – Import polyfill:

```html
<script src="bower_components/webcomponentsjs/webcomponents-lite.min.js"></script>
```

2 – Import custom element:

```html
<link rel="import" href="bower_components/kwc-app/kwc-app.html">
```

3 – Start using it!

See [Full example code](index-kwc-app-show.html)

## Options

Attribute            | Options              | Default      | Description
---                  | ---                  | ---          | ---
`logo`               | *String*             | `null`       | URL of your logo (delegated to `kwc-top-bar`)
`sitename`           | *String*             | `null`       | Your site name (delegated to `kwc-top-bar`)
`sitehome`           | *String*             | `null`       | URL of your of page (delegated to `kwc-top-bar`)
`search`             | *boolean*            | `false`      | Show the input search (delegated to `kwc-top-bar`)
`search-placeholder` | *String*             | `null`       | The placeholder shown in input search (delegated to `kwc-top-bar`)
`delay-search`       | *number*             | `0`          | Delay before the search is triggered after last character typed (delegated to `kwc-top-bar`)
`delay-close-search` | *number*             | `0`          | Delay before the search box is closed after the user leaves the search (blur) (delegated to `kwc-top-bar`)

## Children

Selector                 | Description
---                      | ---
`.top-bar-left-menu`     | Left menu of the top-bar (delegated to `kwc-top-bar`)
`.top-bar-right-menu`    | Right menu of the top-bar (delegated to `kwc-top-bar`)
`.top-bar-search-tips`   | Tips of search (delegated to `kwc-top-bar`)
`.top-bar-search-result` | Results of search (delegated to `kwc-top-bar`)
`.left-panel`            | Content of the left panel
`.content`               | Content of your application, must include an `<app-router>` with `<app-route>`
`.right-panel`           | Content of the right panel

## Methods

Method        | Parameters   | Returns     | Description
---           | ---          | ---         | ---
None          | -            | -           | -

## Events

Event       | Detail   | Description
---         | ---      | ---
search      | *String* | Trigger the search with current query. The search trigger is delayed by `delay-search`. (delegated to `kwc-top-bar`)

## Styles

Name                                   | Default          | Description
---                                    | ---              | --
`--kwc-top-bar-bg-color`               | `#fff`           | Default background color of the top-bar (delegated to `kwc-top-bar`)
`--kwc-top-bar-color`                  | `#000`           | Default text color of the top-bar (delegated to `kwc-top-bar`)
`--kwc-top-bar-box-shadow`             | `0 2px 4px #aaa` | Shadow under the top-bar (delegated to `kwc-top-bar`)
`--kwc-top-bar-site-width`             | `250px`          | Width of the site name part (logo and text) (delegated to `kwc-top-bar`)
`--kwc-top-bar-site-bg-color`          | `#fff`           | Background color of the site name (delegated to `kwc-top-bar`)
`--kwc-top-bar-site-color`             | `#000`           | Text color of the site name (delegated to `kwc-top-bar`)
`--kwc-top-bar-height`                 | `50px`           | Height of the top-bar (delegated to `kwc-top-bar`)
`--kwc-app-top-bar-height`             | `50px`           | Height of the top-bar (needs to be same as `--kwc-top-bar-height`)
`--kwc-top-bar-link-menu-styles`       | `{}`             | Styles of links of menus (delegated to `kwc-top-bar`)
`--kwc-top-bar-link-menu-hover-styles` | `{}`             | Styles of links of menus when hover (delegated to `kwc-top-bar`)
`--kwc-top-bar-search-styles`          | `{}`             | Style of the input search (delegated to `kwc-top-bar`)
`--kwc-app-left-panel-width`           | `250px`          | Width of left panel
`--kwc-app-left-panel-styles`          | `{}`             | Styles of left panel
`--kwc-app-right-panel-width`          | `250px`          | Width of right panel
`--kwc-app-right-panel-styles`         | `{}`             | Styles of right panel

## Development

In order to run it locally you'll need to fetch some dependencies and a basic server setup.

1 – Install [bower](http://bower.io/) & [polyserve](https://npmjs.com/polyserve):

```sh
$ npm install -g bower polyserve
```

2 – Install local dependencies:

```sh
$ bower install
```

3 – Start development server and open `http://localhost:8080/components/kwc-app/`.

```sh
$ polyserve
```

## History

For detailed changelog, check [Releases](https://github.com/successk/kwc-app/releases).

## License

MIT