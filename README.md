# Node.js (A Summary) 

## Introduction to Node.js
[Source: https://nodejs.org/en/learn/getting-started/how-much-javascript-do-you-need-to-know-to-use-nodejs]

### What is Node.js?
- It is Open-source, cross-platform JavaScript runtime.
- It is built on Google Chrome’s V8 engine, allowing JS to run outside the browser.
- Ideal for building fast and scalable applications.

### Architecture & Performance:
- Single-threaded with non-blocking asynchronous I/O (Input/ Output).
- Handles thousands of concurrent connections without creating new threads.
- Avoids CPU waste by resuming operations once I/O responses return.
- Reduces thread management complexity and potential bugs.

### Developer Advantages:
- Allows frontend developers to write backend code using JavaScript.
- Supports modern ECMAScript features-you control the version via Node.
- Experimental features can be enabled via runtime flags.


### Uses: 
- Both frontend and backend
- It excels in performance, simplicity, and modern JavaScript support.


### JavaScript prerequisite for Node.js

#### i) What is recommended to learn before diving deep with Node.js?
- Lexical Structure
- Expressions
- Data Types
- Classes
- Variables
- Functions
- this operator
- Arrow Functions
- Loops 
- Scopes 
- Arrays
- Template Literals
- Strict Mode
- ECMAScript 2015 (ES6) and beyond
- Asynchronous JavaScript
  
#### ii) For Asynchronous Programming:
- Asynchronous Programming and Callbacks
- Timers
- Promises 
- Async and Await
- Closures 
- The Event Loop


### Difference between Node.js and the Browser

1. Same Language, Different Environments 
Both use JavaScript, but development experience is radically different.
Node.js allows full-stack development using a single language (JavaScript for both frontend and backend).

2. Ecosystem Differences:
Browser: Focus on DOM manipulation and Web APIs (e.g. document, window, cookies).
Node.js : Lacks browser-specific APIs but offers powerful modules (eg. filesystem, networking). 

3. Environment Control:
Node.js: You control the runtime version - can use the latest ECMAScript features freely.
Browser: Dependent on users’ browser versions - may need to transpile modern JS and tools like Babel.

4. Module Systems:
Node.js : Supports both CommonJS (require ()) and ES Modules (import).
Browser: Supports only ES Modules (import), and adoption is still evolving.

5. Developer Advantage
Using JavaScript across both client and server sides simplifies the learning curve and increases productivity for full-stack developers.


### The V8 JavaScript Engine:
#### What is V8? 
- JavaScript engine developed by Google, used in Google Chrome and Node.js
- Parses and executes JavaScript code; it does not include the DOM (Document Object Model) or Web APIs - those come from the browser.
- V8 is browser-independent, enabling its use in Node.js and other platforms.

#### Role (of V8)  in Node.js and Beyond:
- Chosen as the engine for Node.js in 2009.
- Powers not just servers but desktop apps too (eg. via Electron).
- A major reason behind the rise of JavaScript on the server-side

#### Other JavaScript Engines
- Firefox -> SpiderMonkey
- Safari - JavaScriptCore (aka Nitro)
- Microsoft Edge -> Originally Chakra, now V8 (via Chromium)
- All conform to the ECMAScript (ECMA -262_ standard

#### Probability & Development : 
- V8 is written in C++, runs on MAC, Windows, Linux, etc
- Continuously evolving for performance improvements.
- Part of an ongoing performance race among JS engines, benefiting both developers and users.

#### Compilation vs Interpretation in JavaScript (with V8)  [AI generated] 

##### Traditional Interpretation (Pre-V8 Era)
JavaScript was originally interpreted, meaning the code was read and executed line-by-line, directly and immediately by the browser.
While this made JavaScript simple and flexible, it came at the cost of performance—especially for large or complex applications.
Each time code ran, it had to be parsed and executed from scratch, with no reuse or optimization.

##### V8 and Just-In-Time (JIT) Compilation
V8 introduced a game-changing approach: Just-In-Time (JIT) Compilation.
Instead of purely interpreting JavaScript, V8 translates JavaScript into optimized machine code while the program is running.

###### This is done in stages:
- Initially interprets the code for quick startup.
- Then analyzes performance-critical parts (hot paths).
- Compiles those parts into machine code for faster execution.
- Continuously optimizes or de-optimizes code based on actual usage (adaptive optimization).

##### Why Is This Important?
In modern web apps, JavaScript codebases often have:
- Thousands of lines of code
- Intensive computations
- Apps that run for minutes or hours (e.g., Google Maps, online editors)
- In such cases, interpretation would be too slow and inefficient.
- JIT compilation ensures:
- Faster execution
- Lower CPU usage
- Better scalability for real-world applications
- Real-World Benefits
- Pages load faster.
- Applications run more smoothly.
- Users get a desktop-like experience in the browser.
- Developers don’t need to manually optimize performance at the machine level—V8 handles it intelligently.

##### Benefits:
- Faster Execution
- Lower CPU usage
- Scalable Performance
- Smoot user experiences

## Common npm CLI Commands

| Command                      | Description                                                              |
| ---------------------------- | ------------------------------------------------------------------------ |
| `npm init`                   | Initializes a new Node.js project and creates a `package.json` file.     |
| `npm install <package>`      | Installs a package and adds it to `node_modules`.                        |
| `npm install`                | Installs all dependencies listed in `package.json`.                      |
| `npm uninstall <package>`    | Removes a package and updates `package.json`.                            |
| `npm update`                 | Updates all the packages to the latest version based on version ranges.  |
| `npm run <script>`           | Runs a custom script defined in the `scripts` section of `package.json`. |
| `npm list`                   | Lists installed packages in the current project.                         |
| `npm outdated`               | Shows packages that are outdated.                                        |
| `npm audit`                  | Checks for known security vulnerabilities in dependencies.               |
| `npm install -g <package>`   | Installs a package globally.                                             |
| `npm uninstall -g <package>` | Uninstalls a globally installed package.                                 |
| `npm cache clean --force`    | Cleans the npm cache (useful for fixing install issues).                 |
| `npm run dev`                | Runs the development script (e.g., starts a dev server).                 |
| `npm start`                  | Runs the `start` script (commonly used to launch the app).               |
| `npm test`                   | Runs the `test` script (used for testing).                               |
| `npm build`                  | Runs the `build` script (e.g., to bundle/compile the app).               |


For more info [https://nodejs.org/en/learn/getting-started/fetch] 
