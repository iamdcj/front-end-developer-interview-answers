## JavaScript (ECMAScript)

#### Explain a Promise
---
A Promise allows a developer to run some asynchronous operation in the background, and handle the result of the operation when it resolves at some point in the future.

Technically a Promise is an object which represents the resolution of some asynchronous operation, the result can either be successful or a failure.

> Do this > carry-on > this finishes > do that with the result of this. 

#### Explain event delegation.
---
#### Explain how `this` works in JavaScript.
The `this` keyword points an object, which determines the calling context for functions within an application.  The calling context being the object which calls a function.

  ##### Can you give an example of one of the ways that working with `this` has changed in ES6?
  ES6 provides arrow functions, which provided a more expected mechanism of handling the calling context, i.e. the context of   an anonymous(arrow) function is bound to the parent context, not bound to the global object. It doesn't always suit when      working with DOM events, e.g. if you use an arrow function as the callback for a `click` event listener, then it won't bind to   the element object, but refer to the wrapping context.
  
---
#### Explain how prototypal inheritance works.
Objects in JS can inherit methods and properties from other objects via the built-in `prototype` property, which is present on every object in a program.

This is how prototypal inheritance works in the JS language;

```
// Create constructor
function Player(name, age, position) {
  this.name = name
  this.position = position
  this.age = age
}

// Create instance using constructor
const Xavi = new Player('Xavi', 'CM', 39)

// Add method to constructor function prototype
Player.prototype.bio = function() {
  console.info(`${this.name} is a ${this.age} year old ${this.position}`);
}

// access method via prototype
Xavi.bio(); 
// Xavi is a 39 year old CM
```

---
#### What's the difference between a variable that is: `null`, `undefined` or undeclared?
- A variable with a value of `null` is a variable that has been initialized with a value of `null`, usually to signify a lack of a true value.
- An `undefined` variable is a variable that has been declared, but not initialized with a value.
- An 'undeclared' variable is a variable that either doesn't exist, i.e. was never declared, or was created without a preceeding statement, e.g. `var` or `const`.

 ###### How would you go about checking for any of these states?
 ```
 const a = null;
 let b;
 ```
 
- Null: `if(a === null) {...}` or if(a) {...}`
- Undefined:  `if(b === undefined) {...}` or if(b) {...}`
- Undeclared: `if(c) {...}`
  
---
#### What is a closure, and how/why would you use one?
---
#### What language constructions do you use for iterating over object properties and array items?
---
#### Can you describe the main difference between the `Array.forEach()` loop and `Array.map()` methods and why you would pick one versus the other?
---
#### What's a typical use case for anonymous functions?
---
#### What's the difference between host objects and native objects?
---
#### Explain the difference between: `function Person(){}`, `var person = Person()`, and `var person = new Person()`?
---
#### Explain the differences on the usage of `foo` between `function foo() {}` and `var foo = function() {}`
---
#### Can you explain what `Function.call` and `Function.apply` do? What's the notable difference between the two?
---
#### Explain `Function.prototype.bind`.
---
#### What's the difference between feature detection, feature inference, and using the UA string?
---
#### Explain "hoisting".
---
#### Describe event bubbling.
---
#### Describe event capturing.
---
#### What's the difference between an "attribute" and a "property"?
---
#### What are the pros and cons of extending built-in JavaScript objects?
---
#### What is the difference between `==` and `===`?
---
#### Explain the same-origin policy with regards to JavaScript.
---
#### Why is it called a Ternary operator, what does the word "Ternary" indicate?
---
#### What is strict mode? What are some of the advantages/disadvantages of using it?
---
#### What are some of the advantages/disadvantages of writing JavaScript code in a language that compiles to JavaScript?
---
#### What tools and techniques do you use debugging JavaScript code?
---
#### Explain the difference between mutable and immutable objects.
  ##### What is an example of an immutable object in JavaScript?
  ##### What are the pros and cons of immutability?
  ##### How can you achieve immutability in your own code?
---
#### Explain the difference between synchronous and asynchronous functions.
---
#### What is event loop?
  ##### What is the difference between call stack and task queue?
---
#### What are the differences between variables created using `let`, `var` or `const`?
---
#### What are the differences between ES6 class and ES5 function constructors?
---
#### Can you offer a use case for the new arrow `=>` function syntax? How does this new syntax differ from other functions?
---
#### What advantage is there for using the arrow syntax for a method in a constructor?
---
#### What is the definition of a higher-order function?
---
#### Can you give an example for destructuring an object or an array?
```
const user = {
  name: "David",
  age: 32
}

const { name, age } = user;
```

---
#### Can you give an example of generating a string with ES6 Template Literals?
```
const name = "David";

const greeting = `My name is ${name}`
```
---
#### Can you give an example of a curry function and why this syntax offers an advantage?
---
#### What are the benefits of using `spread syntax` and how is it different from `rest syntax`?
---
#### How can you share code between files?
JavaScript now has native support for modules - modules allow you to export bindings from a file, and import them to other modules in the application.

---
#### Why you might want to create static class members?
---
#### Make this work:
```javascript
duplicate([1,2,3,4,5]); // [1,2,3,4,5,1,2,3,4,5]
```
##### Solution
```
const duplicate = arr => [...arr, ...arr]
```
---
#### Create a for loop that iterates up to `100` while outputting ########"fizz"######## at multiples of `3`, ########"buzz"######## at multiples of `5` and ########"fizzbuzz"######## at multiples of `3` and `5`
