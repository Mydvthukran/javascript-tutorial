# JavaScript Tutorial

This repository is now a **complete JavaScript learning roadmap** you can use from beginner to advanced level.

## How to use this repo
1. Read one section at a time.
2. Run each code snippet in browser console or Node.js.
3. Modify examples and test edge cases.
4. Build mini projects after each major section.

---

## 1) JavaScript Basics
- What is JavaScript (ECMAScript, engine, runtime)
- `console.log`, comments, semicolons
- Variables: `let`, `const`, `var`
- Data types: `number`, `string`, `boolean`, `undefined`, `null`, `symbol`, `bigint`
- Operators: arithmetic, comparison, logical, assignment, ternary, nullish `??`, optional chaining `?.`
- Type conversion and coercion

```js
const age = 20;
const isAdult = age >= 18;
console.log(isAdult ? "Adult" : "Minor");
```

## 2) Control Flow
- `if`, `else if`, `else`
- `switch`
- Loops: `for`, `while`, `do...while`, `for...of`, `for...in`
- `break`, `continue`

```js
for (let i = 1; i <= 3; i++) {
  console.log(`Count: ${i}`);
}
```

## 3) Functions
- Function declaration, expression, arrow function
- Parameters, default params, rest params
- Return values
- Scope, lexical scope, closures
- IIFE
- Higher-order functions, callbacks

```js
function greet(name = "Learner") {
  return `Hello, ${name}`;
}
console.log(greet());
```

## 4) Arrays
- Create and access arrays
- Core methods: `push`, `pop`, `shift`, `unshift`, `slice`, `splice`
- Iteration: `forEach`, `map`, `filter`, `reduce`, `find`, `some`, `every`
- Sorting and searching
- Destructuring and spread

```js
const nums = [1, 2, 3, 4];
const doubled = nums.map((n) => n * 2);
console.log(doubled);
```

## 5) Objects
- Object literals and property access
- Methods and `this`
- Object utilities: `Object.keys`, `Object.values`, `Object.entries`, `Object.assign`
- Destructuring
- JSON (`JSON.stringify`, `JSON.parse`)

```js
const user = { name: "Dev", role: "Student" };
console.log(Object.keys(user));
```

## 6) Strings, Numbers, Dates, Math
- String methods and template literals
- Number formatting
- `Math` utilities
- `Date` basics
- `Intl` formatting

## 7) Advanced Functions & Objects
- Execution context, call stack
- `call`, `apply`, `bind`
- Prototypes and prototype chain
- Constructor functions
- Classes, inheritance, `super`
- Getters and setters

## 8) Error Handling
- `try...catch...finally`
- Throwing custom errors
- Defensive coding patterns

```js
try {
  JSON.parse("invalid");
} catch (error) {
  console.error("Parsing failed:", error.message);
}
```

## 9) Asynchronous JavaScript
- Synchronous vs asynchronous code
- Event loop, call stack, callback queue, microtasks
- Callbacks and callback hell
- Promises (`then`, `catch`, `finally`)
- `async/await`
- `fetch` API and API handling
- `Promise.all`, `Promise.allSettled`, `Promise.race`, `Promise.any`

```js
async function getTodo() {
  const res = await fetch("https://jsonplaceholder.typicode.com/todos/1");
  const data = await res.json();
  console.log(data);
}
```

## 10) DOM & Browser APIs
- DOM selection and traversal
- Events and event delegation
- Forms and validation
- Local storage / session storage
- Timers: `setTimeout`, `setInterval`
- Browser APIs: Geolocation, Clipboard, History

## 11) Modules & Tooling
- ES Modules: `import` / `export`
- CommonJS basics
- NPM basics
- Bundlers/transpilers (high level): Vite/Webpack/Babel
- Linting and formatting (ESLint/Prettier)

## 12) Modern JavaScript (ES6+)
- `let`/`const`, arrow functions
- Template literals
- Destructuring
- Spread/rest
- Enhanced object literals
- Optional chaining and nullish coalescing
- `Set`, `Map`, `WeakSet`, `WeakMap`

## 13) Important Core Concepts
- Hoisting
- Scope vs closure
- `this` in different contexts
- Equality: `==` vs `===`
- Pass by value vs reference
- Shallow vs deep copy
- Immutability basics
- Debounce and throttle
- Currying
- Memoization

## 14) Patterns and Best Practices
- DRY, KISS, SOLID (intro)
- Pure functions
- Separation of concerns
- Input validation
- Error-first mindset
- Security basics (XSS, safe DOM updates)

## 15) Testing JavaScript
- Unit, integration, end-to-end testing concepts
- Assertions and test structure (Arrange-Act-Assert)
- Mocking and stubbing concepts

## 16) Suggested Practice Projects
1. Calculator
2. To-do app
3. Weather app (API)
4. Quiz app
5. Expense tracker
6. Notes app with local storage
7. Small e-commerce cart

---

## 30-Day Learning Plan
- **Week 1:** Basics, control flow, functions, arrays
- **Week 2:** Objects, advanced functions, error handling
- **Week 3:** Async JavaScript, DOM, browser APIs
- **Week 4:** Modules, modern JS, testing, projects

---

## Quick Start Checklist
- [ ] I can explain all primitive data types
- [ ] I can write and use functions/closures
- [ ] I can use array methods (`map`, `filter`, `reduce`)
- [ ] I can manipulate DOM and handle events
- [ ] I can fetch API data with `async/await`
- [ ] I can build at least 2 small projects

If you want, next step I can also split this into separate lesson files like:
- `/lessons/01-basics.md`
- `/lessons/02-control-flow.md`
- ...up to advanced topics.
