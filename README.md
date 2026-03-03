# 📘 Full-Stack Interview Questions & Answers

---

## NodeJS 10 Interview Questions
https://roadmap.sh/questions/nodejs?fbclid=PAT01DUAQELJxleHRuA2FlbQIxMABzcnRjBmFwcF9pZA81NjcwNjczNDMzNTI0MjcAAacaHT4WABVVlH9lMGIQF_3nM6MJjC5lEvZ_sQoVWk4tJkAgeBEjMXVHs6m76Q_aem_YsUg6h-_tH4nnwMFzayqUw

---

## React Optimization steps
- learn from below repo of mine
- https://github.com/premvishwakarma95/react-optimization-steps

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
    
    // this return code will only run when code get rerender when query 
    // value change then first return code will be executed then above code on second rerender
    return () => clearTimeout(timer);   
  }, [query]);

// In JS, ( this js code is best example of closure concept as we can see timerId variable value needs to remember in return function. this variable is in lexial state.
function debounce(fn, delay) {
  let timerId;

  return function (...args) {
    const context = this;

    clearTimeout(timerId);

    timerId = setTimeout(() => {
      fn.apply(context, args);
    }, delay);
  };
}

function searchAPI(query) {
  console.log("API call for:", query);
}

const debouncedSearch = debounce(searchAPI, 500);

// simulate typing
debouncedSearch("R");
debouncedSearch("Re");
debouncedSearch("Rea");
debouncedSearch("Reac");
debouncedSearch("React");

// Output of this js code -> React
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
**SWC** is a fast Rust-based compiler used by Next.js. it stands for Speedy Web Compiler.

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

## 1 What is Apache and it's role?
- Apache is an open-source web server that handles client HTTP/HTTPS requests and serves web content such as HTML pages, images, and dynamic applications.
- Its role is to receive requests from browsers, process them (or forward them to backend logic like PHP), and return the appropriate response to the client.

---

## 2 What is Nginx?
NGINX is a web server and reverse proxy. I mean nginx helps to interact and make connection from client to actual application port means our ec2 http port is 80 and nodejs port is 3000 so if user hits browser then first go to 80 and then 3000 then response so all this thing handles nginx.

---

## 3 What is replica in mongodb?
sharding algorithm make copies of primary db, if primary db gets crashed then make primary to as secondary copy db so our nodejs app will never get crashed.

---

## 4 What is sharding in mongodb?
This splits our db in multiple db this doesn’t store copy it store different data for example. It makes application faster.
- A DB - 1 to 1000 records
- B DB - 1001 to 2000 records
- C DB - 2001 to 3000 records 

---

## 5 What is Indexing in mongodb?
Indexing in mongodb is an amazing thing it makes application or query optimized and faster if we create indexing in anything then i will not seach all the document directly go to that document and fetch it that’s the power of indexing. By default indexing is added in _id in mongodb.

---

### 6 what is robot.txt file?
we describe in this what we are allowing or what not to craw in google.

---

### 7 what is sitemap.xml?
This defines where the crawling routes exist in the project.

### 8 What is buffer in nodejs?
In Node.js, a Buffer is a built-in object used to handle raw binary data directly in memory.
- Buffer = temporary memory space used to store and work with binary data.

---

### 9 Why do we use mongodb and why is this different and benefecial than other?
Mongodb is more powerful because in this we aggregate to filter data we can filteer data easily in this and can do query fast have indexing power that makes query faster and also we have and it is flexible we can store anything we want because it's flexible but in SQL we need to define everything but mongodb is nosql and it is flexible like we know in some fileds we don't need to store field or in some we can.

---

### 10 Explain useMemo, useCallback, React.memo and lazy loading?
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

# 📦 Important clarification: "load" vs "bundle" in React
# ---------------------------------------
# Case 1: Normal import (NO lazy loading)
# ---------------------------------------

import Login from "./Login";
import About from "./About";
import Contact from "./Contact";

# ✔ All component files are bundled and downloaded at build time
# ✔ Browser receives Login, About, and Contact JS together
# ❌ Only the Login component is rendered (based on route)
# ❌ About and Contact are NOT mounted or executed

# 👉 Impact:
# - Larger initial bundle size
# - Slower first page load
# - No UI difference (only route component renders)

# ---------------------------------------
# Case 2: Lazy loading (Best Practice 🚀)
# ---------------------------------------

const Login = React.lazy(() => import("./Login"));
const About = React.lazy(() => import("./About"));
const Contact = React.lazy(() => import("./Contact"));

# ✔ Only Login JS is downloaded on initial load
# ✔ About and Contact are split into separate chunks
# ✔ They load ONLY when the user visits those routes

# 👉 Impact:
# - Smaller initial bundle size
# - Faster first load
# - Better performance and scalability

# ---------------------------------------
# Summary
# ---------------------------------------

# Normal Import  → All JS downloaded, only one page rendered
# Lazy Loading   → Only required JS downloaded per route

# Recommended: Use React.lazy() for route-based components

