<h1> JavaScript Questions Repository </h1>

Welcome to the **JavaScript Questions Repository**! Below is a step-by-step guide to JavaScript and ECMAScript features. Whether you are a full beginner or an experienced developer, you will be provided with helpful information and practical examples to enhance your JavaScript skills.

This repository contains a set of learning files about JavaScript and different features of ECMAScript. Each file is in Markdown format, with a clear explanation of the concepts and features alongside useful examples. The originals have been taken from w3schools.com, I have reorganized it and added further explanation to those topics. Also, all contents have been translated into Persian (Farsi) and added to this repository to make it more convenient for usage.

برای دسترسی به محتوای فارسی، به فایل [README-FA.md](README-FA.md) مراجعه کنید.

## 📚 Table of Contents

<h2> 📘 JavaScript Topics </h2>
<ul>
  <li><a href="#basic-topics">Basic Topics</a>: Covers foundational JavaScript concepts like data types, variables, operators, conditionals, and loops.</li>
  <li><a href="#intermediate-topics">Intermediate Topics</a>: Delves into functions, arrays, objects, error handling, callbacks, promises, DOM, and BOM.</li>
  <li><a href="#advanced-topics">Advanced Topics</a>: Explores OOP, memory management, advanced array and string methods, async/await, and module management.</li>
</ul>

<h2> 🧩 ECMAScript Features </h2>
<ul>
  <li><a href="#es5---2009-topics">ES5 - 2009</a>: Introduces "use strict", new methods for strings and arrays, and JSON handling.</li>
  <li><a href="#es6---2015-topics">ES6 - 2015</a>: Features `let`, `const`, arrow functions, destructuring, classes, promises, and more.</li>
  <li><a href="#es7---2016-topics">ES7 - 2016</a>: Adds exponentiation operators and the `includes` method for arrays.</li>
  <li><a href="#es8---2017-topics">ES8 - 2017</a>: Introduces string padding, object methods, async/await, and trailing commas.</li>
  <li><a href="#es9---2018-topics">ES9 - 2018</a>: Focuses on asynchronous iteration, new promise methods, object rest properties, and regex enhancements.</li>
  <li><a href="#es10---2019-topics">ES10 - 2019</a>: Adds `trimStart`, `trimEnd`, `Object.fromEntries`, flat and flatMap methods, and optional catch binding.</li>
  <li><a href="#es11---2020-topics">ES11 - 2020</a>: Introduces BigInt, `matchAll`, nullish coalescing, and optional chaining.</li>
  <li><a href="#es12---2021-topics">ES12 - 2021</a>: Adds `Promise.any`, `replaceAll`, and numeric separators.</li>
  <li><a href="#es13---2022-topics">ES13 - 2022</a>: Features `at` methods for arrays and strings, the `d` flag in regex, and `Object.hasOwn`.</li>
  <li><a href="#es14---2023-topics">ES14 - 2023</a>: Introduces `findLast`, `findLastIndex`, and safe array methods.</li>
  <li><a href="#es15---2024-topics">ES15 - 2024</a>: Covers new grouping methods and Temporal API features.</li>
</ul>

---

## 📘 JavaScript Topics

### Basic Topics
[View File](EN/01-basic.md)

<ul>
  <li>Introduction to JavaScript</li>
  <li>Data Types and Variables</li>
  <li>Operators and Expressions</li>
  <li>Conditional Structures</li>
  <li>Loops</li>
</ul>

### Intermediate Topics
[View File](EN/02-intermediate.md)

<ul>
  <li>Functions and Variable Scope</li>
  <li>Working with Arrays and Objects</li>
  <li>Error Handling</li>
  <li>Understanding Callbacks and Promises</li>
  <li>Introduction to DOM and BOM</li>
</ul>

### Advanced Topics
[View File](EN/03-advance.md)

<ul>
  <li>Object-Oriented Programming</li>
  <li>Memory Management and Optimization</li>
  <li>Advanced Methods for Arrays and Strings</li>
  <li>Using `async/await`</li>
  <li>Concepts of Modularity and Module Management</li>
