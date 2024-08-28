# Advanced JavaScript Questions

## JavaScript Fundamentals

### 1. What is a JavaScript engine?
> A JavaScript engine is a program that executes JavaScript code. Examples include Google’s V8, Mozilla’s SpiderMonkey, and Microsoft’s Chakra.

### 2. Explain the concept of execution context and call stack in JavaScript.
> To explain, the execution context is the environment where JavaScript code is executed. This environment includes `this` binding, variables, objects, and functions. The call stack is a data structure called a stack that keeps track of function calls and helps the JavaScript engine know where to return after executing each function.

### 3. What is the event loop, and how does it work?
> The event loop allows JavaScript to perform non-blocking operations by delegating tasks to the system kernel whenever possible. It continuously checks the call stack and the callback queue and adds the first task from the queue to the call stack if the stack is empty.

## Advanced Functions and Closures

### 4. Explain the concept of higher-order functions and give an example.
> Higher-order functions are functions that can take other functions as arguments or return functions as results. Example:
> ```javascript
> function higherOrder(fn) {
>   // Returns a new function that takes a value and applies the input function to it
>   return function(value) {
>     return fn(value);
>   };
> }
> // Create a function called 'double' that doubles its input using the higherOrder function
> const double = higherOrder((x) => x * 2);
> console.log(double(5)); // 10
> ```

### 5. What are generators, and how do you use them?
> Generators are functions that can be paused in the middle and then resumed later. To define a generator, use the `function*` syntax and the `yield` keyword. Example:
> ```javascript
> function* generator() {
>   yield 1; // Pause and return 1
>   yield 2; // Pause and return 2
>   yield 3; // Pause and return 3
> }
> const gen = generator();
> console.log(gen.next().value); // 1
> console.log(gen.next().value); // 2
> console.log(gen.next().value); // 3
> ```

### 6. Explain the concept of memoization in JavaScript.
> Memoization is an optimization technique used to speed up function calls by caching the results of expensive function calls and returning the cached result when the same inputs occur again.

## Objects and Prototypes

### 7. What's the difference between `Object.create()` and `Object.assign()`?
> To explain, `Object.create()` creates a new object with a specified prototype and properties, while `Object.assign()` copies properties from one or more source objects to a target object.

### 8. What is a `Proxy` object, and how do you use it?
> A `Proxy` object is used to define custom behavior for fundamental operations (like property lookup, assignment, enumeration, and function invocation). Example:
> ```javascript
> const target = {};
> const handler = {
>   get: function(obj, prop) {
>     // Return the property's value if it exists, otherwise return 42
>     return prop in obj ? obj[prop] : 42;
>   }
> };
> const proxy = new Proxy(target, handler);
> console.log(proxy.answer); // 42
> ```

## Asynchrony and Performance Optimization

### 9. What's the difference between microtasks and macrotasks in the event loop?
> To explain, microtasks are tasks that execute after the current operation completes but before rendering. Examples include promises and `MutationObserver` callbacks. On the other hand, macrotasks are tasks that execute after rendering, such as `setTimeout`, `setInterval`, and I/O tasks.

### 10. What are Web Workers, and how do they improve performance?
> Web Workers allow you to run JavaScript code in the background, on a separate thread from the main thread. This makes it possible to perform heavy computations without blocking the user interface (UI).

## Advanced DOM Manipulation

### 11. What is Shadow DOM, and how do you use it?
> To explain, Shadow DOM is a web standard that allows you to encapsulate a DOM tree and CSS styles, hiding and separating them from the main document's DOM. This is useful for creating web components.

### 12. How can you effectively update the DOM to minimize reflows and repaints?
> To effectively update the DOM, batch DOM changes together, use `DocumentFragment`, minimize layout thrashing, and use `requestAnimationFrame` for animations.

## Memory Management

### 13. What is garbage collection in JavaScript?
> Garbage collection is the process that automatically frees up memory that's no longer in use. This means objects that are no longer needed or accessible are removed.

