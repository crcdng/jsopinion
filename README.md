# jsopinion

Everyone has an opinion about JavaScript. Here is mine.

JavaScript is certainly [the world's most misunderstood computer language](http://www.crockford.com/javascript/javascript.html). At the same time it is now in a fundamental position: JavaScript is the language of the web. It gets better and has spread to almost every platform.

It is also an [artwork](http://aem1k.com/) and great [fun](https://www.destroyallsoftware.com/talks/wat), if you like Kafka.

What is unique about JavaScript is that not only opinionated beginners but also the most prominent experts cannot agree on fundamentals like semicola or how to implement OOP. There is slowly forming some sort of consensus that functional programming is - very - useful. 👏

The following reflects my thinking which has changed and will change over time.

## JavaScript: do's

* ES6, transpile with Babel
* ES6 modules, use webpack for the Browser   
* `let` and `const`
* `===` except for `== null`
* use `null` to initialize variables that don't have a value yet (not `undefined`), this communicates intention
* arrow functions in callbacks   
* rest operator, default function parameters   
* move from callbacks to promises then to `async/await`
* use tail recursion when it is properly implemented
* use object `{}` and array `[]` literals wherever possible
* did I mention functional programming?      
* use `class` (because it is now a language standard and makes translating legacy code / code from other languages easy. It helps onboarding. Code is easy to read. Individual prototypical inheritance solutions (I tried many) might be technically superior but suffer from a "not being standardized" problem. Transpilers and the evolving JavaScript standard will hopefully  take care about under-the-hood problems currently associated with `class`.)
* use modules for data privacy, not classes
* small, shallow OOP inheritance hierarchies are ok
* semicola (language intention and majority of examples)
* 2 spaces for indentation (the argumentation for using tabs is interesting though. In practice it creates problems.)
* (this means you can use [semistandard](https://github.com/Flet/semistandard) as a linter)

## JavaScript: avoid

* idiomatic ES5 constructions, including  `self = this`, `bind`, IFFE etc. Not necessary anymore.   
* var (because it is almost universally misunderstood. maybe there are exceptions?)   
* `.prototype` - use `class` instead   
* `this` (except in classes or frameworks that dictate `this`)   
* other module systems (?)   
* `!x` to check for null or undefined
* most of the stuff warned against in [JavaScript The Good Parts](http://shop.oreilly.com/product/9780596517748.do). Book needs an ES6 update.     
* lots of other stuff not mentioned here

## JavaScript: Resources

### Essential

[Exploring ES6](https://leanpub.com/exploring-es6/) by Dr. Axel Rauschmayer
[Online Version](http://exploringjs.com/es6/index.html)

### Useful

http://www.ecma-international.org/ecma-262/6.0/

https://caniuse.com/

### Become a better programmer

[Professor Frisby's Mostly Adequate Guide](https://github.com/MostlyAdequate/mostly-adequate-guide) by Brian Lonsdorf

[JavaScript Allongé, the "Six" Edition](https://leanpub.com/javascriptallongesix/read) by Reginald Braithwaite

[Eric Elliot](https://ericelliottjs.com/) I don't agree on everything but lots of good stuff.

[Modular JavaScript](https://mjavascript.com/) by Nicolás Bevacqua
(Looks good, I haven't read it yet. Will update accordingly.)

# Stay up-to-date

http://javascriptweekly.com/

# Postface

🤔 I should add code examples to illustrate some of the points.