</ul>

---

## 🧩 ECMAScript Features

### ES5 - 2009 Topics
[View File](EN/04-ES5-2009.md)

<ul>
  <li><a href="EN/04-ES5-2009.md#use-strict-in-javascript">"use strict" and its advantages</a>: Enforce stricter parsing and error handling in JavaScript.</li>
  <li><a href="EN/04-ES5-2009.md#accessing-string-characters-using-indexes">Accessing string characters using indexes</a>: Work with string characters like arrays.</li>
  <li><a href="EN/04-ES5-2009.md#multi-line-strings">Multi-line strings</a>: Handle strings that span multiple lines.</li>
  <li><a href="EN/04-ES5-2009.md#using-reserved-words-as-property-names">Using reserved words as property names</a>: Use reserved words as object property names safely.</li>
  <li><a href="EN/04-ES5-2009.md#stringtrim-method">String.trim Method</a>: Remove whitespace from both ends of a string.</li>
  <li><a href="EN/04-ES5-2009.md#arrayisarray-method">Array.isArray Method</a>: Check if a value is an array.</li>
  <li><a href="EN/04-ES5-2009.md#arrayforeach-method">Array.forEach Method</a>: Execute a function on each array element.</li>
  <li><a href="EN/04-ES5-2009.md#arraymap-method">Array.map Method</a>: Create a new array with the results of calling a function on every array element.</li>
  <li><a href="EN/04-ES5-2009.md#arrayfilter-method">Array.filter Method</a>: Create a new array with elements that pass a test.</li>
  <li><a href="EN/04-ES5-2009.md#arrayreduce-method">Array.reduce and reduceRight Methods</a>: Execute a reducer function on each element, resulting in a single output value.</li>
  <li><a href="EN/04-ES5-2009.md#arrayevery-method">Array.every and some Methods</a>: Test whether all or some elements pass a test.</li>
  <li><a href="EN/04-ES5-2009.md#arrayindexof-method">Array.indexOf and lastIndexOf Methods</a>: Find the index of an element in an array.</li>
  <li><a href="EN/04-ES5-2009.md#jsonparse-method">JSON.parse and JSON.stringify Methods</a>: Parse and stringify JSON data.</li>
  <li><a href="EN/04-ES5-2009.md#datenow-method">Date.now, toISOString, and toJSON Methods</a>: Work with date and time.</li>
  <li><a href="EN/04-ES5-2009.md#using-getters-and-setters">Using Getters and Setters</a>: Control access to object properties.</li>
  <li><a href="EN/04-ES5-2009.md#objectdefineproperty-method">Object.defineProperty Method</a>: Define a new property directly on an object.</li>
  <li><a href="EN/04-ES5-2009.md#objectcreate-method">Object.create Method</a>: Create a new object with a specified prototype object and properties.</li>
  <li><a href="EN/04-ES5-2009.md#objectkeys-method">Object.keys Method</a>: Return an array of a given object's own property names.</li>
  <li><a href="EN/04-ES5-2009.md#functionbind-method">Function.bind Method</a>: Create a new function that, when called, has its `this` keyword set to the provided value.</li>
  <li><a href="EN/04-ES5-2009.md#trailing-commas">Trailing Commas</a>: Use commas at the end of objects or arrays.</li>
</ul>

### ES6 - 2015 Topics
[View File](EN/05-ES6-2015.md)