```

---

### 11 Serialization & Deserialization in MERN Flow?
Serialization
- Converting data (object) into a format that can be stored or sent over the network, i mean in format that machine understand in the network or server example object to json.
```js
const user = {
  name: "Prem",
  age: 26,
  role: "Developer"
};

// Serialize
const jsonData = JSON.stringify(user);

console.log(jsonData);
// {"name":"Prem","age":26,"role":"Developer"}

```

Deserialization
- Converting serialized data back into its original object form that we understand i mean we work with example json to object.
```js
app.use(express.json()); // this is deserialization

const response = '{"name":"Prem","age":26,"role":"Developer"}';

// Deserialize
const userObj = JSON.parse(response);

console.log(userObj.name); // Prem
```
React → Express → MongoDB → Express → React

---

### 12 Can we pass data in body in GET http method?
- Yes we can get body in GET http method req.body.
```js
app.get("/get-data", (req, res) => {
    console.log(req.body);  // Here we will get body data and can access body data if we will pass
    res.send("Welcome to the Todo API!");
});
```

---

### 13 Why don't we return or use more one parent in jsx in reactjs i mean to say please check in below code?
```js
// this code gives error
function App() {
  return (
    <h1>Hello</h1>
    <p>World</p>
  );
}

// After babel conversion
return (
  React.createElement("h1", null, "Hello"),
  React.createElement("p", null, "World")
);

```
output: 
- So babel converts it into like this and we know function cannot return two values that's why we get error.
```js
<>
  <h1>Hello</h1>
  <p>World</p>
</>

// converted into this
React.createElement(
  React.Fragment,
  null,
  React.createElement("h1", null, "Hello"),
  React.createElement("p", null, "World")
);

```
- And when we use empty fragments then it convert into like above code

---

### 14 What Temporal dead zone (TDC)?
- Temporal Dead Zone (TDZ) is the time between entering a scope and initializing a variable, where accessing that variable causes a ReferenceError.
```js
console.log(a); // ❌ ReferenceError So here this area is TDC for variable a and it's only for const and let variable because they are block scoped
let a = 10;
```

---

### 15 Explain Higher order component?
- A Higher-Order Component is a function that takes a component and returns a new component with additional functionality.
```js
import React from "react";

/* ================================
   Higher Order Component (HOC)
================================ */
function withAuth(WrappedComponent) {
  return function AuthComponent(props) {
    const isLoggedIn = true; // change to false to test

    if (!isLoggedIn) {
      return <h2 style={{ color: "red" }}>Please login first</h2>;
    }

    return <WrappedComponent {...props} />;
  };
}

/* ================================
   Normal Component
================================ */
function Dashboard({ user }) {
  return (
    <div>
      <h1>Dashboard</h1>
      <p>Welcome, {user}</p>
    </div>
  );
}

/* ================================
   Enhanced Component using HOC
================================ */
const ProtectedDashboard = withAuth(Dashboard);

/* ================================
   App Component
================================ */
export default function App() {
  return (
    <div style={{ padding: "20px" }}>
      <ProtectedDashboard user="Prem" />
    </div>
  );
}
```
- What’s Happening (Quick Explanation)
- withAuth → Higher-Order Component
- Dashboard → Original component
- ProtectedDashboard → Enhanced component
- withAuth(Dashboard) → HOC pattern
- 👉 The HOC adds authentication logic without modifying Dashboard.

---

## 16 If we have million data list how do we manage it in reactjs?
### Use virtualization
- react-window
- react-virtualized
```js
import React from "react";
import { FixedSizeList as List } from "react-window";

// Sample data: 10,000 items
const data = Array.from({ length: 10000 }, (_, index) => ({
  id: index + 1,
  name: `Item ${index + 1}`,
}));

// Row component
const Row = ({ index, style }) => {
  const item = data[index];
  return (
    <div
      style={{
        ...style,
        display: "flex",
        alignItems: "center",
        padding: "0 10px",
        borderBottom: "1px solid #eee",
        backgroundColor: index % 2 === 0 ? "#f9f9f9" : "#fff",
      }}
    >
      <span>{item.id}.</span>&nbsp;
      <span>{item.name}</span>
    </div>
  );
};

// Main List component
const VirtualizedList = () => {
  return (
    <div style={{ margin: "20px" }}>
      <h2>Virtualized List of 10,000 Items</h2>
      <List
        height={400}       // height of the container
        itemCount={data.length} // number of items
        itemSize={35}      // height of each row
        width={"100%"}     // width of the list
      >
        {Row}
      </List>
    </div>
  );
};
export default VirtualizedList;

---

// Another solution
import React from "react";
import { List } from "react-virtualized";
const data = Array.from({ length: 10000 }, (_, i) => `Item ${i + 1}`);
const rowRenderer = ({ index, key, style }) => (
  <div key={key} style={style}>
    {data[index]}
  </div>
);
export default function VirtualizedList() {
  return (
    <List
      width={300}          // list width
      height={400}         // viewport height
      rowCount={data.length} // number of rows
      rowHeight={30}       // height of each row
      rowRenderer={rowRenderer} // render function
    />
  );
}

