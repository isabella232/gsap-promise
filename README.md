# gsap-promise

[![experimental](http://badges.github.io/stability-badges/dist/experimental.svg)](http://github.com/badges/stability-badges)

A Promise wrapper around gsap / tweenlite. 

```js
var animate = require('gsap-promise')

Promise.all([
	animate(element, 1.0, { x: 10 }),
	animate(element, 1.0, { y: 10, delay: 0.5 })
]).then(function() {
	console.log("all animations finished")
})
```

*Note:* This uses Bluebird for the promises, although you can get around it with: `require('gsap-promise/base')(Promise)`

## Usage

[![NPM](https://nodei.co/npm/gsap-promise.png)](https://nodei.co/npm/gsap-promise/)

This promisifies the `TweenMax` methods: `to`, `from`, `set` and `fromTo`. 

#### ```animate.to(element, duration, params)```
#### ```animate.from(element, duration, from)```
#### ```animate.set(element, params)```
#### ```animate.fromTo(element, duration, from, to)```

Matches the TweenMax methods by the same name, but returns a Promise for the onComplete event. 

#### ```animate(element, duration, params)```

The default export is the same as `animate.to`.

## License

MIT, see [LICENSE.md](http://github.com/mattdesl/gsap-promise/blob/master/LICENSE.md) for details.