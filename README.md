# 📘 Full-Stack Interview Questions & Answers

---

## 1️⃣ What is Hoisting in JavaScript?
**Hoisting** is JavaScript’s behavior of moving **declarations** to the top of their scope before code execution OR when varibles and functions get hoisted at the top of their scope is called hoisting.


```js
console.log(a);
var a = 10;
```

**Output**
```
undefined
```

**Explanation:**  
`var` is hoisted and initialized with `undefined`.

---

## 2️⃣ What is Closure in JavaScript?
A **closure** is a function that remembers variables from its **outer scope**, even after the outer function has finished execution.

```js
function outer() {
  let count = 0;
  return function () {
    return ++count;
  };
}
```

---

## 3️⃣ What is the Event Loop in Node.js?
The **event loop** allows Node.js to handle **non-blocking asynchronous operations** using the call stack, callback queue, and microtask queue and all time check call stack if it is empty then take process from callback and put it in stack and execute it is called event loop.

```js
console.log("A");
setTimeout(() => console.log("B"), 0);
console.log("C");
```

**Output**
```
A
C
B
```

---

## 4️⃣ Difference between `var`, `let`, and `const`
- `var` → function scoped, hoisted
- `let` → block scoped
- `const` → block scoped, cannot be reassigned

---

## 5️⃣ What are Callbacks in JavaScript?
A **callback** is a function passed as an argument to another function and executed later.

```js
function greet(name, cb) {
  cb(name);
}
```

---

## 6️⃣ What are Promises in JavaScript?
A **Promise** represents a value that will be **resolved or rejected** in the future.

```js
fetch(url).then(res => res.json());
```

---

## 7️⃣ What is the Spread Operator (`...`)?
The **spread operator** expands elements of arrays or objects.

```js
const arr = [1, 2];
const newArr = [...arr, 3];
```

---

## 8️⃣ What is a Higher-Order Function?
A function that **takes another function as an argument or returns a function**.

```js
[1, 2, 3].map(n => n * 2);
```

---

## 9️⃣ What is Destructuring?
Destructuring extracts values from arrays or objects.

```js
const { name } = { name: "JS" };
```

---

## 🔟 Arrow Function vs Normal Function
- Arrow functions do **not** have their own `this`
- Normal functions do

---

## 1️⃣1️⃣ What is the Rest Operator?
The **rest operator** collects multiple arguments into an array.

```js
function sum(...nums) {
  return nums.reduce((a, b) => a + b);
}
```

---

## 1️⃣2️⃣ Common Array, String & Object Methods
- Array → `map`, `filter`, `reduce`
- String → `split`, `slice`
- Object → `keys`, `values`

---

## 1️⃣3️⃣ What is Debouncing?
Debouncing limits function execution until a delay passes.

```js
// In ReeactJS
useEffect(() => {
    const timer = setTimeout(() => {
      setDebouncedQuery(query);
    }, 500); // delay in ms

    return () => clearTimeout(timer);
  }, [query]);

// In JS
function debounce(fn, delay) {
  let timer;
  return (...args) => {
    clearTimeout(timer);
    timer = setTimeout(() => fn(...args), delay);
  };
}
```

---

## 1️⃣4️⃣ What is Middleware in Node.js?
Middleware is a function that runs **between request and response**.

```js
app.use((req, res, next) => next());
```

---

## 1️⃣5️⃣ What is Reconciliation & Diffing in React?
React compares **Virtual DOM changes** and updates only required parts of the real DOM.

### Reconciliation
**Reconciliation** is the process React uses to **update the UI efficiently** when state or props change.

Instead of updating the entire DOM, React:
- Creates a **new Virtual DOM**
- Compares it with the **previous Virtual DOM**
- Updates only the **changed parts** in the Real DOM

### 🔍 Diffing
**Diffing** is the algorithm React uses during reconciliation to **find differences** between the old and new Virtual DOM trees.

---

## 1️⃣6️⃣ Virtual DOM vs Real DOM
- Virtual DOM → lightweight JavaScript object
- Real DOM → actual browser DOM

---

## 1️⃣7️⃣ React.js vs Next.js
- React → UI library
- Next.js → React framework with SSR & routing

---

## 1️⃣8️⃣ SQL vs NoSQL
- SQL → structured schema
- NoSQL → flexible schema

---

## 1️⃣9️⃣ ES6 Features
- `let`, `const`
- Arrow functions
- Promises
- Spread & Destructuring

---

## 2️⃣0️⃣ What is JSX?
JSX allows writing **HTML-like syntax in JavaScript**.

---

## 2️⃣1️⃣ map, filter, reduce
- `map` → transform
- `filter` → select
- `reduce` → combine

---

## 2️⃣2️⃣ What is Babel?
**Babel** converts modern JavaScript into browser-compatible JavaScript.

---

## 2️⃣3️⃣ What is SWC in Next.js?
**SWC** is a fast Rust-based compiler used by Next.js.

---

## 2️⃣4️⃣ JavaScript, React, Node, Express, MongoDB
- JavaScript → Language
- React → UI library
- Node.js → Runtime
- Express → Framework
- MongoDB → NoSQL Database

---

## 2️⃣5️⃣ Aggregation Pipeline in MongoDB
Processes data in stages like `$match`, `$group`, `$project`.

---

## 2️⃣6️⃣ What is `useEffect`?
Handles **side effects** and runs after render.

---

## 2️⃣7️⃣ React Hooks
- `useState`
- `useEffect`
- `useContext`
- `useMemo`
- `useCallback`
- `useRef`

---

## 2️⃣8️⃣ useCallback vs useMemo
- `useCallback` → memoizes functions
- `useMemo` → memoizes values

---

## 2️⃣9️⃣ How to Optimize React & Node Apps?
- Code splitting
- Lazy loading
- Caching
- Indexing
- Clustering

---

## 3️⃣0️⃣ What is Indexing in MongoDB?
Indexing improves query performance by reducing scan time.

---

## 3️⃣1️⃣ Buffers & Streams in Node.js
- Buffer → binary data
- Stream → continuous data flow

---

## 3️⃣2️⃣ What is Bundling?
Combining multiple files into one optimized file.

---

## 3️⃣3️⃣ What is Clustering in Node.js?
Uses multiple CPU cores to handle more requests.

---

## 3️⃣4️⃣ What is Replica in MongoDB?
Provides **high availability and redundancy**.

---

## 3️⃣5️⃣ What are Microservices?
Architecture where applications are split into **small independent services**.

---

### ✅ Why this is the **best way**
✔ Uses proper Markdown headings  
✔ Prevents line mixing  
✔ Looks professional on GitHub  
✔ Interview-friendly explanations  

---

If you want, I can:
- Add **more interview questions**
- Create **separate JS / React / Node sections**
- Convert this into **Q&A only format**
- Add **real project-based examples**

Just tell me 👍
