![JavaScript Logo](https://i.morioh.com/2020/01/06/2b34e42c3159.jpg) \
<small> JavaScript Logo by i.morioh.com</small>

# JavaScript evolution and Modern Syntaxis

# Table Of Contents

- [JavaScript evolution and Modern Syntaxis](#javascript-evolution-and-modern-syntaxis)
- [Table Of Contents](#table-of-contents)
- [Brief History](#brief-history)
  - [Version list and releases dates](#version-list-and-releases-dates)
  - [Versions Evolution](#versions-evolution)
- [Variables](#variables)
  - [let](#let)
  - [const](#const)
- [Functions](#functions)
  - [Functions Evolution](#functions-evolution)
  - [Functions can have default parameters](#functions-can-have-default-parameters)
  - [Immediately invoked function expression (IIFE)](#immediately-invoked-function-expression-iife)
  - [Arrow Functions](#arrow-functions)
- [Arrays](#arrays)
- [Objects](#objects)
- [Map, Set, and More](#map-set-and-more)
- [Promises](#promises)
- [Async and Wait](#async-and-wait)
- [References](#references)
- [Tools](#tools)
- [Author](#author)

# Brief History

JavaScript(JS) is a compiled programming language known as the scripting languages for the web. JavaScript is a single-threaded language that supports object-oriented programming. It was initially developed by Netscape and standardized by ECMAScript. This scripting language was initially named Mocha, later LiveScript, and finally, JavaScript. In the beginning, all releases were called by a numeric value. However, after June 2015, ES6(6th version) name convention changed to ECMAScript 2015 (ES2015) to follow annual releases of the standard. The latest version released in June 2020, named ECMAScript 2020 (ES2020) or ES11.

![JavaScript Version List](https://miro.medium.com/max/373/1*wd1d5oHP9mJaj6sLS6F83w.jpeg)\
_“An organization that creates standards for technologies.” - European Computer Manufacturers Association (ECMA)_

## Version list and releases dates

![JavaScript Version List](https://cdn-media-1.freecodecamp.org/images/uBY4n5MuFWvc81VWSWVk2wc1ZYQ4MF1RM39A) \
<sub>courtesy freecodecamp.org</sub>

## Versions Evolution

The first two versions were quickly released in the late 90s. The new browser competition generated that each browser added functionalities beyond ECMAScript standards. These additions brought a substantial technical fragmentation between browser and JavaScript compatibility. With the decline of Netscape, which was leading the development of JavaScript, the ES4 release was abandoned. For the next years, the committee controlling the proposal for ECMAScript Standard was Microsoft, Mozilla, Adobe, and Opera. The committee took years to agree on features and new standards for JavaScript, but in 2009 comes the major release ES5. This version became the most supported version of JavaScript. With the arrival of Google Chrome, the ECMAScript committee agreed to evolve JavaScript beyond the web browsers and make it a general-purpose language. The generalization of JavaScript gives this programming language a new life as one of the most dominant languages nowadays. This allowed JavaScript to be used to web pages, mobile apps, server-side, application, and many more.`[2]`

**Next a list of the most useful features of JavaScript**

# Variables

The classic way to declare a variable in JavaScript is using the keyword `var`. A variable created with `var` it is assigned to the global object and it is available everywhere in the code. Moreover, a variable declared with `var` inside a function it is local and available only on the function.

## let

- Declaring a variable using `let` allows that this new variable is only bound to a block, this is named `block scoping`. In other words, the variable will be available inside the scope `{ .. }`

```JS
var a = 2;
{
  let a = 3;
  console.log(a); // 3
}
console.log(a); // 2

```

- On the contrary than `var`, declaring `let` outside of any function, the variable is not a global variable but it will be available on all lower scope;

```JS
function test() {
  var x = 5;
  while (x < 6) {
    let y = x + 3;
    console.log("y", y);
    x += 1;
  }
  console.log("x", x);
  console.log("y", y);
}

test();
```

Example: \
![let](img/let_scope.gif)

```JS
let y = 3;

function test() {
  var x = 5;

  while (x < 6) {
    y = x + 3;
    console.log(y);
    x += 1;
  }
  console.log(x);
  console.log(y);
}
test();

```

Example: \
![let](img/let_scope2.gif)

## const

- `const` declares a constanst variable that cannot be reasigned.
- Similar to `let`, `const` has block scope.
- An array declared as `const`, its elements can be overwritten but not the array itself.

```JS
const myArray = [1, 2, 3];
myArray[0] = "a";
myArray.pop();
myArray.push(4);
console.log(myArray);
myArray = ['a', 'b']
```

Example: \
![array const](img/array_const.gif)

# Functions

- In javascript a `function` is a block of code that can be used multiple times, in different part of the code and this make the code reusable and easy to mantaine.

```JS
 function myFunction(p1, p2) {
  return p1 * p2;
}
```

## Functions Evolution

- With the new editions of JavaScript, functions become one of the first element evolved to more useful functionalities.

```JS
// Named function declaration (classic)
function myFunction () { /* ... */ }

// function expression assigned to a variable
var myFunction = function () { /* ... */ };

// function as object property
var myObj = {
    myFunction: function () { /* ... */ }
};
```

## Functions can have default parameters

- With default parameters in a function, we don't need extra code to check for a missing parameter in a function

```JS
function myFunction(p1 = 5, p2 = 10) {
  return p1 * p2;
}
```

## Immediately invoked function expression (IIFE)

- this is a design patter known as `self-executing anonymous function` that runs as soon as it is defined.
- The first part `(function () { })` is the anonymous function. This prevents accessing variables within the IIFE, and polluting the global scope.
- The second part `()` creates the immediately invoked function, where JavaScript will inmediatelly interpret the function.

```JS
(function () {
   /*  ... */
})();

// passign parameters to the IIFE
var x = "value";
(function (innerX) {
    console.log(innerX);
})(x);
```

## Arrow Functions

- This type of functions was introduced on ES6 and revolutionized the way of JavaScript looks forever.
- The new syntax to write functions allowed condensed and concise code, where the `function` prefix, `return,` curly brackets `{}` and parentheses become obsolete.

```JS
// classic function
function test() {
  return "test!";
}

// function as variable
let test = function () {
  return "test!";
};

// arrow function
let test = () => {
  return "test!";
};

// arrow function return vlaue by default
let test = () => "test!";

// arrow function with parentheses
let test = (x) => {
 x * 10;
};

// arrow function without parentheses
let test = x => x * 10;
```

# Arrays

# Objects

# Map, Set, and More

# Promises

# Async and Wait

# References

1. https://developer.mozilla.org/en-US/docs/Web/JavaScript
1. https://www.freecodecamp.org/news/es5-to-esnext-heres-every-feature-added-to-javascript-since-2015-d0c255e13c6e/
1. https://swarmonline.com/the-evolution-of-javascript/
1. https://medium.com/javascript-in-plain-english/the-relationship-between-javascript-ecmascript-6d17706a576
1. https://medium.com/launch-school/javascript-es6-var-let-const-9645f543f7cb
1. https://developer.mozilla.org/en-US/docs/Glossary/IIFE
1. https://www.w3schools.com/js/js_arrow_function.asp
1. http://adripofjavascript.com/blog/drips/an-introduction-to-iffes-immediately-invoked-function-expressions.html

# Tools

- Written with Markdown
- Hosted by Github
- Gif by Giphy Capture
- VSCode as IDE
- Github desktop for Git respository
- jsfiddle.net to host live code
- Grammarly for proofreading

# Author

Francia Riesco \
August 2020
