# jsopinion

Everyone has an opinion about JavaScript. Here is mine.

JavaScript is certainly [the world's most misunderstood computer language](http://www.crockford.com/javascript/javascript.html). At the same time it is in a fundamental position: JavaScript is the language of the web. It gets better over time (keeping all the bad stuff), while it has spread to almost every platform.

It is also an [artwork](http://aem1k.com/) and great [fun](https://www.destroyallsoftware.com/talks/wat), if you like Kafka.

"Underneath that awkward Java-esque patina, JavaScript has always had a gorgeous heart." (Jeremy Ashkenas, http://coffeescript.org)

I see this gorgeous heart coming out more and more with the current evolution of the language.

What is unique about JavaScript is that not only opinionated beginners but also the most prominent experts cannot agree on fundamentals like to use/not to use semicola or how to implement OOP. There is slowly forming some sort of consensus that functional programming is - very - useful. 👏

What is also unique is that the majority of "authoritative" resources is outdated and sometimes dangerously wrong. Signs to run away (or refactor to ES6) are `for (var i..`, `.prototype`, `that = this`, `==` (except for null testing) and similar constructions.  

There is a three-question litmus test: 1. Does your code reflect your intention? 2. Does your code reflect the intention expressed in the language? 3. Can you say "yes" three times?

The following Do's and Dont's reflect my thinking (which has changed and will change over time).

## JavaScript: Do's

* ES6
* transpile with Babel, use babel-preset-env to avoid unnecessary transpiling.
* ES6 modules, both Safari >= 10.1.2 and Chrome >= 61 support them, use webpack for other / older browsers or Babel for node.js
* `let` and `const`
* `===` except for `== null`
* use `null` to initialize variables that don't have a value yet (not `undefined`), this communicates intention
* use arrow functions in callbacks when you access `this`  
* default function parameters, spread / rest operators  
* move from callbacks to promises, then to `async/await`
* use tail recursion when it is properly implemented
* use object `{}` and array `[]` literals
* did I mention functional programming?      
* use `class` (because it is now a language standard and makes translating legacy code / code from other languages easy. It helps onboarding. Code is more easy to read. Individual prototypical inheritance solutions (I tried many) might be technically superior but suffer from a ["not being standardized"](https://xkcd.com/927/) problem. Transpilers and the evolving JavaScript standard will hopefully take care about under-the-hood problems currently associated with `class`.)
* use modules for privacy, not classes
* small, shallow OOP inheritance hierarchies are ok
* semicola. If you leave them out and rely on the insertion *repair* mechanism you are doing it wrong (see litmus test).
* 2 spaces for indentation (the argumentation for using tabs is interesting though. In practice it creates problems.)
* (this means you can use [semistandard](https://github.com/Flet/semistandard) as a linter)
* Use a linter. Your code will be safer, better and much more pleasant to read.

## JavaScript: Avoid

* writing ES5 code 'because it's more common'
* idiomatic ES5 constructions, including `self = this`, `bind`, `apply`, IFFE etc. Not necessary anymore.   
* `this` (except in classes or in frameworks that dictate `this`)   
* `var` (because it is almost universally misunderstood. `var` declarations have to be at the top of functions *only*. This is because the language intends it. If you put `var` anywhere else and rely on hoisting you are doing it wrong (see litmus test). Most programmers don't know this or ignore it and hope for the best. If your intention is to declare a variable somewhere in the middle of a function, use `let`.  
* `.prototype` - use `class` instead   
* other module systems (?)   
* `!x` to check for null or undefined
* `typeof`. If your code relies on static typing, use [TypeScript](https://www.typescriptlang.org)
* string concatenation (use template literals)
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