<ul>
  <li><a href="EN/05-ES6-2015.md#let-keyword-in-javascript">let and const Keywords</a>: Introduce block-scoped variables.</li>
  <li><a href="EN/05-ES6-2015.md#arrow-functions">Arrow Functions</a>: Provide a concise syntax for writing functions.</li>
  <li><a href="EN/05-ES6-2015.md#object-destructuring">Object and Array Destructuring</a>: Extract values from arrays or properties from objects.</li>
  <li><a href="EN/05-ES6-2015.md#spread-operator">Spread Operator</a>: Expand elements in an iterable.</li>
  <li><a href="EN/05-ES6-2015.md#forof-loop">For/of Loop</a>: Iterate over iterable objects.</li>
  <li><a href="EN/05-ES6-2015.md#map-object">Map Object</a>: Hold key-value pairs and remember the original insertion order.</li>
  <li><a href="EN/05-ES6-2015.md#set-object">Set Object</a>: Store unique values of any type.</li>
  <li><a href="EN/05-ES6-2015.md#classes-in-javascript">Classes and Their Usage</a>: Provide a blueprint for creating objects.</li>
  <li><a href="EN/05-ES6-2015.md#promises-in-javascript">Promises</a>: Handle asynchronous operations.</li>
  <li><a href="EN/05-ES6-2015.md#symbol-data-type">Symbol Data Type</a>: Create unique identifiers.</li>
  <li><a href="EN/05-ES6-2015.md#default-parameters-in-functions">Default Parameters in Functions</a>: Set default values for function parameters.</li>
  <li><a href="EN/05-ES6-2015.md#rest-parameter-in-functions">Rest Parameter in Functions</a>: Represent an indefinite number of arguments as an array.</li>
  <li><a href="EN/05-ES6-2015.md#stringincludes-method">String.includes Method</a>: Check if a string contains a substring.</li>
  <li><a href="EN/05-ES6-2015.md#stringstartswith-method">String.startsWith and endsWith Methods</a>: Determine whether a string starts or ends with certain characters.</li>
  <li><a href="EN/05-ES6-2015.md#arrayentries-method">Array.entries, from, and keys Methods</a>: Work with arrays in new ways.</li>
  <li><a href="EN/05-ES6-2015.md#arrayfind-method">Array.find and findIndex Methods</a>: Find the first element or index that satisfies a condition.</li>
  <li><a href="EN/05-ES6-2015.md#new-math-methods">New Math Methods</a>: Perform mathematical operations.</li>
  <li><a href="EN/05-ES6-2015.md#new-number-features">New Number Features</a>: Work with numbers more effectively.</li>
  <li><a href="EN/05-ES6-2015.md#new-global-methods">New Global Methods</a>: New methods added to global objects.</li>
  <li><a href="EN/05-ES6-2015.md#modules-in-javascript">Modules in JavaScript</a>: Reuse code by importing and exporting modules.</li>
</ul>

### ES7 - 2016 Topics
[View File](EN/06-ES7-2016.md)

<ul>
  <li><a href="EN/06-ES7-2016.md#exponentiation-operator-in-javascript">Exponentiation Operator (**)</a>: Perform exponentiation more concisely.</li>
  <li><a href="EN/06-ES7-2016.md#exponentiation-assignment-operator">Exponentiation Assignment Operator (**=)</a>: Assign results of exponentiation to variables directly.</li>
  <li><a href="EN/06-ES7-2016.md#arrayincludes-method">Array.includes Method</a>: Check if an array contains a specific element.</li>
</ul>

### ES8 - 2017 Topics
[View File](EN/07-ES8-2017.md)

<ul>
  <li><a href="EN/07-ES8-2017.md#string-padding-in-javascript">String Padding (padStart and padEnd)</a>: Pad strings to a specific length.</li>
  <li><a href="EN/07-ES8-2017.md#objectentries-method">Object.entries and Object.values Methods</a>: Convert objects to arrays of key-value pairs or values.</li>
  <li><a href="EN/07-ES8-2017.md#asyncawait-syntax">Async/await Syntax</a>: Write asynchronous code more comfortably.</li>
  <li><a href="EN/07-ES8-2017.md#trailing-commas-in-functions">Trailing Commas in Functions</a>: Make function parameters lists more manageable.</li>
  <li><a href="EN/07-ES8-2017.md#objectgetownpropertydescriptors-method">Object.getOwnPropertyDescriptors Method</a>: Get all property descriptors of an object.</li>
</ul>

### ES9 - 2018 Topics
[View File](EN/08-ES9-2018.md)

