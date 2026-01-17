interview_questions:

  - question: What is hoisting in JavaScript?
    answer: Hoisting is JavaScript’s behavior of moving declarations to the top of their scope before code execution.
    example: |
      console.log(a);
      var a = 10;
      // Output: undefined

  - question: What is closure in JavaScript?
    answer: A closure is a function that remembers variables from its outer scope even after the outer function has finished execution.
    example: |
      function outer() {
        let count = 0;
        return function () {
          count++;
          return count;
        };
      }

  - question: What is the event loop in Node.js?
    answer: The event loop handles asynchronous operations by executing callbacks from the task and microtask queues after the call stack is empty.
    example: |
      console.log("A");
      setTimeout(() => console.log("B"), 0);
      console.log("C");
      // Output: A C B

  - question: Difference between let, var, and const?
    answer: var is function-scoped, let and const are block-scoped; const cannot be reassigned.
    example: |
      var a = 1;
      let b = 2;
      const c = 3;

  - question: What are callbacks in JavaScript?
    answer: A callback is a function passed as an argument to another function and executed later.
    example: |
      function greet(name, cb) {
        cb(name);
      }

  - question: What are promises in JavaScript?
    answer: A promise represents a value that may be resolved or rejected in the future.
    example: |
      new Promise((resolve) => resolve("Done"))
        .then(console.log);

  - question: What is the spread operator?
    answer: Spread operator expands elements of arrays or objects.
    example: |
      const arr = [1, 2];
      const newArr = [...arr, 3];

  - question: What is a higher-order function?
    answer: A function that takes another function as argument or returns a function.
    example: |
      const nums = [1,2,3];
      nums.map(n => n * 2);

  - question: What is destructuring in JavaScript?
    answer: Destructuring extracts values from arrays or objects into variables.
    example: |
      const { name } = { name: "JS" };

  - question: Difference between arrow and normal function?
    answer: Arrow functions do not have their own this and are not hoisted.
    example: |
      const fn = () => console.log(this);

  - question: What is rest operator?
    answer: Rest operator collects multiple values into an array.
    example: |
      function sum(...nums) {
        return nums.reduce((a,b) => a+b);
      }

  - question: Common array, string, object methods?
    answer: Common methods include map, filter, reduce, slice, split, Object.keys.
    example: |
      [1,2,3].map(n => n*2);

  - question: Debouncing in JavaScript and React?
    answer: Debouncing limits function execution until a delay passes.
    example: |
      function debounce(fn, delay) {
        let timer;
        return (...args) => {
          clearTimeout(timer);
          timer = setTimeout(() => fn(...args), delay);
        };
      }

  - question: What is middleware in Node.js?
    answer: Middleware is a function that executes between request and response.
    example: |
      app.use((req, res, next) => next());

  - question: Reconciliation and diffing in React?
    answer: React compares virtual DOM changes using diffing to update the real DOM efficiently.

  - question: Virtual DOM vs Real DOM?
    answer: Virtual DOM is a lightweight copy of real DOM used for performance optimization.

  - question: Difference between React.js and Next.js?
    answer: React is a UI library; Next.js is a React framework with SSR and routing.

  - question: Difference between SQL and NoSQL?
    answer: SQL uses structured tables; NoSQL uses flexible schemas.

  - question: ES6 features?
    answer: let/const, arrow functions, promises, spread, destructuring.

  - question: What is JSX?
    answer: JSX is a syntax extension that allows writing HTML-like code in JavaScript.

  - question: What are map, filter, reduce?
    answer: Array methods for transforming, filtering, and reducing data.
    example: |
      arr.filter(n => n > 2);

  - question: What is Babel?
    answer: Babel is a JavaScript compiler that converts modern JS into backward-compatible code.

  - question: What is SWC in Next.js?
    answer: SWC is a fast Rust-based compiler used by Next.js.

  - question: What are JavaScript, React, Node, Express, MongoDB?
    answer: JS is a language, React is UI library, Node is runtime, Express is framework, MongoDB is NoSQL DB.

  - question: Latest versions?
    answer: React 18+, Node 20+, AI: GPT-4/5 based models.

  - question: What is aggregation pipeline in MongoDB?
    answer: Aggregation pipeline processes data in stages like $match, $group, $project.

  - question: What is useEffect and lifecycle?
    answer: useEffect handles side effects and runs after render.

  - question: React hooks?
    answer: useState, useEffect, useContext, useMemo, useCallback, useRef.

  - question: useCallback vs useMemo?
    answer: useCallback memoizes functions; useMemo memoizes values.

  - question: How to optimize React & Node apps?
    answer: Code splitting, caching, lazy loading, indexing, clustering.

  - question: What is indexing in MongoDB?
    answer: Indexing improves query performance by reducing search space.

  - question: What are buffers and streams in Node.js?
    answer: Buffer handles binary data; streams handle continuous data flow.

  - question: What is bundling in React?
    answer: Bundling combines multiple files into a single optimized file.

  - question: What is clustering in Node.js?
    answer: Clustering uses multiple CPU cores to improve performance.

  - question: What is replica in MongoDB?
    answer: Replica sets provide high availability and data redundancy.

  - question: What are microservices?
    answer: Microservices architecture splits applications into small independent services.
