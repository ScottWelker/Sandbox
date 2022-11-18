[Home](/Slalom-LLC/Slalom-Consulting) | [Glossary](/Glossary) | [Tech Ref](/Tech-Ref) | [Software Development](/Tech-Ref/Software-Development) | [JavaScript](/Tech-Ref/Software-Development/JavaScript) | [Node.js](/Tech-Ref/Software-Development/JavaScript/Node.js)
**Disambiguation:** [ES Modules (ESM)](/Tech-Ref/Software-Development/JavaScript/Module-\(JavaScript\)/ESM-\(ES-Modules\)), [Module (JavaScript)](/Tech-Ref/Software-Development/JavaScript/Module-\(JavaScript\)), [Package (npm)](/Tech-Ref/Software-Development/JavaScript/npm).
**AKA:** [Node.js Module](/Tech-Ref/Software-Development/JavaScript/Node.js).

[[_TOC_]]

---
# Introduction
|:warning: CAUTION!|
|:-|
| [ES Modules (ESM)](/Tech-Ref/Software-Development/JavaScript/Module-\(JavaScript\)/ESM-\(ES-Modules\)) is the newer, preferred, and native way to [modularize](/Tech-Ref/Software-Development/Modular-Programming) [JavaScript](/Tech-Ref/Software-Development/JavaScript) code. Still, you find considerable [packages (npm)](/Tech-Ref/Software-Development/JavaScript/npm) continuing to use ***CommonJS***. |

"_***CommonJS (CJS)*** is a project with the goal to establish conventions on the module ecosystem for [JavaScript](/Tech-Ref/Software-Development/JavaScript) outside of the [web browser](/Tech-Ref/WWW-\(World-Wide-Web\)/Web-Browser). The primary reason for its creation was a major lack of commonly accepted forms of [JavaScript](/Tech-Ref/Software-Development/JavaScript) module units which could be reusable in environments different from that provided by conventional [web browsers](/Tech-Ref/WWW-\(World-Wide-Web\)/Web-Browser) running [JavaScript](/Tech-Ref/Software-Development/JavaScript) scripts (e.g. [web servers](/Tech-Ref/WWW-\(World-Wide-Web\)/Web-Server) or [native desktop applications](/Tech-Ref/Software-Development/UX-\(User-Experience\)/Desktop-Applicataion))._"

CommonJS's module specification is widely used today, in particular for server-side JavaScript programming with Node.js._"

## Reference
1. [JavaScript Modules: A Brief History](https://objectpartners.com/2019/05/24/javascript-modules-a-brief-history/)
1. [Wikipedia: CommonJS](https://en.wikipedia.org/wiki/CommonJS)
1. [GeeksForGeeks: Node.js Modules](https://www.geeksforgeeks.org/node-js-modules/)
1. [NodeBeginner: What are Node.js modules?](https://www.nodebeginner.org/blog/post/nodejs-tutorial-what-are-node.js-modules/)
1. [How the module system, CommonJS & require works](https://blog.risingstack.com/node-js-at-scale-module-system-commonjs-require/).

---
# Topics
1. [Desktop Application](/Tech-Ref/Software-Development/UX-\(User-Experience\)/Desktop-Applicataion)).
1. [JavaScript](/Tech-Ref/Software-Development/JavaScript).
1. [Modular Programming](/Tech-Ref/Software-Development/Modular-Programming).
1. [Module (JavaScript)](/Tech-Ref/Software-Development/JavaScript/Module-\(JavaScript\)).
1. [Node.js](/Tech-Ref/Software-Development/JavaScript/Node.js).
1. [Web Browser](/Tech-Ref/WWW-\(World-Wide-Web\)/Web-Browser).
1. [Web Server](/Tech-Ref/WWW-\(World-Wide-Web\)/Web-Server).

---
# Modules
Modules are loaded via the global `require` statement. The `module` object's `exports` property defines what is available to the using (`require`) code.

- ![image.png](/.attachments/image-08260052-cc91-4222-a4ad-0a49ed260a0d.png)

## Core, Local, and Thrid-Party
Modules are of three types, core, local, and third-party.

### Core Modules
Core Modules are built-in modules that are part of the platform and come with Node.js installation. These modules can be loaded into the program by using the require function, e.g. 
```javascript
var module = require('module_name');
```
### Local Modules
Local Modules are those you create locally in your [Node.js](/Tech-Ref/Software-Development/JavaScript/Node.js) application.

### Third-party Modules
Third-party Modules are modules that are available online using the [Node Package Manager (NPM)](/Tech-Ref/Software-Development/JavaScript/npm). These modules can be installed in the project folder or globally.

## node_modules