<ul>
  <li><a href="EN/08-ES9-2018.md#asynchronous-iteration-loop">Asynchronous Iteration Loop</a>: Iterate over asynchronous data sources.</li>
  <li><a href="EN/08-ES9-2018.md#promiseprototypefinally-method">Promise.prototype.finally Method</a>: Execute a callback when a promise is settled, regardless of the outcome.</li>
  <li><a href="EN/08-ES9-2018.md#object-rest-properties">Object Rest Properties</a>: Extract parts of an object while keeping the rest.</li>
  <li><a href="EN/08-ES9-2018.md#new-regexp-features">New RegExp Features</a>: Enhance regular expressions with new capabilities.</li>
  <li><a href="EN/08-ES9-2018.md#shared-memory-in-javascript">Shared Memory in JavaScript</a>: Share data between threads or web workers safely.</li>
</ul>

### ES10 - 2019 Topics
[View File](EN/09-ES10-2019.md)

<ul>
  <li><a href="EN/09-ES10-2019.md#stringprototypetrimstart-and-stringprototypetrimend-methods">String.prototype.trimStart and trimEnd Methods</a>: Remove whitespace from the start or end of a string.</li>
  <li><a href="EN/09-ES10-2019.md#objectfromentries-method">Object.fromEntries Method</a>: Convert an array of key-value pairs into an object.</li>
  <li><a href="EN/09-ES10-2019.md#optional-catch-binding">Optional Catch Binding</a>: Simplify error handling by omitting the error parameter.</li>
  <li><a href="EN/09-ES10-2019.md#arrayprototypeflat-and-arrayprototypeflatmap-methods">Array.flat and Array.flatMap Methods</a>: Flatten nested arrays.</li>
  <li><a href="EN/09-ES10-2019.md#revised-arraysort-feature">Revised Array.sort Feature</a>: Ensure stable sorting of arrays.</li>
  <li><a href="EN/09-ES10-2019.md#revised-jsonstringify-feature">Revised JSON.stringify Feature</a>: Always produce valid Unicode strings.</li>
  <li><a href="EN/09-ES10-2019.md#use-of-separators-in-string-literals">Use of Separators in String Literals</a>: Make JSON a full superset of ECMAScript.</li>
  <li><a href="EN/09-ES10-2019.md#revised-functionprototypetostring-method">Revised Function.prototype.toString Method</a>: Return exact source code text.</li>
</ul>

### ES11 - 2020 Topics
[View File](EN/10-ES11-2020.md)

<ul>
  <li><a href="EN/10-ES11-2020.md#bigint-feature">BigInt</a>: Handle large integers safely without losing precision.</li>
  <li><a href="EN/10-ES11-2020.md#stringprototypematchall-method">String.prototype.matchAll Method</a>: Find all matches of a regex in a string.</li>
  <li><a href="EN/10-ES11-2020.md#nullish-coalescing-operator">Nullish Coalescing Operator (??)</a>: Provide a default value only for `null` or `undefined`.</li>
  <li><a href="EN/10-ES11-2020.md#optional-chaining-operator">Optional Chaining Operator (?.)</a>: Access properties deeply without worrying about `undefined` errors.</li>
  <li><a href="EN/10-ES11-2020.md#logical-and-assignment-operator">Logical AND Assignment Operator (&&=)</a>: Assign a value to a variable only if it is `true`.</li>
  <li><a href="EN/10-ES11-2020.md#logical-or-assignment-operator">Logical OR Assignment Operator (||=)</a>: Assign a value to a variable only if it is `false`, `null`, or `undefined`.</li>
  <li><a href="EN/10-ES11-2020.md#nullish-coalescing-assignment-operator">Nullish Coalescing Assignment Operator (??=)</a>: Assign a value to a variable only if it is `null` or `undefined`.</li>
  <li><a href="EN/10-ES11-2020.md#promiseallsettled-method">Promise.allSettled Method</a>: Wait for all promises to complete and handle all outcomes.</li>
  <li><a href="EN/10-ES11-2020.md#dynamic-import-feature">Dynamic Import Feature</a>: Load modules only when needed.</li>
</ul>

### ES12 - 2021 Topics
[View File](EN/11-ES12-2021.md)

