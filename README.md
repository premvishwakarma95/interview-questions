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
- Virtual DOM → lightweight JavaScript object OR lightwight copy of real dom and used to optimize rendering.
- Real DOM → actual browser DOM

---

## 1️⃣7️⃣ React.js vs Next.js
- React → JS library that gives developer to create single page application, component, reconciliation, hooks, optimized.
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
**Babel** converts modern JavaScript into browser-compatible JavaScript OR converts ES6 JS into old JS is called babel or also we call it reactjs compiler.

---

## 2️⃣3️⃣ What is SWC in Next.js?
**SWC** is a fast Rust-based compiler used by Next.js.

---

## 2️⃣4️⃣ JavaScript, React, Node, Express, MongoDB
- JavaScript → JS is scripting langauge that runs on broswer handle and change brower content.
- React → JS library that gives developer to create single page application, component, reconciliation, hooks, optimized.
- Node.js → Node.js is a runtime environment that allows you to run JavaScript outside the browser, mainly on the server side.
- Express → Express.js is a lightweight Node.js framework that simplifies backend development and makes building APIs faster compared to using plain Node.js.
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

## 2️⃣9️⃣ How to Optimize React & Node Applications?

### 🔹 React.js Optimization Techniques

#### 1️⃣ Code Splitting
Code splitting loads only the required JavaScript instead of the entire app.

```jsx
import React, { Suspense } from "react";

const Dashboard = React.lazy(() => import("./Dashboard"));

function App() {
  return (
    <Suspense fallback={<div>Loading...</div>}>
      <Dashboard />
    </Suspense>
  );
}
```

#### 2️⃣ Lazy Loading
Lazy loading delays loading components or assets until they are needed.

```jsx
const Profile = React.lazy(() => import("./Profile"));
```

#### 3️⃣ Caching
Caching stores API responses or static assets to avoid repeated requests.

Examples:
- Browser cache
- Service workers
- React Query / SWR

### 🔹 Node.js Optimization Techniques

#### 4️⃣ Indexing
Indexes improve database query performance by reducing scan time.

```js
db.users.createIndex({ email: 1 });
```

#### 5️⃣ Clustering
Clustering allows Node.js to use multiple CPU cores.

```js
const cluster = require("cluster");
const os = require("os");

if (cluster.isMaster) {
  for (let i = 0; i < os.cpus().length; i++) {
    cluster.fork();
  }
} else {
  require("./server");
}
```

### 🔥 One-Line Interview Answer
> **React optimization focuses on reducing bundle size and re-renders, while Node.js optimization focuses on efficient CPU usage and faster database queries.**

---

## 3️⃣0️⃣ What is Indexing in MongoDB?
Indexing improves query performance by reducing scan time.

---

## 3️⃣1️⃣ Buffers & Streams in Node.js
- Buffer → binary data handle large files in bunch.
- Stream → continuous data flow handle data in one time like image or small size file.

---

## 3️⃣2️⃣ What is Bundle in ReactJS?
## 📦 Bundle in React.js (Interview Answer)

A **bundle** in React.js is the **compiled JavaScript file(s)** that contains:
- React components
- JS logic
- CSS & assets
- Third-party libraries

Bundlers like **Webpack, Vite, or SWC (Next.js)** convert **JSX & ES6+ code** into browser-readable JavaScript and combine everything into bundles.

### ⚠️ Issue
Large bundles slow down page load.

### ✅ Solution
Use **code splitting & lazy loading** to reduce initial load.

```jsx
const Page = React.lazy(() => import("./Page"));
```

### 🧠 One-Line Interview Answer
> **A bundle is the final compiled JavaScript file delivered to the browser to run a React application.**

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

## What is Apache and it's role?
- Apache is an open-source web server that handles client HTTP/HTTPS requests and serves web content such as HTML pages, images, and dynamic applications.
- Its role is to receive requests from browsers, process them (or forward them to backend logic like PHP), and return the appropriate response to the client.

---

## What is Nginx?
NGINX is a web server and reverse proxy. I mean nginx helps to interact and make connection from client to actual application port means our ec2 http port is 80 and nodejs port is 3000 so if user hits browser then first go to 80 and then 3000 then response so all this thing handles nginx.

---

## What is replica in mongodb?
sharding algorithm make copies of primary db, if primary db gets crashed then make primary to as secondary copy db so our nodejs app will never get crashed.

---

## What is sharding in mongodb?
This splits our db in multiple db this doesn’t store copy it store different data for example. It makes application faster.
- A DB - 1 to 1000 records
- B DB - 1001 to 2000 records
- C DB - 2001 to 3000 records 

---

## What is Indexing in mongodb?
Indexing in mongodb is an amazing thing it makes application or query optimized and faster if we create indexing in anything then i will not seach all the document directly go to that document and fetch it that’s the power of indexing. By default indexing is added in _id in mongodb.

---

## what is robot.txt file?
we describe in this what we are allowing or what not to craw in google.

---

what is sitemap.xml?
This defines where the crawling routes exist in the project.

### What is buffer in nodejs?
In Node.js, a Buffer is a built-in object used to handle raw binary data directly in memory.
- Buffer = temporary memory space used to store and work with binary data.

---

### Why do we use mongodb and why is this different and benefecial than other?
Mongodb is more powerful because in this we aggregate to filter data we can filteer data easily in this and can do query fast have indexing power that makes query faster and also we have and it is flexible we can store anything we want because it's flexible but in SQL we need to define everything but mongodb is nosql and it is flexible like we know in some fileds we don't need to store field or in some we can.

---

### Explain useMemo, useCallback, React.memo and lazy loading?
React.memo ->
- Memoizes a component
- Re-renders only if props change
```js
const Child = React.memo(({ count }) => {
  console.log("Child rendered");
  return <h2>Count: {count}</h2>;
});
```
 
useCallback -> 
- Functions are recreated on every render, causing child re-renders.
```js
const handleClick = useCallback(() => {
  setCount((c) => c + 1);
}, []);
```
 
useMemo ->
- Caches expensive calculation result
- Runs only when dependencies change
```js
const expensiveValue = useMemo(() => {
  console.log("Calculating...");
  return slowFunction(count);
}, [count]);
``` 

Lazy loading ->
```js
import { Suspense } from "react";
const Dashboard = React.lazy(() => import("./Dashboard"));
 
<Suspense fallback={<div>Loading...</div>}>
  <Dashboard />
</Suspense>
```

