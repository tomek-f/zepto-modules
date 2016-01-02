# zepto-modules

> Zepto in CommonJS (and ES6) modules

## Installation

```bash
$ npm install --save zepto-modules
```

## Usage

Configs (recommended):

```javascript
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

```javascript
var $ = require('zepto-modules/zepto');
var each = require('cmnjs/each');

// these modules (singleton) extend zepto with methods which are available everywhere in your modules
require('zepto-modules/event');
require('zepto-modules/ie'); // kinda important

// rest of module
```

You can extend configs:

```javascript
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

## ES6 version

copy (for now) modules from `./es6` dir to your location and import them

```javascript
// configs
import $ from './es6/_default'
//import $ from './es6/_custom'
//import $ from './es6/_min'

// --------------------------------

// own config (./my-zepto)

import $ from './es6/zepto';

import './es6/event';
import './es6/ajax';
import './es6/form';
import './es6/ie';

export default $;

// later
import $ from './my-zepto'

// --------------------------------

// own module
import $ from './es6/zepto';
var each = require('cmnjs/each');

import './es6/event';
import './es6/ie';

// rest of module
```

## Changelog

[View on github](https://github.com/tomek-f/zepto-modules/blob/master/changelog.md).
