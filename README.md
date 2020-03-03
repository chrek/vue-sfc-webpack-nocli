# vue-sfc-webpack-nocli

Single File Components With Webpack
-----------------------------------

Using Webpack without the CLI for Vue.js Single File Components

Webpack
-------
- Webpack is a module bundler. It bundles code from multiple files into one.
- Converts JavaScript (ECMAScript 6+) into ECMAScript 5
- Transforms code with loaders and plugins (add-ons for Webpack)

Useful Commands to run (see package.json for available scripts):
----------------------------------------------------------------
- `npm run clean` to delete any previous builds we may have
- `npm run build` runs the clean command followed by running all webpack tasks and minify output...
- `npm run serve` to run the dev server, compile and recompile assets after changes.

Webpack configuration file
--------------------------
The webpack.config.js file is the configuration file for webpack

* webpack-dev-server:
  * contentBase: Used to gzip and serve everything from our dist/ directory in the project root
  * Hot Module Replacement(HMR): For LiveReload replacement - exchanges, adds, or removes modules while an application is running, without a full reload. Enable this feature by setting its hot option to true:
  * Set open option to true - Tells dev-server to open default browser after server had been started.

## What has been implemented
* Interporlation
* Directives (v-if, v-bind, v-on or corresponding shorthands)
* Props
* Nested Component
* Single File Components

<hr>

## References

1. [scotch.io] (https://scotch.io/courses/getting-started-with-vuejs/processing-a-form-with-vue)
2. [vegibit.com] (https://vegibit.com/vuejs-form-example/)