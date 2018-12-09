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

1. ES6
1. if you need older or Browser-specific versions, still write your code in ES6 and transpile with Babel.
1. ES6 modules, all major browsers support them now, use webpack for other / older browsers or Babel for node.js
1. `let` and `const`
1. `===` except for `== null` (in case you need to be convinced: https://stackoverflow.com/questions/48270127/can-a-1-a-2-a-3-ever-evaluate-to-true)
1. use `null` to initialize variables that don't have a value yet (not `undefined`), this communicates intention
1. use arrow functions in callbacks when you have to access `this`
1. use default function parameters, spread / rest operators  
1. move from callbacks to `async/await` and learn about Promises
1. use tail recursion after it is fully implemented (this possibly means never)
1. use object `{}` and array `[]` literals
1. did I mention functional programming?      
1. small, shallow OOP inheritance hierarchies are ok
1. if your code is object-oriented use `class` (because it is now a language standard and makes translating legacy code / code from other languages easy. It helps onboarding. Code is easy to read. Individual prototypical inheritance and object factory solutions (I tried many) might be technically superior but suffer from a ["not being standardized"](https://xkcd.com/927/) problem. Transpilers and the evolving JavaScript standard will hopefully take care about problems currently associated with `class`.)
1. use modules, not classes, for privacy
1. semicola. If you leave them out and rely on the insertion *repair* mechanism you are doing it wrong (see litmus test).
1. 2 spaces for indentation (the argumentation for using tabs is interesting though. In practice it creates problems)
1. use a linter. your code will be safer, better and much more pleasant to read.
1. if you follow these points you can use [semistandard](https://github.com/Flet/semistandard) as your linter

## JavaScript: Avoid

1. writing ES5 code 'because it's more common'
1. teaching ES5 code (!!)
1. idiomatic ES5 constructions, including `self = this`, `bind`, `apply`, IFFE etc. Not necessary anymore.   
1. `this` (except in classes or in frameworks that dictate `this`)   
1. `var` (because it is almost universally misunderstood. `var` declarations have to be at the top of functions *only*. This is because the language intends it. If you put `var` anywhere else and rely on hoisting you are doing it wrong (see litmus test). Most programmers don't know this or ignore it and hope for the best. If your intention is to declare a variable somewhere in the middle of a function, use `let`.  
1. `.prototype` - use `class` instead   
1. other module systems, migrate to ES6 modules   
1. `!x` to check for null or undefined
1. `typeof`. If your code relies on static typing, use [TypeScript](https://www.typescriptlang.org) if in your organization people wear neckties, or [PureScript](http://www.purescript.org/) otherwise
1. string concatenation (use template literals)
1. most of the stuff warned against in [JavaScript The Good Parts](http://shop.oreilly.com/product/9780596517748.do). Book needs an ES6 update.     
1. lots of other stuff not mentioned here

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

[Eric Elliot](https://ericelliottjs.com/) I don't agree on everything, but lots of good stuff.

[Modular JavaScript](https://mjavascript.com/) by Nicolás Bevacqua
(Looks good, I haven't read it yet. Will update accordingly.)

# Stay up-to-date

http://javascriptweekly.com/

# Postface

🤔 I should add code examples to illustrate some of the points.
