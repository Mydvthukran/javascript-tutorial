# JavaScript Tutorial

This repository is a **complete JavaScript learning roadmap** from beginner to advanced.
Each concept below includes a short explanation so you understand both **what it is** and **why it matters**.

## How to use this repo
1. Read one section at a time.
2. Run each snippet in browser console or Node.js.
3. Modify examples and test edge cases.
4. Build mini projects after each major section.

---

## 1) JavaScript Basics
- **What is JavaScript**: JavaScript is the language of the web, standardized as ECMAScript and executed by engines like V8.
- **Runtime vs engine**: The engine runs JS code; the runtime (browser/Node.js) adds APIs like DOM, fetch, timers, and file system access.
- **`console.log`, comments, semicolons**: `console.log` prints output, comments explain intent, and semicolons end statements (often optional but helpful).
- **Variables (`let`, `const`, `var`)**: `let` allows reassignment, `const` prevents reassignment, and `var` is function-scoped and mostly legacy.
- **Data types**: Primitive types (`number`, `string`, `boolean`, `undefined`, `null`, `symbol`, `bigint`) plus reference types like objects/arrays/functions.
- **Operators**: Arithmetic (`+`), comparison (`===`), logical (`&&`), assignment (`=`), ternary (`? :`), nullish (`??`), optional chaining (`?.`).
- **Type conversion/coercion**: JS can convert values explicitly (`Number("5")`) or implicitly (`"5" * 2`), which can cause subtle bugs.

```js
const age = 20;
const isAdult = age >= 18;
console.log(isAdult ? "Adult" : "Minor");
```

## 2) Control Flow
- **`if`, `else if`, `else`**: Execute different branches based on conditions.
- **`switch`**: Cleaner branching when comparing one value against many cases.
- **Loops**: `for` (counted), `while` (condition-first), `do...while` (runs at least once), `for...of` (values), `for...in` (keys).
- **`break` and `continue`**: `break` exits loops early; `continue` skips to next iteration.

```js
for (let i = 1; i <= 3; i++) {
  console.log(`Count: ${i}`);
}
```

## 3) Functions
- **Declaration, expression, arrow**: Different syntax forms for reusable logic.
- **Parameters**: Default params provide fallbacks; rest params collect variable arguments.
- **Return values**: Functions can produce outputs and make code composable.
- **Scope and lexical scope**: Variables are accessible based on where they are declared.
- **Closures**: Inner functions remember outer variables even after outer function finishes.
- **IIFE**: Immediately invoked function expression creates isolated scope instantly.
- **Higher-order functions/callbacks**: Functions can take/return other functions for flexible behavior.

```js
function greet(name = "Learner") {
  return `Hello, ${name}`;
}
console.log(greet());
```

## 4) Arrays
- **Create/access arrays**: Ordered lists indexed from `0`.
- **Core methods**: `push/pop` modify end; `shift/unshift` modify start; `slice/splice` copy/edit sections.
- **Iteration methods**: `forEach` (side effects), `map` (transform), `filter` (select), `reduce` (accumulate), `find/some/every` (search checks).
- **Sorting/searching**: `sort` can mutate and needs compare callbacks for numbers.
- **Destructuring/spread**: Extract values and copy/merge arrays cleanly.

```js
const nums = [1, 2, 3, 4];
const doubled = nums.map((n) => n * 2);
console.log(doubled);
```

## 5) Objects
- **Object literals**: Key-value structures for grouped data.
- **Property access**: Dot notation for known keys, bracket notation for dynamic keys.
- **Methods and `this`**: Methods are functions on objects; `this` usually points to the caller object.
- **Utilities**: `Object.keys/values/entries` inspect objects; `Object.assign` copies/merges.
- **Destructuring**: Pull properties into variables quickly.
- **JSON**: `JSON.stringify` converts to string; `JSON.parse` converts back to object.

```js
const user = { name: "Dev", role: "Student" };
console.log(Object.keys(user));
```

## 6) Strings, Numbers, Dates, Math
- **String methods/template literals**: Format and process text efficiently.
- **Number formatting**: Use methods like `toFixed` and `Intl.NumberFormat` for readable numeric output.
- **`Math` utilities**: Random values, rounding, min/max, powers, and trigonometry helpers.
- **`Date` basics**: Create dates, read components, and compute time differences.
- **`Intl` formatting**: Locale-aware formatting for dates, numbers, and currencies.

## 7) Advanced Functions & Objects
- **Execution context/call stack**: Understand how JS tracks function calls and variables during runtime.
- **`call`, `apply`, `bind`**: Control a function's `this` value and argument passing.
- **Prototypes/prototype chain**: Objects inherit behavior through linked prototypes.
- **Constructor functions**: Pre-class pattern for building multiple similar objects.
- **Classes/inheritance/`super`**: Modern syntax over prototypes for reusable object blueprints.
- **Getters/setters**: Controlled property read/write with function-like hooks.

## 8) Error Handling
- **`try...catch...finally`**: Catch runtime errors and run cleanup code regardless of success/failure.
- **Throwing custom errors**: Use `throw new Error(...)` for meaningful failure messages.
- **Defensive coding**: Validate inputs and fail early to avoid hidden bugs.

