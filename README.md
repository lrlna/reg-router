# reg-router
[![npm version][2]][3] [![downloads][8]][9] [![js-standard-style][10]][11]

Just your reg router to match routes based on provided regex.

## Usage 

```
var router = require('reg-router')()

router.route(/^\/reset$/, function (req, res, params) {
  res.writeHead(200, 'reset route is hit', { 'content-encoding': 'application/json' })
}

http.createServer(function (req, res) {
  router.match(req, res)
}).listen(8080)
```

# API

## router = new Router()
Creates a new instance off reg-router.

## router.route(regex, handler)
Register a new route. Handler is generally `req, res, params`. 

## router.default(handler)
Defaults to sending back a 404, but you can provide your own default. `router.default` will do this for you.

## router.match(req, res)
Match requests to registered routes. Would usually use when server's fired up. 


# Related content:
- [bankai](https://github.com/choojs/bankai)
- [choo](https://github.com/choojs/choo)

# License
[MIT](https://tldrlegal.com/license/mit-license)

[2]: https://img.shields.io/npm/v/reg-router.svg?style=flat-square
[3]: https://npmjs.org/package/reg-router
[8]: http://img.shields.io/npm/dm/reg-router.svg?style=flat-square
[9]: https://npmjs.org/package/reg-router
[10]: https://img.shields.io/badge/code%20style-standard-brightgreen.svg?style=flat-square
[11]: https://github.com/feross/standard
