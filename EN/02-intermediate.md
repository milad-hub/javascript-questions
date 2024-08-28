# Intermediate JavaScript Questions

## Advanced Variables and Scopes

### 1. What's the difference between function scope and block scope?
> Function scope means variables are accessible inside a function, but block scope means variables are only accessible within the block where they’re defined, like inside an `if` or `for` loop.

### 2. How does Hoisting work in JavaScript?
> Hoisting means JavaScript moves declarations to the top of the current scope. Variable declarations (with `var`) and function declarations are hoisted, but not their initializations.

## Functions and Closures

### 3. What’s a Closure in JavaScript?
> A Closure is a function that has access to its own lexical scope even when the function is executed outside of that scope.

### 4. What are arrow functions, and how are they different from regular functions?
> Arrow functions have shorter syntax and bind `this` lexically, meaning from the surrounding scope. These functions don’t have their own `this`, `arguments`, `super`, or `new.target`.

### 5. What's the difference between `call`, `apply`, and `bind` methods?
> The `call` method invokes a function with a specific `this` value and arguments one by one. `apply` also invokes a function with a specific `this` but takes an array of arguments. `bind` returns a new function with a specific `this` value and optional arguments.

## Objects and Prototypes

### 6. Explain the prototype chain in JavaScript.
> The prototype chain is a series of links between objects created using `new` or `Object.create`. When a property on an object is accessed, the JavaScript engine traverses the prototype chain to find it.

### 7. What is the `__proto__` property?
> The `__proto__` property is a reference to the prototype object of the current object. It's used to access the prototype of an object and is part of the prototype chain.

### 8. How can you create an object using a constructor function?
> You can create an object by defining a function and using the `new` keyword to create instances:
> ```javascript
> function Person(name) {
>   this.name = name;
> }
> const john = new Person('John');
> ```

## Asynchronous JavaScript

### 9. What is a promise, and how do you use it?
> A promise is an object representing the eventual completion or failure of an asynchronous operation. You use `then` and `catch` methods to handle resolved and rejected states.

### 10. What does `async/await` mean in JavaScript?
> `async` functions return a promise and allow you to use `await` inside them to pause execution until the promise is either resolved or rejected. This makes async code look and behave more like synchronous code.

### 11. What is the event loop in JavaScript?
> The event loop is a mechanism that allows JavaScript to perform non-blocking operations by delegating tasks to the system kernel. It continuously checks the call stack and the callback queue, moving tasks to the call stack if it’s empty.

## Advanced Arrays and Objects

### 12. What's the difference between `map` and `forEach`?
> The difference is that `map` creates a new array with the results of calling a provided function on every element in the original array. `forEach` executes a provided function once for each array element but doesn’t return a new array.

### 13. How do you create a deep copy of an object?
> To create a deep copy, you can use a recursive function or use JSON methods:
> ```javascript
> const deepCopy = JSON.parse(JSON.stringify(original));
> ```

### 14. What is the spread operator, and how do you use it?
> The spread operator (`...`) allows an iterable, like an array or string, to be expanded.
> ```javascript
> const arr = [1, 2, 3];
> const newArr = [...arr, 4, 5];
> ```

### 15. What does destructuring mean in JavaScript?
> Destructuring is a syntax that lets you unpack values from arrays or properties from objects into separate variables.
> ```javascript
> const { a, b } = { a: 1, b: 2 };
> const [x, y] = [1, 2];
> ```

## DOM Manipulation and Events

### 16. Explain event delegation.
> Event delegation allows you to use a single event listener to manage similar events on multiple elements by leveraging event propagation in the DOM tree.

### 17. How do you create a custom event in JavaScript?
> To create a custom event, you can use the `CustomEvent` constructor:
> ```javascript
> const event = new CustomEvent('eventName', { detail: { key: 'value' } });
> ```

### 18. What's the difference between `window.onload` and `document.ready`?
> `window.onload` triggers when the whole page has fully loaded, including all dependent resources like stylesheets and images. `document.ready` triggers when the DOM is fully loaded, meaning the document structure is ready, but external resources might still be loading.

## Error Handling

### 19. How do you handle errors in a promise chain?
> To handle errors in a promise chain, you can use the `catch` method.

## Modules

### 20. What is a JavaScript module?
> A JavaScript module is a file that allows code to be imported and exported between different parts of an application using `import` and `export` statements. Modules help in organizing and encapsulating code.

## Miscellaneous Topics

### 21. What is a higher-order function in JavaScript?
> Higher-order functions are functions that can take other functions as arguments or return functions as results. Examples include `map`, `filter`, and `reduce`.

### 22. What does immutability mean in JavaScript?
> Immutability refers to the inability to change an object or data structure once it has been created. Instead of modifying the existing object, new objects with updated values are created.

### 23. What is currying in JavaScript?
> Currying is the process of transforming a function that takes multiple arguments into a series of functions that each take a single argument. This allows partial application of functions.

### 24. What is a Polyfill?
> A polyfill is code that implements a feature on web browsers that don’t natively support that feature, ensuring compatibility across different browsers.

### 25. What's the purpose of `Object.keys`?
> `Object.keys` returns an array of a given object's own enumerable property names.

### 26. What's the purpose of `Object.values`?
> `Object.values` returns an array of a given object's own enumerable property values.

### 27. What's the purpose of `Object.entries`?
> `Object.entries` converts an object into an array of key-value pairs.

### 28. What’s the difference between `slice` and `splice` methods?
> `slice` returns a shallow copy of a portion of an array into a new array. `splice` changes the contents of an array by removing or replacing existing elements and/or adding new elements.