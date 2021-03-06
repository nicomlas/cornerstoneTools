[![NPM version][npm-version-image]][npm-url] [![NPM downloads][npm-downloads-image]][npm-url] [![MIT License][license-image]][license-url] [![Build Status][travis-image]][travis-url]
[![Coverage Status][coverage-image]][coverage-url]

cornerstoneTools
================

cornerstoneTools is a library built on top of [cornerstone](https://github.com/chafey/cornerstone) that provides
a set of common tools needed in medical imaging to work with images and stacks of images.

View the [live examples](https://rawgithub.com/chafey/cornerstoneTools/master/examples/index.html) to see this
library in action!

View the [simple image viewer](http://chafey.github.io/cornerstoneDemo/) built on cornerstone.

Community
---------

Have questions?  Try posting on our [google groups forum](https://groups.google.com/forum/#!forum/cornerstone-platform).

Status
------

**Project Status: Alpha (Stable) **

NOTE: Project is currently under active development - functionality is not complete, bugs exist,
APIs will change and documentation is missing or not correct.  The implemented functionality is considered
relatively stable.

Make sure to visit the [wiki](https://github.com/chafey/cornerstoneTools/wiki) for more information.


Install
-------

Get a packaged source file:

* [cornerstoneTools.js](https://raw.githubusercontent.com/chafey/cornerstoneTools/master/dist/cornerstoneTools.js)
* [cornerstoneTools.min.js](https://raw.githubusercontent.com/chafey/cornerstoneTools/master/dist/cornerstoneTools.min.js)

Or install via [Bower](http://bower.io/):

> bower install cornerstoneTools

Usage
-------

See the live examples and wiki for documentation on how to use this library

*New*: Specify the cornerstone, jQuery, and Hammer.js instances you want to use the library with.

````javascript
cornerstoneTools.externals.cornerstone = cornerstone;
cornerstoneTools.externals.$ = $;
cornerstoneTools.externals.Hammer = Hammer;
````

```
TODO
```

Features Targeted for V1.0
--------------------------

* Tools that work with a single image
  * WW/WL
  * Zoom
  * Pan
  * Length
  * Rectangle ROI
  * Elliptical ROI
  * Pixel Probe
  * Angle
* Tools that work with a stack of images
  * Scroll
  * Cine / Playing Clips
  * Cross reference lines
* Tools that work with timeseries (4D)
  * Play
  * Scroll
  * Probe
* Measurement Manager
* Synchronization tools
  * Stack by image index
  * Stack by image position
  * Image by zoom and pan
  * Sync ww/wc/invert
* Support for binding each tool to different mouse inputs:
  * Left mouse button
  * Middle mouse button
  * Right mouse button
  * Mouse Wheel
* Support for touch based gestures
  * Drag
  * Pinch
* Tool framework that can be used to simplify development of new tools that work in a consistent manner with the included
  tools
* Provides API to access measurement data for serialization purposes (e.g. save measurements to database)

Build System
============

This project uses webpack to build the software.

Pre-requisites:
---------------

NodeJs - [click to visit web site for installation instructions](http://nodejs.org).

Common Tasks
------------

Update dependencies (after each pull):
> npm install

Running the build:
> npm start

Automatically running the build and unit tests after each source change:
> npm run watch

Backlog
------------

* Updating related handles while resizing (e.g. resize top left handle of a rect and update the bottom left and top right as it changes)
* measurement calibration tool
* Config object that allows tool appearance to be customized (e.g. line color, text color, handle size, shape, etc)
* automatically disabling tools when the enabled element is disabled
* reconsider the state management api, it is a bit clunky
* add support for pointer events as an input source
* Reference line renderer for first/last/active
* Annotations (e.g. text, arrows, circles)
* Move all API documentation from wiki into markdown in a doc folder
* key press input source - so user can interact with tools via keyboard (e.g. scroll stack image using arrow keys)

Copyright
============
Copyright 2015 Chris Hafey [chafey@gmail.com](mailto:chafey@gmail.com)

[license-image]: http://img.shields.io/badge/license-MIT-blue.svg?style=flat
[license-url]: LICENSE

[npm-url]: https://npmjs.org/package/cornerstone-tools
[npm-version-image]: http://img.shields.io/npm/v/cornerstone-tools.svg?style=flat
[npm-downloads-image]: http://img.shields.io/npm/dm/cornerstone-tools.svg?style=flat

[travis-url]: http://travis-ci.org/chafey/cornerstoneTools
[travis-image]: https://travis-ci.org/chafey/cornerstoneTools.svg?branch=master

[coverage-url]: https://coveralls.io/github/chafey/cornerstoneTools?branch=master
[coverage-image]: https://coveralls.io/repos/github/chafey/cornerstoneTools/badge.svg?branch=master