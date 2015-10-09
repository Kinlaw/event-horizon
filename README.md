<p align="center"><img src="https://cloud.githubusercontent.com/assets/129737/10388026/5e3fe9da-6e34-11e5-8795-bb56a861a572.png"></p>


# event-horizon

[npm-url]: https://npmjs.org/package/event-horizon
[downloads-image]: http://img.shields.io/npm/dm/event-horizon.svg
[npm-image]: http://img.shields.io/npm/v/event-horizon.svg
[![NPM version][npm-image]][npm-url] [![Downloads][downloads-image]][npm-url]

Eats things that happen too many times per time window.
A time window in this case is a sliding window.

# Example

## Simple

```javascript
var horizon = require('event-horizon').instance({window: 200, max: 50});
horizon.run(function () {
    request(...);
});
```

## With a callback

```javascript
var horizon = require('event-horizon').instance({window: 200, max: 50});
horizon.run(function () {
    request(...);
}, function () {
    deferred.reject();
});
```
