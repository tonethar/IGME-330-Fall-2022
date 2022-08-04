# IGME-330 - Course Code Style Requirements

- These rules are in effect for all IGME-330 HW assignments and projects
- *What if some of the class "start code" breaks these rules? You are required to FIX the code!*

## I. Web file naming conventions

1) "web" folder and file names (HTML/CSS/JS/images etc) will be in all lower case letters, with words separated by dashes:
    - capital letters are NOT allowed anywhere in a file name
    - example **user-form.html** is best, **userform.html** is acceptable, but **Userform.html** OR **userForm.html** are NOT allowed
    - spaces are NOT allowed in file names - ex. **user form.html** or **user%20form.html** are NOT allowed

2) exceptions:
      - ES6 class names will begin in an uppercase letter (ex. **Sprite.js**)
      - font file names may have uppercase letters
    
<hr><hr>

## II. HTML & DOM Traversal

1) HTML source code elements will be properly and consistently indented

2) HTML `id` and `class` attribute names will be in all lower case letters, with words separated by dashes
    - example `<a id="my-name" />` or `<a id="myname" />` are OK, but `<a id="myName" />` is NOT allowed

3) Selecting DOM elements (aka "DOM Traversal") will be done with `document.querySelector()` and/or `document.querySelectorAll()`:
    - *NEVER* use `document.getElementById()`, `document.getElementsByTagName()` etc, or *jQuery* in this class

4) Hooking up events:
    - *Event listeners* (ex. `myButton.addEventListener("click",doStuff)`) and *Event Handlers* (ex. `myButton.onclick = doStuff)`) are both allowed
    - NEVER use inline event handlers in the HTML - ex. `<button onclick="doStuff()">Click Me</button>`

<hr><hr>

## III. JavaScript

1) declare variables with `const` & `let` only:
    - *NEVER* use `var` in this course

2) function, variable, constant and function parameter *names* will begin in a lower case letter - ex. `function queryService()`, `const numSprites = 10`
    - the above also applies to ES6 class method names, and class method parameter names
    - object literal property names will also begin in a lower-case letter, and spaces in property names are not allowed
    - camel casing for all of the above - ex `btnSeach` IS allowed
    - *Q: So why is camel-casing allowed with variable names, but not with file names, function names, id names etc?*
      - *A: Because we can't use dashes in JS variable names, they would be interpreted as a minus sign*

3) ES6 class names *always* begin in an uppercase letter - ex. `class Sprite{}`
    - code shall be consistently indented and "line up" so that it is readable:
    - you can use 2-spaces, 4-spaces, or tabs - it just has to be  *consistent* and *readable*

<hr>

### III-A. ES6 Modules

1)  In general, your HTML page will import only one JS file of `type="module"`
    - for example, imagine if you had 2 files **app.js** and **my-component.js**
    - you would import **app.js** like this -  `<script type="module" src="./src/app.js">`
    - and then (at the top of) **app.js** you `import` **my-component.js** like this - `import {MyComponent} from "./my-component.js";`
    - you would NOT do this in the HTML file:
      - `<script type="module" src="./src/app/js">` and `<script type="module" src="./src/my-component.js">`

2) All `import` statements must be at the top of the file


<hr>

### III-B. Extraneous or Unnecessary Code

1) There may be grade deductions for *unnecessary* code such as:
    - unused variables or functions
    - code that doesn't do anything (ex. `"use strict"` or `window.onload=...` in a module)
    - looping through an array that always has only one element in it
    - highly *inefficient* code that could easily be simplified
    - misuse of `for` or `while` loops in such a way that the resources of the browser are taxed
    - repeated blocks of code that have not been factored out into a common function (i.e. violating the D.R.Y. principle)
    - and so on. The amount of the grade deduction will vary in proportion to the severity of the violation

2) **What we *won't* deduct points for**:
    - the use of regular functions instead of the more compact syntax of ES6 Arrow Functions (regular JS functions are OK to use!)
    - minor stylistic differences (ex. we don't care where you place your curly braces, or whether you use spaces or tabs for indenting)
    - if you never use [array/object destructuring assignment](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Destructuring_assignment) (*although you really should use these when it makes sense!*)
    - if you prefer longer `if/else` syntax instead of the more terse versions such as 
      - [ternary operator](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Conditional_Operator)
      - [logical short circuiting](https://codeburst.io/javascript-what-is-short-circuit-evaluation-ff22b2f5608c?gi=523775959546)
      - [nullish-coalesing operator](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Nullish_coalescing_operator)
      - [logical nullish assignment](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Logical_nullish_assignment)
      - [optional chaining](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Optional_chaining)
      - etc ... (*although you really should use these!*)

<hr>

### III-C. JS Errors

1) Potential errors must be guarded against:
    - ex. checking to see if an object is "not nil" before trying to access a property of it
    - Code that could throw an exception needs a `try/catch` or a `.catch()`:
      - ex. `JSON.parse()` throws an exception when the string can't be converted to valid JSON
      - ex. `fetch()` throws an exception when there is a network error
    - the amount of the grade deduction will vary in proportion to the severity of the error

<hr>

### IV-D. Commenting your code

- Homework code DOES NOT have to be commented
- In your projects:
  - all functions and class methods MUST have a comment right before the declaration of the function/method that summarizes what it does
- You might (but don't have to) use the JSDoc commenting syntax:
  - https://jsdoc.app/
  - https://devhints.io/jsdoc
  - JSDoc comments in concert with VSCode give you type hinting and other features

```js
/**
 * Returns the sum of the two provided arguments
 *
 * @param {number} num1 - A number param
 * @param {number} num2 - A number param
 *
 * @example
 *
 *     addThem(1,2)
 */
 
function addThem(num1,num2){
  return num1 + num2;
}
```
