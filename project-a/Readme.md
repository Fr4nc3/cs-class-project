![JavaScript Logo](https://www.tutorialrepublic.com/lib/images/javascript-illustration.png)

###### figure 1. JavaScript Logo by tutorialrepublic.com

# Javascript

JavaScript is one of the most popular languages globally, and it is most commonly used as the language that handles and renders dynamic features to the web pages on a web browser. In was created by Netscape in 1995 and standardized in 1997. Nowadays, JavaScript is the standard language for web applications and is supported by web-browsers such as Firefox, Safari, Chrome, and Edge, among others.

_"JavaScript is officially maintained by ECMA (European Computer Manufacturers Association) as ECMAScript. ECMAScript 6 (or ES6) is the latest major version of the ECMAScript standard"_[1]

# The 10 Concepts about JavaScript

JavaScript is easy to use and learn as a programming language. It can be used as scripting language or object-oriented to handle the client-side of the web browser, and more recent as the server-side with Node.js. This document will explain the basic concept associated with JavaScript.

_*For our examples, we will use the `console.log(varName)` that is a function that write message to log on the debug console in the browser. Moreover, in many examples we will write to the console.log using template strings iteration `${}`*_

```JS
 var myVar = 1;
 console.log(`myVar value is ${myVar}`);

```

## Variables

In all languages, variables are entities that are created to hold or store data values. These values can be anything such as string, numbers, objects, functions, arrays, or booleans. In other languages, when a variable is created, the type needs to be defined. However, in JavaScript, the type of the variable is not defined when the variable is created. Therefore, a variable can be created as a string and later become or re-assign to a number or other type.

### var let and const

There are several ways declare a varibale

- using var keyword and

```JS
 var name;
```

- assign the value after the variable is created

```JS
  name = 'Francia';
```

- declare the variable with the value

```JS
 var name = 'Francia';
```

- declare several variables at the same time

```JS
 var name = 'Francia', lastname='Riesco', country = 'USA';
```

- The latest version of JavaScript introduced `let` and `const` as a keyword to create or declare variables. Declaring a variable using `let` the variable will be defined on a specific scope, and it can be overwritten or re-assigned. On the contrary, declaring a variable using `const,` the variable is read-only and cannot be modified.

```JS
 let name = 'Francia';
 const country = 'USA';
```

Example:

![Let  Const example](img/let_const.gif)

###### An error will appears when you try to re-assign a const variable

### typeof

- in JavaScript we can identity the type of an variable using `typeof`. Moreover, we can notice that a varible which started as String can become a Number or something else.

```JS
var oneName = 'one';
console.log(oneName);
console.log(typeof oneName);

// re assiging data to our variable
oneName = 1;
console.log(oneName);
console.log(typeof oneName);
```

Example:

![Type of Example](img/typeof.gif)

- String can be concatenated using `+` or using a more modern approach of template strings iteration `${}`

```JS
var oneName = "one"
var twoName = "two"
var example1 = oneName + " is before " + twoName;

console.log(example1)
var example2 = `${oneName} is before ${twoName}`;
console.log(example2)
```

Example:

![string arith](img/string_ar.gif)

### Null and Undefined

- In javascript, when a variable is `null` is the absence of any value in the variable or object. Moreover, it is treated as false of boolean operations. In the same way, a variable is `undefined` when it has been declared, but not defined. Similar to `null`, `undefined` is treated as false for boolean operations.

```JS
var example = null;
console.log(example);
console.log(Boolean(example));

var example2;
console.log(example2);
console.log(Boolean(example2))
```

Example:

![null undefined ](img/null_undefined.gif)

- While `null` and `undefined` are not the same and they are not interchangable. However, they share similarities. When they are compared with double equality (`==`), JavaScript return `true` because double equals(`==`) compares values after convert the variables to the common type. (we will back to `==` and `===`)

```JS
console.log(typeof null);
console.log(typeof undefined);
console.log(null === undefined);
console.log(null == undefined);
console.log(null === null);
console.log(null == null);
console.log(!null);
console.log(isNaN(1 + null));
console.log(isNaN(1 + undefined));
```

Example:

![null undefined ](img/null_undefined_comp.gif)

###### example from https://developer.mozilla.org/

### Type Conversion

## Operators

## Statement

### If Else Statement

### Switch statement

## Arrays

## Objects

## Loops

### For

### For In

### For Of

### While

### Do While

## Functions

## Global Objects

## DOM

## BOM

```JS

```

```JS

```

### Tools for this document

- Written with Markup
- Hosted by Github
- Gif by Giphy Capture
- VSCode as IDE
- Github desktop for Git respository
- jsfiddle.net to host live code
- Grammarly for proofreading

##### Author

##### Francia F. Riesco

### References

1. https://www.tutorialrepublic.com/javascript-tutorial/
1. https://codeburst.io/javascript-null-vs-undefined-20f955215a2
1. https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/null