### 14. What are memory leaks, and how can you prevent them?
> Memory leaks occur when memory that has been allocated to something is not properly freed, causing memory usage to increase over time. To prevent this, you should remove references to objects that are no longer needed, avoid excessive use of global variables, and use tools like Chrome DevTools to monitor memory usage.

## Advanced Error Handling

### 15. What are custom errors, and how can you create them in JavaScript?
> Custom errors are user-defined errors that inherit from the built-in `Error` class. Example:
> ```javascript
> class CustomError extends Error {
>   constructor(message) {
>     super(message);
>     this.name = 'CustomError';
>   }
> }
> throw new CustomError('This is a custom error');
> ```

## Modules and Build Tools

### 16. What is the difference between ES6 modules and CommonJS modules?
> ES6 modules use `import` and `export` statements and are statically analyzed, allowing for tree shaking. CommonJS modules use `require` and `module.exports` and are dynamically loaded.

### 17. What are bundlers like Webpack, and why are they used?
> Bundlers like Webpack are tools that transform JavaScript modules into one or more optimized files for the browser. These tools help manage dependencies, perform code splitting, and optimize output for production.

## Security

### 18. What are the most common security vulnerabilities in JavaScript, and how can you mitigate them?
> Common vulnerabilities include XSS (Cross-Site Scripting), CSRF (Cross-Site Request Forgery), and code injection. You can mitigate these by validating and sanitizing user inputs, using Content Security Policy (CSP), and implementing proper authentication and authorization mechanisms.

## Advanced API and Browser Features

### 19. What are service workers, and how do they enable Progressive Web Apps (PWAs)?
> Service workers are scripts that run in the background and provide features like caching, push notifications, and background sync. These capabilities allow for offline usage and improved performance for Progressive Web Apps (PWAs).

### 20. Explain the use of IndexedDB in web applications.
> To explain, IndexedDB is a low-level API for storing large amounts of structured data in the browser. It provides asynchronous access to data and supports transactions, making it suitable for offline storage and complex data needs.

### 21. What is WebAssembly, and how does it interact with JavaScript?
> WebAssembly is a binary format for a stack-based virtual machine designed for compiling high-level languages like C, C++, and Rust. It allows code to run at near-native speed in the browser and can interact with JavaScript through APIs.

## Advanced Patterns and Practices

### 22. Explain the concept of functional programming and how it relates to JavaScript.
> Functional programming is a programming paradigm that treats computation as the evaluation of mathematical functions and avoids changing state and mutable data. JavaScript supports functional programming through first-class functions, higher-order functions, and methods like `map`, `reduce`, and `filter`.

### 23. What is the observer pattern, and how is it implemented in JavaScript?
> The observer pattern is a design pattern where an object (subject) maintains a list of dependencies (observers) and notifies them of state changes. This pattern can be implemented using event listeners or libraries like RxJS for reactive programming.

### 24. How can you implement debouncing and throttling in JavaScript?
> To explain, debouncing ensures that a function is only executed after a specified delay has passed since the last invocation. Throttling ensures that a function is executed at most once in a specified time period. Example:
> ```javascript
> function debounce(fn, delay) {
>   let timer;
>   return function(...args) {
>     // Clear the previous timer if it exists, and set a new timer
>     clearTimeout(timer);
>     timer = setTimeout(() => fn.apply(this, args), delay);
>   };
> }
> function throttle(fn, limit) {
>   let lastCall = 0;
>   return function(...args) {
>     const now = Date.now();
>     // If enough time has passed since the last call, execute the function
>     if (now - lastCall >= limit) {
>       lastCall = now;
>       fn.apply(this, args);
>     }
>   };
> }
> ```

### 25. What is the concept of duck typing in JavaScript?
> To explain, Duck typing is a concept where the usability of an object is determined based on the presence of certain methods and properties rather than its actual type. It's often described with the phrase

, "If it looks like a duck and quacks like a duck, then it's a duck."

### 26. What is tail call optimization, and how does it work in JavaScript?
> Tail call optimization is a feature in some JavaScript engines that optimizes recursive calls that are in tail position (the last operation in a function). This results in more efficient memory usage and can prevent stack overflow errors.