<ul>
  <li><a href="EN/11-ES12-2021.md#promiseany-method">Promise.any Method</a>: Get the first successfully resolved promise out of several.</li>
  <li><a href="EN/11-ES12-2021.md#replaceall-method">replaceAll Method</a>: Replace all occurrences of a word or phrase in a string.</li>
  <li><a href="EN/11-ES12-2021.md#numeric-separators">Numeric Separators (_)</a>: Improve the readability of large numbers.</li>
</ul>

### ES13 - 2022 Topics
[View File](EN/12-ES13-2022.md)

<ul>
  <li><a href="EN/12-ES13-2022.md#arrayat-method">Array.at and String.at Methods</a>: Access elements or characters using positive or negative indices.</li>
  <li><a href="EN/12-ES13-2022.md#d-flag-in-regexp">d Flag in RegExp</a>: Provide exact start and end positions of matches.</li>
  <li><a href="EN/12-ES13-2022.md#objecthasown-method">Object.hasOwn Method</a>: Safely check if an object has a specific property.</li>
  <li><a href="EN/12-ES13-2022.md#errorcause-feature">error.cause Feature</a>: Attach detailed information about error causes.</li>
  <li><a href="EN/12-ES13-2022.md#await-import-feature">await import Feature</a>: Dynamically import modules using `await`.</li>
  <li><a href="EN/12-ES13-2022.md#class-field-declarations">Class Field Declarations</a>: Declare class variables directly inside the class.</li>
  <li><a href="EN/12-ES13-2022.md#private-methods-and-fields-in-classes">Private Methods and Fields in Classes</a>: Protect internal code from outside access.</li>
</ul>

### ES14 - 2023 Topics
[View File](EN/13-ES14-2023.md)

<ul>
  <li><a href="EN/13-ES14-2023.md#arrayfindlast-method">Array.findLast Method</a>: Find the last element that matches a condition.</li>
  <li><a href="EN/13-ES14-2023.md#arrayfindlastindex-method">Array.findLastIndex Method</a>: Find the index of the last element that matches a condition.</li>
  <li><a href="EN/13-ES14-2023.md#arraytoreversed-method">Array.toReversed Method</a>: Return a reversed copy of the array without modifying the original.</li>
  <li><a href="EN/13-ES14-2023.md#arraytosorted-method">Array.toSorted Method</a>: Return a sorted copy of the array without modifying the original.</li>
  <li><a href="EN/13-ES14-2023.md#arraytospliced-method">Array.toSpliced Method</a>: Return a modified copy of the array without altering the original.</li>
  <li><a href="EN/13-ES14-2023.md#arraywith-method">Array.with Method</a>: Return a new array with specified elements replaced.</li>
  <li><a href="EN/13-ES14-2023.md#-shebang-feature">#! (Shebang) Feature</a>: Specify the interpreter to execute a script file in Unix/Linux environments.</li>
</ul>

### ES15 - 2024 Topics
[View File](EN/14-ES15-2024.md)

<ul>
  <li><a href="EN/14-ES15-2024.md#objectgroupby-method">Object.groupBy Method</a>: Group elements of an array of objects based on a callback function result.</li>
  <li><a href="EN/14-ES15-2024.md#mapgroupby-method">Map.groupBy Method</a>: Similar to `Object.groupBy` but returns a `Map` for more flexibility in key types.</li>
  <li><a href="EN/14-ES15-2024.md#temporalplaindate-feature">Temporal.PlainDate Feature</a>: Manage dates without time-of-day information, perfect for calendar calculations.</li>
  <li><a href="EN/14-ES15-2024.md#temporalplaintime-feature">Temporal.PlainTime Feature</a>: Handle time without dates, ideal for representing times in a day with precision.</li>
  <li><a href="EN/14-ES15-2024.md#temporalplainmonthday-feature">Temporal.PlainMonthDay Feature</a>: Manage recurring dates like birthdays and anniversaries without associating a year.</li>
  <li><a href="EN/14-ES15-2024.md#temporalplainyearmonth-feature">Temporal.PlainYearMonth Feature</a>: Manage year-month combinations, useful for financial dates and monthly reporting.</li>
</ul>