```
Output:- This renders only visible items

---

## 17 Difference between microtask and macrotask in javascript event loop?
In JavaScript, microtasks and macrotasks are two different queues used by the event loop. Microtasks run first (Promise callbacks), macrotasks run later (timers like setTimeout / setInterval).
```js
console.log("A");

setTimeout(() => {
  console.log("B");
}, 0);

console.log("C");
```
Output:-
```css
A
C
B
```
```js
console.log("A");

Promise.resolve().then(() => {
  console.log("B");
});

console.log("C");
```
output:-
```css
A
C
B
```

---

## 18 What is Node.js, and how is it different from a browser's runtime environment?
Node.js is a server-side JavaScript runtime environment that allows you to execute code outside of a web browser. While a browser's runtime is for front-end web development, Node.js is for building back-end services, command-line tools, and network applications.

---

## 19 Explain the purpose of the JavaScript engine (V8) in Node.js.
The V8 JavaScript engine compiles JavaScript code into machine code, allowing Node.js to execute it very quickly. It's the same engine used in Chrome, which is why Node.js is so fast.

---

## 20 How would you debug a Node.js application?
I use vs code debugger or Chatgpt i mean ai or chorme dev tool. It depends on error then i think what should i do but now a days i mostly use AI to debug because we need to deliver work fastly so we need to be upgraded according to time.

---

## 21 What difference between Horizontal and Vertical scaling?
1️⃣ Vertical Scaling (Scale UP ⬆️)
You increase the power of a single server.
- More CPU
- More RAM
- More Disk
Same server → stronger server.
🧠 Example
You have:
```code
1 server
2 CPU
4 GB RAM
```
Traffic increases ➝ you upgrade to:
```code
1 server
8 CPU
32 GB RAM
```
✅ Same machine

2️⃣ Horizontal Scaling (Scale OUT ➡️)
You add more servers instead of making one bigger.
- Multiple servers
- Load balancer distributes traffic
🔧 Real-world Example
- Load balancer (Nginx / ALB)
- AWS Auto Scaling Group

---

## 22 How do you do error handling in nodejs?
In Node.js, I handle errors using a centralized error-handling approach.
I use try–catch for synchronous and async/await code, create custom error classes, pass errors using next(error) in Express, and handle them in a global error middleware.
I also handle unhandled promise rejections, validate inputs, and log errors properly without crashing the server.
✅ Step 1: Custom Error Class
```js
class AppError extends Error {
  constructor(message, statusCode) {
    super(message);
    this.statusCode = statusCode;
    this.status = `${statusCode}`.startsWith('4') ? 'fail' : 'error';
  }
}

module.exports = AppError;
```
✅ Step 2: Async Wrapper (Avoid repeating try–catch)
```js
const catchAsync = fn => {
  return (req, res, next) => {
    Promise.resolve(fn(req, res, next)).catch(next);
  };
};

module.exports = catchAsync;
```
✅ Step 3: Use in Controller
```js
const catchAsync = require('./catchAsync');
const AppError = require('./appError');

exports.getUser = catchAsync(async (req, res, next) => {
  const user = await User.findById(req.params.id);

  if (!user) {
    return next(new AppError('User not found', 404));
  }

  res.status(200).json({ user });
});
```
✅ Step 4: Global Error Middleware (MOST IMPORTANT)
```js
module.exports = (err, req, res, next) => {
  err.statusCode = err.statusCode || 500;
  err.status = err.status || 'error';

  res.status(err.statusCode).json({
    status: err.status,
    message: err.message
  });
};
```
Use this in app.js
```js
app.use(globalErrorHandler);
```

---

## 23 How would you secure you NodeJS application?
- Use JWT access and refresh token (Authentication).
- Role based access control (authorization).
- Rate limiting (only response in this time and only user can do 100 request per second).
- Add cors strategy and secure header.

---

## 24 Pure vs Impure function in JS.

### Pure function
A pure function:
- Always returns the same output for the same input
- Does not change anything outside its scope (no side effects)
```js
function add(a, b) {
  return a + b;
}

add(2, 3); // 5
add(2, 3); // 5 (always the same)
```

### Impure Function
An impure function:
- May return different results for the same input
- Has side effects
```js
let count = 0;

function increment() {
  count++;
  return count;
}

// Second function
function getCurrentTime() {
  return new Date().toLocaleTimeString();
}
```
🔁 Pure vs Impure (Side-by-Side)

| Feature                  | Pure Function | Impure Function  |
| ------------------------ | ------------- | ---------------- |
| Same input → same output | ✅ Yes         | ❌ Not guaranteed |
| Side effects             | ❌ No          | ✅ Yes            |
| Modifies external state  | ❌ No          | ✅ Yes            |
| Easy testing             | ✅ Very easy   | ❌ Hard           |
| Predictable              | ✅ Yes         | ❌ No             |


---

