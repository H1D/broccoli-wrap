# this repo is obsolete! Use `map()` from [stefanpenner/broccoli-stew](https://github.com/stefanpenner/broccoli-stew) instead! How to reaplce example: [asakusuma/ember-rollup/pull/5/files](https://github.com/asakusuma/ember-rollup/pull/5/files)

---

# broccoli-wrap

## Installation

```bash
npm install --save-dev broccoli-wrap
```

## Usage

```js
var wrapFiles = require('broccoli-wrap');
tree = wrapFiles(tree, options);
```

### Options

The following options are supported:

* `wrapper` array of two strings to be placed as start and the end of stream (file)

* `extensions` array of file extensions to process; default: `['js']`

###Example
```js
var wrapFiles = require('broccoli-wrap');

// this will wrap files in 'js' folder into anonymous function
var tree = wrapFiles('js', { wrapper: ["(function(){;\n", "})();"] });

module.exports = tree;
```
