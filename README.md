# jsopinion

Everyone has an opinion about JavaScript. Here is mine.

JavaScript is certainly [the world's most misunderstood computer language](http://www.crockford.com/javascript/javascript.html). At the same time it sits in a fundamental place: JavaScript is the language of the web.

It is also an [artwork](http://aem1k.com/) and great [fun](https://www.destroyallsoftware.com/talks/wat), if you like Kafka.

What is quite unique about JavaScript is that not only opinionated beginners but also the most prominent experts cannot agree on fundamentals like semicola or how to implement OOP. There seems to be slowly forming some sort of consensus that functional programming is - very - useful. 👏

The following reflects my thinking which has changed and will change over time.

## JavaScript: do's

* ES6, transpile with Babel
* ES6 modules, use webpack   
* `let` and `const`
* `===` except for `== null`
* use `null` different from `undefined`, this communicates intention
* Arrow functions in callbacks   
* Rest operator, default options   
* Move from callbacks to promises then to  async / await   
* `class` (because it is a language standard now and makes translating legacy code / code from other languages easy. Individual prototypical inheritance solutions might be superior but suffer from a "not being standardized" problem. Transpilers and the evolving JavaScript standard will hopefully  take care about problems currently associated with `class`.)
* Semicola (language intention and majority of examples)
* 2 spaces (the argumentation for using tabs is interesting though. In practice it creates problems.)
* (this means you can use use [semistandard](https://github.com/Flet/semistandard) as a linter)

## JavaScript: avoid

* idiomatic ES5 constructions, including  `self = this`, `bind`, IFFE etc. Not necessary anymore.   
* var (because it is almost universally  misunderstood. exceptions?)   
* `.prototype` - use `class` instead   
* `this` (except in classes or frameworks that dictate `this`)   
* other module systems (?)   
* `!x` to check for null or undefined
* most of the stuff warned against in [JavaScript The Good Parts](http://shop.oreilly.com/product/9780596517748.do). Book needs an ES6 update.     
* lots of other stuff not mentioned here

## JavaScript: resources

https://leanpub.com/exploring-es6/
http://exploringjs.com/es6/index.html

https://leanpub.com/javascriptallongesix/read

http://shop.oreilly.com/product/0636920047124.do
https://github.com/mjavascript/practical-modern-javascript
(Looks good, I haven't read yet. Will update.)

http://javascriptweekly.com/

[Eric Elliot](https://ericelliottjs.com/) I don't agree on everything but lots of good stuff.

https://caniuse.com/

# Postface

🤔 I should add code examples to illustrate some of the points.
