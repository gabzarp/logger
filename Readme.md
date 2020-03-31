
# koa-ctx-logger

[![npm version][npm-image]][npm-url]

Improved version of [koa-logger](https://www.npmjs.com/package/koa-logger) that saves logs to a /logs/log file, sends ctx.body on logs and has logs functions that you can call inside your context. 


## Installation

```js
$ npm install koa-ctx-logger
```

## How to use
```js
const logger = require('koa-ctx-logger');

app.use(logger());
```
This will automatically log requests and responses in your console and in /logs/log.log file

Log example:
```js
<-- PUT /send-lead
--> PUT /send-lead 500 111ms 66b {"shopId":["shopId is required but was either undefined or null"]}
```

To call log service in another part of your application simply call logger in your ctx:
```js
ctx.logger.info('your string')
```
To get log:
```js
INFO: your string
```
Or:
```js
ctx.logger.error('your string')
```
To get:
```js
ERROR: your string
```

## License

  MIT

[npm-url]: https://www.npmjs.com/package/koa-ctx-logger
[npm-image]: https://img.shields.io/npm/v/koa-logger.svg?style=flat-square