```js
try {
  JSON.parse("invalid");
} catch (error) {
  console.error("Parsing failed:", error.message);
}
```

## 9) Asynchronous JavaScript
- **Sync vs async**: Sync blocks step-by-step; async allows waiting without freezing the app.
- **Event loop model**: JS coordinates call stack, callback queue, and microtask queue.
- **Callbacks/callback hell**: Early async style; deep nesting hurts readability.
- **Promises**: Represent future success/failure with `then`, `catch`, `finally`.
- **`async/await`**: Cleaner promise syntax that reads like synchronous code.
- **`fetch` and APIs**: Request remote data and parse responses.
- **Promise combinators**: `all`, `allSettled`, `race`, `any` coordinate multiple async tasks.

```js
async function getTodo() {
  const res = await fetch("https://jsonplaceholder.typicode.com/todos/1");
  const data = await res.json();
  console.log(data);
}
```

## 10) DOM & Browser APIs
- **DOM selection/traversal**: Find and move through HTML elements.
- **Events/event delegation**: Respond to user actions efficiently, even for dynamic elements.
- **Forms/validation**: Collect and validate user input before processing.
- **Storage APIs**: `localStorage` persists data; `sessionStorage` lasts per tab session.
- **Timers**: `setTimeout` delays once; `setInterval` repeats on a schedule.
- **Browser APIs**: Geolocation, Clipboard, and History add richer app capabilities.

## 11) Modules & Tooling
- **ES Modules (`import`/`export`)**: Split code into reusable files with clear boundaries.
- **CommonJS**: Node.js legacy module system using `require`/`module.exports`.
- **NPM basics**: Install/manage packages and scripts.
- **Bundlers/transpilers**: Vite/Webpack/Babel optimize and transform code for browsers.
- **Linting/formatting**: ESLint and Prettier enforce consistency and catch mistakes.

## 12) Modern JavaScript (ES6+)
- **`let`/`const` and arrows**: Safer variables and concise function syntax.
- **Template literals**: String interpolation with backticks.
- **Destructuring**: Extract object/array parts in one line.
- **Spread/rest**: Expand or collect values elegantly.
- **Enhanced object literals**: Short property and method syntax.
- **Optional chaining/nullish**: Safer deep access and defaulting for null/undefined.
- **`Set`, `Map`, `WeakSet`, `WeakMap`**: Specialized collections for uniqueness, key-value mapping, and memory-sensitive references.

## 13) Important Core Concepts
- **Hoisting**: Declarations are processed before execution, with different behavior for `var`, `let`, `const`, and functions.
- **Scope vs closure**: Scope controls visibility; closure preserves outer state.
- **`this` behavior**: Depends on call-site, not where function is defined (except arrows, which inherit).
- **`==` vs `===`**: `==` coerces types; `===` checks strict equality.
- **Value vs reference**: Primitives copy by value; objects/arrays copy references.
- **Shallow vs deep copy**: Shallow copies nested references; deep copies duplicate nested structures.
- **Immutability**: Prefer returning new data over mutating shared state.
- **Debounce/throttle**: Control high-frequency events (typing, scrolling) for performance.
- **Currying**: Transform multi-arg functions into chained single-arg functions.
- **Memoization**: Cache expensive function results.

## 14) Patterns and Best Practices
- **DRY/KISS/SOLID (intro)**: Keep code reusable, simple, and maintainable.
- **Pure functions**: Same inputs produce same outputs without side effects.
- **Separation of concerns**: Keep logic, UI, and data responsibilities distinct.
- **Input validation**: Never trust external/user input blindly.
- **Error-first mindset**: Design for failure paths, not just happy paths.
- **Security basics**: Avoid XSS by sanitizing or safely rendering untrusted content.

## 15) Testing JavaScript
- **Unit/integration/E2E**: Test isolated functions, combined modules, and full user flows.
- **Assertions and AAA structure**: Arrange setup, Act on code, Assert expected results.
- **Mocking/stubbing**: Replace dependencies to test logic deterministically.

## 16) Suggested Practice Projects
1. Calculator (operators, state updates, edge-case handling)
2. To-do app (CRUD, filtering, persistence)
3. Weather app (API requests, loading/error states)
4. Quiz app (timers, scoring, UI transitions)
5. Expense tracker (data modeling, totals, charting)
6. Notes app with local storage (persistence + search)
7. Small e-commerce cart (state, price calculation, validation)

---

## 30-Day Learning Plan
- **Week 1:** Basics, control flow, functions, arrays.
- **Week 2:** Objects, advanced functions, error handling.
- **Week 3:** Async JavaScript, DOM, browser APIs.
- **Week 4:** Modules, modern JS, testing, projects.

---

## Quick Start Checklist
- [ ] I can explain all primitive data types.
- [ ] I can write and use functions and closures.
- [ ] I can use array methods (`map`, `filter`, `reduce`).
- [ ] I can manipulate DOM and handle events.
- [ ] I can fetch API data with `async/await`.
- [ ] I can build at least 2 small projects.

If you want, next step I can split this into separate lesson files like:
- `/lessons/01-basics.md`
- `/lessons/02-control-flow.md`
- ...up to advanced topics.
