![JavaScript Logo](https://www.tutorialrepublic.com/lib/images/javascript-illustration.png)\
<sub>JavaScript Logo by tutorialrepublic.com</sub>

# The 12 Concepts about JavaScript

JavaScript is one of the most popular languages globally, and it is most commonly used as the language that handles and renders dynamic features to the web pages on a web browser. In was created by Netscape in 1995 and standardized in 1997. Nowadays, JavaScript is the standard language for web applications and is supported by web-browsers such as Firefox, Safari, Chrome, and Edge, among others.

_"JavaScript is officially maintained by ECMA (European Computer Manufacturers Association) as ECMAScript. ECMAScript 6 (or ES6) is the latest major version of the ECMAScript standard"_ <sup>1</sup>

**Table of Contents**

- [The 12 Concepts about JavaScript](#the-12-concepts-about-javascript)
  - [Variables](#variables)
    - [var, let, and const](#var-let-and-const)
    - [typeof](#typeof)
    - [Null and Undefined](#null-and-undefined)
  - [Strings](#strings)
  - [Numbers](#numbers)
  - [Arrays](#arrays)
  - [Operators](#operators)
    - [Arithmetic Operators](#arithmetic-operators)
    - [Assignment Operators](#assignment-operators)
    - [String Operators](#string-operators)
    - [Comparison Operators](#comparison-operators)
    - [Conditional (Ternary) Operator](#conditional-ternary-operator)
    - [Logical Operators](#logical-operators)
  - [Objects](#objects)
  - [Functions](#functions)
  - [Statement](#statement)
    - [If Else Statement](#if-else-statement)
    - [Switch statement](#switch-statement)
  - [Loops](#loops)
    - [For](#for)
    - [For In](#for-in)
    - [While](#while)
    - [Do While](#do-while)
  - [Global Objects](#global-objects)
  - [DOM](#dom)
  - [BOM](#bom)
- [References](#references)
- [Tools](#tools)
- [Author](#author)

JavaScript is easy to use and learn as a programming language. It can be used as scripting language or object-oriented to handle the client-side of the web browser, and more recent as the server-side with Node.js. This document will explain the basic concept associated with JavaScript.

_*For our examples, we will use the `console.log(varName)` that is a function that write message to log on the debug console in the browser. Moreover, in many examples we will write to the console.log using template strings iteration `${}`*_

```JS
 var myVar = 1;
 console.log(`myVar value is ${myVar}`);

```

## Variables

In all languages, variables are entities that are created to hold or store data values. These values can be anything such as string, numbers, objects, functions, arrays, or booleans. In other languages, when a variable is created, the type needs to be defined. However, in JavaScript, the type of the variable is not defined when the variable is created. Therefore, a variable can be created as a string and later become or re-assign to a number or other type.

- Rules for Variables names;
  - names can starts with letters or `$` and `_`
  - names are case sensitive i.e: x and X are not the same variable
  - there are reserved words that cannot be names such as JavaScript or keywords.

### var, let, and const

There are several ways declare a varibale

- using var keyword

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

Example:\
![Let  Const example](img/let_const.gif) \
<sub>An error will appears when you try to re-assign a const variable</sub>

### typeof

- in JavaScript we can identity the type of an variable using `typeof`. Moreover, we can notice that a varible which started as String can become a Number or something else.

```JS
var oneName = 'one';
console.log(oneName);
console.log(typeof oneName);

// re-assiging data to our variable
oneName = 1;
console.log(oneName);
console.log(typeof oneName);
```

Example: \
![Type of Example](img/typeof.gif)

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

Example: \
![null undefined ](img/null_undefined.gif)

- While `null` and `undefined` are not the same and they are not interchangable, they share similarities. For instance, When they are compared with double equality (`==`), JavaScript return `true` because double equals(`==`) compares values after convert the variables to the common type. (we will back to `==` and `===`)

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

Example: \
![null undefined ](img/null_undefined_comp.gif)

## Strings

- Variables that are storing text are named string. A String variable has several methods associated that help to manipulate the text. Moreover, a String variable can be declared with single `'` or double `"` quote.

```JS
var oneName = 'one';
var twoName = "two";
```

- String can be concatenated using `+` or using a more modern approach of Template literals that allows embedded expressions `${}`

```JS
var oneName = "one"
var twoName = "two"
var example1 = oneName + " is before " + twoName;

console.log(example1)
var example2 = `${oneName} is before ${twoName}`;
console.log(example2)
```

Example: \
![string arith](img/string_ar.gif)

- The length of the string can be found using `length`

```JS
var oneName = "one", twoName = "two";
var example1 = oneName + " is before " + twoName;
console.log(example1.length);
```

Example: \
![string length](img/string_length.gif)

- A string variable has several methods associates and the more relevant are:
  - `indexOf()` that return the index position of a specific text, it return `-1` if the text is not found.
  - `includes()` return a true if the text is part of the string, false if it doesnt't
  - `split(separator)` return and array from the string.
  - `slice(start, end)` it will extract a part of the string

```JS
var str = 'francia riesco homework was good'; // =)
console.log(str.indexOf('r'));
console.log(str.indexOf('y'));
console.log(str.includes('r'));
console.log(str.split(' '));
console.log(str.slice(0, 7));
```

Example:
![string methods](img/string_methods.gif)

## Numbers

- JavaScript support integers and floating points numbers such as decimal, hexadecimal to name few.

```JS
var x = 100; // integer
var y = 3.14; // decimal
```

- When two or more number are added, JavaScript does it as regular algebra addition but when you try to add a string with a number JavaScript will concatenate them as they are string.

```JS
var x = 100;
var y = 50;
var z = "80";

console.log(x + y);
console.log(x + z);
console.log(x + y + z);
console.log(x + z + y);
```

Example: \
![number add ](img/number_add_con.gif)

- JavaScript doesn't get confused `-, %, /, *` and it tries to convert strings to numbers in all numeric operations. If one fo the variables is not an number it will return `NaN`

```JS
var x = 100;
var y = 50;
var z = "80";

console.log(x / z);
console.log(x * z);
console.log(x % z);
console.log(x - z);
console.log(x - z - y);
```

Example: \
![string length](img/number_other_ops.gif)

- There are three ways to convert string to numbers:
  - `Number()` converted the argument to a number, it doesn't convert when there is letter or other character
  - `parseFloat()` Parses the argument and returns a floating number
  - `parseInt()` Parses its argument and returns an integer

```JS
console.log(parseInt("10.1"));
console.log(parseInt("10.q"));

console.log(parseFloat("10.1"));
console.log(parseFloat("10.a"));

console.log(Number("10.1"));
console.log(Number("10.a"));
```

<sub>NaN means Not a Number</sub>

Example: \
![number parse](img/number_parse.gif)

## Arrays

- Arrays variables thay can store multiples values. In JavaScript, an array can store different type of values in the same array.

```JS
var strArray = ["Spain", "Brazil", "Argentina", "U.K."];
var newArray = new Array("California", "Illinois", "Iowa");
var numArray = [1, 2, 3, 4];
var mixArray = ["Spain", 6, "U.K", 19];
var emptyArray = [];
```

- We can access Arrays to elements by indexes
  - The length of the array can be found using `length`
  - `array[index] = value` overwrites an element
  - `push()` add an element at the end of the array
  - `pop()` remove the last element of the array
  - `shift()` remove the first element of the array
  - `unshift()` add an element on the beginning of the array
  - `join()` merge the array into an string;
  - `typeof` an Array will return `object` and we need to use `Array.isArray()` to find if we are dealing with an Array

```JS
var countries = ["Spain", "Brazil", "Argentina", "U.K."];
console.log("countries length", countries.length);
countries[0] = "Sweden";
countries.push("France");
console.log(countries);
countries.pop();
console.log(countries);
countries.unshift("Germany");
console.log(countries);
countries.shift();
console.log(countries);
console.log(countries.join(","));
console.log(typeof countries);
console.log(Array.isArray(countries));
```

Example: \
![array prop](img/array_prop.gif)

- looping the array
- there are several ways to loop elements of the array. Moreover, lastest version of JavaScript, introduced simple way to do it

```JS
var countries = ["Spain", "Brazil", "Argentina", "U.K."];
// classic
for (var i = 0; i < countries.length; i++) {
  console.log(countries[i]);
}
console.log('---');
// in
for (var i in countries) {
  console.log(countries[i]);
}
console.log('---');
// of: it doesn't care about the index of the element
for (var country of countries) {
  console.log(country);
}
```

Example: \
![array loop](img/array_loop.gif)

## Operators

- In javascript, operators classified as `Arithmetic Operators`, `Assignment Operators`, `String Operators`, `Comparison Operators`, `Conditional (Ternary) Operator`, `Logical Operators`, `Bitwise Operators`, `typeof Operator`, `delete Operator`, `in Operator`. Operators are the most useful elements in JavaScript helping, the software developer write the logic and functionality of her code.

### Arithmetic Operators

- They are used to perform arithmetic between variables and/or values<sup>5</sup>.

Table: \
![operator arithmetic](img/op_arith.png)\
<sub>courtesy of w3schools.com<sup>5</sup></sup>

```JS
var x = 5;
var y = 2;
console.log("5 + 2:", 5 + 2);
console.log("5 - 2:", 5 - 2);
console.log("x + y:", x + y);
console.log("x - y:", x - y);
console.log("x * y:", x * y);
console.log("x ** y:", x ** y);
console.log("x / y:", x / y);
console.log("x % y:", x % y);
console.log("++x:", ++x);
console.log("--x:", --x);
```

Example: \
![operator arithmetic](img/op_arith.gif)

### Assignment Operators

- Assignment operators are used to assign values to JavaScript variables<sup>5</sup>. `=` is one of the most important operators, we use to create variables, re-assign values and many others.

Table: \
![operator assign](img/op_assign.png)\
<sub>courtesy of w3schools.com<sup>5</sup></sup>

```JS
var x = 5;
var y = 2;
console.log(" x += y", (x += y));
console.log("x -= y", (x -= y));
console.log("x *= y", (x *= y));
console.log("x /= y", (x /= y));
console.log("x %= y", (x %= y));
```

Example: \
![operator assign](img/op_assign.gif)

### String Operators

- In JavaScript, `+` add operator is used to concatenate two or more string.
- New version of JavaScript use template interpolation `${}` rather than `+` (as mentioned in String manipulation as variable).

Table: \
![operator string](img/op_string.png)\
<sub>courtesy of w3schools.com<sup>5</sup></sup>

```JS
var oneName = "one";
var twoName = "two";
var example = oneName + " before than " + twoName;
console.log(example);
oneName += " before than " + twoName;
console.log(oneName);
```

Example: \
![operator string](img/op_string.gif)

### Comparison Operators

- they are used in logical statements to determine `equality` or `difference` between values. Moreover, they return boolean `true` or `false` depending the results<sup>5</sup>.

Table: when `x = 5` \
![operator comparison](img/op_comp.png)\
<sub>courtesy of w3schools.com<sup>5</sup></sup>

```JS
var x = 5;
console.log("x == 8", x == 8);
console.log("x == 5", x == 5);
console.log('x == "5"', x == "5");
console.log("x === 5", x === 5);
console.log('x === "5"', x === "5");
console.log("x != 8", x != 8);
console.log("x != 5", x != 5);
console.log('x != "5"', x != "5");
console.log("x !== 8", x !== 8);
console.log("x !== 5", x !== 5);
console.log('x !== "5"', x !== "5");
console.log("x > 8", x > 8);
console.log("x < 8", x < 8);
console.log("x > 5", x > 5);
console.log("x < 5", x < 5);
console.log("x >= 8", x >= 8);
console.log("x <= 8", x <= 8);
console.log("x >= 5", x >= 5);
console.log("x <= 5", x <= 5);
```

Example: \
![operator comparison](img/op_comp.gif)

### Conditional (Ternary) Operator

- This operator assigns a value to a variable based on a condition<sup>5</sup>. Moreover, this operator is an easy way to reduce the amount of code and syntax. (see `If Else Statement`)

Table: \
![operator conditional](img/op_tern.png)\
<sub>courtesy of w3schools.com<sup>5</sup></sup>

```JS
var isSpanish = true;
// if / else simplified
var name = isSpanish ? "hola" : "hello";
console.log(name);
// if variable exist
var oneName = name ? name : "noname";
console.log(name);
// even shorter version pf if variable exist
var twoName = name ?? "noname";
console.log(twoName);
```

Example: \
![operator conditional](img/op_tern.gif)

### Logical Operators

Table: \
![operator logic](img/op_logic.png)\
<sub>courtesy of w3schools.com<sup>5</sup></sup>

## Objects

## Functions

- A function is a block of code that performs a task, it can be reused, and they are practical for not repeating code or creating a compact logic of code that is easy to read and organize.

## Statement

### If Else Statement

### Switch statement

## Loops

### For

### For In

### While

### Do While

## Global Objects

## DOM

## BOM

```JS

```

```JS

```

# References

1. https://www.tutorialrepublic.com/javascript-tutorial/
1. https://www.w3schools.com/jsref/
1. https://codeburst.io/javascript-null-vs-undefined-20f955215a2
1. https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/null
1. https://www.w3schools.com/jsref/jsref_operators.asp

# Tools

- Written with Markdown
- Hosted by Github
- Gif by Giphy Capture
- VSCode as IDE
- Markdown All in One
- Github desktop for Git respository
- jsfiddle.net to host live code
- Grammarly for proofreading

# Author

Francia Riesco \
August 2020
