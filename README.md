# lazy-static-site-gen

This is a simple skeleton of static site generator.

Uses [Brunch](http://brunch.io) as build system.

## Structure

```
static-site-gen
│  .gitignore
│  .jshintrc
│  brunch-config.js
│  package.json
│  README.md
│
└─app
    │  initialize.js
    │
    ├─assets
    ├─js
    ├─static_jade
    │      index.jade
    │      _head.jade
    │
    └─styles
            style.styl
```

- package.json - npm settings with all required dependencies for this skeleton.
- .jshintrc - settings for great lint tool [JSHint](http://jshint.com/). Each build runs it using these settings.
- _app_ - contains everything that's going to be build.
    - assets - Everything inside is copied as it is.
    - js - Contains JS code that will be concatenated into `js/app.js`
        - Each js file will be available as separated module which can be loaded via `require`
    - static_jade - Contains **JADE** templates.
        - `index.jade` - Will be parsed into `index.html`
        - `_head.jade` - Will be ignored, but can be included by other templates. Files starting with `_` are ignored.
    - styles - Contains _stylus_ CSS templates which are concatenated into `style.css`

## Usage

- Fill it with content!
- Run server to preview site with command `npm start`
- Once satisfied build your site with `npm build`
- Post it on github pages or wherever you want!
- PROFIT!
