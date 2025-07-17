Absolutely! Here's a **clear and detailed answer set** for each question, categorized as **Basic** and **Intermediate JavaScript Interview Questions**.

---

### ✅ Basic JavaScript Interview Questions – With Answers

1. **What is JavaScript?**
   JavaScript is a high-level, interpreted programming language used to make web pages interactive. It runs in the browser and supports object-oriented, functional, and imperative styles.

2. **What are the different data types in JavaScript?**

   * **Primitive Types**: string, number, boolean, null, undefined, symbol, bigint
   * **Non-Primitive (Reference) Types**: object, array, function

3. **Explain the difference between `var`, `let`, and `const`.**

   * `var` is function-scoped and allows re-declaration.
   * `let` is block-scoped and cannot be re-declared in the same scope.
   * `const` is also block-scoped but must be initialized and cannot be reassigned.

4. **What is Hoisting in JavaScript?**
   Hoisting is JavaScript's default behavior of moving declarations (not initializations) to the top of the current scope before code execution.

5. **What is the difference between `==` and `===` operators?**

   * `==` compares values after type coercion.
   * `===` compares both value and type (strict equality).

6. **What is the "this" keyword in JavaScript? How does its value change?**
   `"this"` refers to the object it's called on:

   * In a method → refers to the object
   * In global scope → `window` (in browsers)
   * In strict mode → `undefined`
   * In arrow functions → inherits from the surrounding lexical context

7. **What are "truthy" and "falsy" values in JavaScript? Give examples.**

   * **Falsy**: `false`, `0`, `''`, `null`, `undefined`, `NaN`
   * **Truthy**: all other values (like `'hello'`, `1`, `[]`, `{}`)

8. **Explain the concept of scope in JavaScript.**
   Scope determines the visibility of variables.

   * **Global Scope**: accessible everywhere
   * **Function Scope**: only accessible within functions
   * **Block Scope**: introduced by `let` and `const`

9. **What is an IIFE (Immediately Invoked Function Expression)? Why is it used?**
   An IIFE is a function that runs immediately after it's defined. Syntax:

   ```js
   (function() { /* code */ })();  
   ```

   It’s used to create a private scope and avoid polluting the global namespace.

10. **How do you handle errors in JavaScript?**
    Using `try...catch` blocks:

    ```js
    try {
      // code that might throw an error
    } catch (error) {
      console.error(error);
    }
    ```

---

### ✅ Intermediate JavaScript Interview Questions – With Answers

1. **What are Closures in JavaScript? Provide an example.**
   A closure is a function that remembers variables from its outer scope even after that scope has exited.

   ```js
   function outer() {
     let count = 0;
     return function inner() {
       count++;
       return count;
     };
   }
   const counter = outer();
   console.log(counter()); // 1
   console.log(counter()); // 2
   ```

2. **Explain `call()`, `apply()`, and `bind()` methods.**
   These methods change the `this` context of a function:

   * `call()`: `fn.call(thisArg, arg1, arg2, ...)`
   * `apply()`: `fn.apply(thisArg, [argsArray])`
   * `bind()`: returns a new function with `this` bound: `const boundFn = fn.bind(thisArg)`

3. **What are Promises? How do they help with asynchronous programming?**
   A Promise is an object representing the eventual completion or failure of an asynchronous operation. It helps avoid "callback hell".
   States: *pending*, *fulfilled*, *rejected*

   ```js
   fetch(url)
     .then(res => res.json())
     .catch(err => console.error(err));
   ```

4. **Explain `async`/`await`. How do they relate to Promises?**
   `async` functions return a Promise. `await` pauses the execution until the Promise is resolved.

   ```js
   async function fetchData() {
     try {
       const res = await fetch(url);
       const data = await res.json();
       console.log(data);
     } catch (err) {
       console.error(err);
     }
   }
   ```

5. **What is Event Delegation? Why is it useful?**
   Event delegation involves attaching a single event listener to a parent element instead of individual child elements.
   Useful for dynamic content and better performance.

   ```js
   document.getElementById("list").addEventListener("click", (e) => {
     if (e.target.tagName === "LI") {
       console.log("List item clicked");
     }
   });
   ```

6. **What is the Event Loop in JavaScript?**
   The Event Loop is a mechanism that handles asynchronous code execution by picking tasks from the queue and pushing them into the call stack when it's empty.

7. **Differentiate between `localStorage`, `sessionStorage`, and `cookies`.**

   | Feature        | localStorage | sessionStorage | cookies        |
   | -------------- | ------------ | -------------- | -------------- |
   | Expiry         | Never        | On tab close   | Manual/Expires |
   | Size Limit     | \~5MB        | \~5MB          | \~4KB          |
   | Sent to Server | No           | No             | Yes            |

8. **Explain prototypal inheritance in JavaScript.**
   JavaScript uses prototypes to inherit properties and methods. Objects can inherit from other objects via the prototype chain.

   ```js
   const parent = { greet() { console.log("Hello"); } };
   const child = Object.create(parent);
   child.greet(); // "Hello"
   ```

9. **What is the difference between `null` and `undefined`?**

   * `undefined`: a variable declared but not assigned a value
   * `null`: intentional absence of any object value

   ```js
   let a;        // undefined
   let b = null; // null
   ```

10. **Describe the purpose of `map()`, `filter()`, and `reduce()` array methods.**

* `map()`: transforms elements

  ```js
  [1,2,3].map(x => x * 2) // [2,4,6]
  ```
* `filter()`: returns elements that meet a condition

  ```js
  [1,2,3].filter(x => x > 1) // [2,3]
  ```
* `reduce()`: reduces array to a single value

  ```js
  [1,2,3].reduce((sum, x) => sum + x, 0) // 6
  ```

---

Let me know if you want these compiled as a PDF, flashcards, or a quiz for practice.
