# Basic JavaScript Questions

## Variables and Data Types

### 1. What's the difference between `let`, `const`, and `var`?
> The main difference is that `var` is function-scoped, while `let` and `const` are block-scoped. `let` lets you update a variable but not re-declare it, whereas `const` doesn’t allow you to do either. It’s more strict.

### 2. What are the different data types in JavaScript?
> In JavaScript, we have primitive data types like `Number`, `String`, `Boolean`, `Undefined`, `Null`, `Symbol`, and `BigInt`. And then there’s non-primitive types like `Object`, which include things like `Array`, `Function`, etc.

### 3. How do you check if a variable is an array?
> You can check by using the method `Array.isArray(variable)`. Simple as that.

### 4. What does the `typeof` operator do?
> The `typeof` operator gives back a string that tells you the type of the value it’s checking.

## Operators and Control Structures

### 5. What's the difference between `==` and `===`?
> `==` checks for value equality but allows type coercion (so it might convert types to make a match), while `===` is more strict—it checks for both value and type equality. No type conversion happens here.

### 6. How do you handle exceptions in JavaScript?
> To handle exceptions, you use `try`, `catch`, and `finally` blocks. The `try` block tests a piece of code for errors, `catch` takes care of the error if there’s one, and `finally` runs some code after the try/catch, no matter what.

## Functions

### 7. What is a callback function?
> A callback function is basically a function that you pass into another function as an argument, and then it gets executed inside that function to complete a task. Handy for asynchronous stuff.

### 8. Can you explain the `this` keyword in JavaScript?
> The `this` keyword refers to something different depending on the context. In a method, `this` refers to the object the method belongs to. In a function, `this` points to the global object (or undefined in strict mode). In an event handler, `this` refers to the element that got the event.

### 9. What's the `arguments` object?
> The `arguments` object is like an array, available inside functions, that contains all the arguments passed to the function. It’s old school, kinda replaced by modern rest parameters.

### 10. What are default parameters in JavaScript?
> Default parameters let you set default values for function parameters if no value or `undefined` is passed when calling the function.
> ```javascript
> function greet(name = 'Guest') { console.log(`Hello, ${name}`); }
> ```

## Arrays and Objects

### 11. How do you create an object in JavaScript?
> You can create objects using object literals, constructors, or even the `Object.create` method. There’s more than one way to do it!

### 12. How do you merge two objects in JavaScript?
> Merging two objects can be done with `Object.assign` or using the spread operator. Both works.
> ```javascript
> const merged = Object.assign({}, obj1, obj2);
> const merged = {...obj1, ...obj2};
> ```

### 13. How do you add an element to the start of an array?
> To add an element to the beginning of an array, use the `unshift` method.
> ```javascript
> array.unshift(element);
> ```

### 14. How do you remove the last element from an array?
> You can remove the last element from an array using the `pop` method.
> ```javascript
> array.pop();
> ```

### 15. How do you make a shallow copy of an array?
> Making a shallow copy is easy with the `slice` method or the spread operator.
> ```javascript
> const copy = array.slice();
> const copy = [...array];
> ```

### 16. How do you turn an array-like object into a real array?
> You can turn an array-like object into an actual array using `Array.from` or the spread operator.
> ```javascript
> const array = Array.from(arrayLike);
> const array = [...arrayLike];
> ```

## Strings

### 17. What are template literals and how do you use them?
> Template literals allow for embedded expressions, multi-line strings, and string interpolation. They’re wrapped in backticks (`` ` ``) instead of regular quotes.
> ```javascript
> const name = 'John';
> const message = `Hello, ${name}`;
> ```

### 18. How do you convert a string to a number in JavaScript?
> You can convert a string to a number using `parseInt(string)`, `parseFloat(string)`, `Number(string)`, or even the unary `+` operator.

## DOM Manipulation

### 19. What's the difference between `innerHTML` and `innerText`?
> `innerHTML` returns all the content including HTML tags, while `innerText` only gives you the plain text without any HTML.

### 20. How can you prevent the default behavior in an event handler?
> To prevent the default behavior, you just call `event.preventDefault()` inside the event handler.

## Events

### 21. What is event delegation?
> Event delegation is a technique that lets you handle events for multiple elements with a single event listener, taking advantage of event bubbling in the DOM.

### 22. What is event bubbling?
> Event bubbling is when an event starts from the target element and bubbles up through the parent elements up to the root of the document.

## Miscellaneous

### 23. What's `NaN` in JavaScript?
> `NaN` stands for "Not-a-Number" and represents a value that comes from a mathematical operation that doesn't result in a valid number.

### 24. What does `"use strict"` do?
> `"use strict"` turns on strict mode, which helps catch common coding mistakes and prevents certain actions. Makes your JavaScript safer and sometimes faster.

### 25. What is a polyfill?
> A polyfill is code that adds a feature to browsers that don’t support that feature natively, ensuring compatibility across different browsers.

### 26. What is CORS?
> CORS (Cross-Origin Resource Sharing) is a mechanism that allows restricted resources on a webpage to be requested from another domain outside the one the resource originated from.

### 27. What is hoisting in JavaScript?
> Hoisting is JavaScript's behavior of moving declarations to the top of the current scope. So, variable declarations (with `var`) and function declarations are hoisted, but their initializations aren't.

### 28. How do you check if an object is empty in JavaScript?
> You can check if an object is empty by checking the length of its keys:
> ```javascript
> Object.keys(obj).length === 0;
> ```

### 29. What's the purpose of `JSON.stringify`?
> `JSON.stringify` is used to convert a JavaScript object into a JSON string.

### 30. What's the purpose of `JSON.parse`?
> `JSON.parse` is used to convert a JSON string back into a JavaScript object.