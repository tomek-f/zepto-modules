# zepto-modules

> [Zepto](https://www.npmjs.com/package/zepto) (zepto@28.09.2016 - 1.2.0) in CommonJS modules

## Installation

```bash
$ npm install --save zepto-modules
```

## Usage

Configs (recommended):

```js
// default config (zepto, event, ajax, form, ie)
var $ = require('zepto-modules');
// or
//var $ = require('zepto-modules/_default');

// --------------------------------

// custom config (zepto, event, form, ie, detect, data, touch, stack)
var $ = require('zepto-modules/_custom');

// --------------------------------

// min config (zepto, event, ie, stack)
var $ = require('zepto-modules/_min');

// --------------------------------

// write your own (./my-zepto)

var $ = require('zepto-modules/zepto');

require('zepto-modules/event');
require('zepto-modules/ajax');
require('zepto-modules/form');
require('zepto-modules/ie');

module.exports = $;

// later
var $ = require('./my-zepto');
```

`When-you-need-it` &trade;:

```js
var $ = require('zepto-modules/zepto');
var each = require('cmnjs/each');

// these modules (singleton) extend zepto with methods which are available everywhere in your modules
require('zepto-modules/event');
require('zepto-modules/ie'); // kinda important

// rest of module
```

You can extend configs:

```js
var $ = require('zepto-modules/_custom');

require('zepto-modules/ajax')

$.ajax({
  type: 'GET',
  url: '/projects',
  success: function(data) {
    // do sth
  }
});
```

## ES6

```js
import $ from 'zepto-modules';
// or
// import $ from 'zepto-modules/_default';
```

## Changelog

[View on github](https://github.com/tomek-f/zepto-modules/blob/master/changelog.md).
