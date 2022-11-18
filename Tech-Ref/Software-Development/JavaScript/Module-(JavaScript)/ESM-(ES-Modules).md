[Home](/Slalom-LLC/Slalom-Consulting) | [Glossary](/Glossary) | [Tech Ref](/Tech-Ref) | [Software Development](/Tech-Ref/Software-Development) | [JavaScript](/Tech-Ref/Software-Development/JavaScript) | [Node.js](/Tech-Ref/Software-Development/JavaScript/Node.js)
**Disambiguation:** [Module (JavaScript)](/Tech-Ref/Software-Development/JavaScript/Module-\(JavaScript\)), [Package (npm)](/Tech-Ref/Software-Development/JavaScript/npm).
**AKA:** ECMAScript Modules System (ESM), ES6.

[[_TOC_]]

---
# Introduction
***ES Modules (ESM)*** adds an official, standardized [module system](/Tech-Ref/Software-Development/JavaScript/Module-\(JavaScript\)) to [JavaScript (ES2015)](/Tech-Ref/Software-Development/JavaScript). All major [browsers](/Tech-Ref/WWW-\(World-Wide-Web\)/Web-Browser) now support _ES Modules_ as does (at least) [Node.js](/Tech-Ref/Software-Development/JavaScript/Node.js), and [WebAssembly (Wasm)](/Tech-Ref/Software-Development/Wasm-\(WebAssembly\)) is also said to be planning support (if not already).

## Reference
1. [JavaScript Modules: A Brief History](https://objectpartners.com/2019/05/24/javascript-modules-a-brief-history/)
1. [ES modules: A cartoon deep-dive](https://hacks.mozilla.org/2018/03/es-modules-a-cartoon-deep-dive/)
1. [Using ES modules in Node.js](https://blog.logrocket.com/es-modules-in-node-today/)
1. [Avoid these issues when using new ECMAScript modules in your Node.js application](https://www.darraghoriordan.com/2021/06/26/publishing-package-using-esm-esmodules/)
1. [Import ES6 Modules in Node.js](https://pakstech.com/blog/node-import-error/)

---
# Topics
1. [ECMA Script version 6 (ES6)](/Tech-Ref/Software-Development/JavaScript/ECMAScript/ECMAScript-2015/ES6-\(ECMAScript-version-6\))
1. [JavaScript](/Tech-Ref/Software-Development/JavaScript).
1. [Modular Programming](/Tech-Ref/Software-Development/Modular-Programming).
1. [Module (JavaScript)](/Tech-Ref/Software-Development/JavaScript/Module-\(JavaScript\)).
1. [Node.js](/Tech-Ref/Software-Development/JavaScript/Node.js).
1. [WebAssembly (Wasm)](/Tech-Ref/Software-Development/Wasm-\(WebAssembly\)).
1. [Web Browser](/Tech-Ref/WWW-\(World-Wide-Web\)/Web-Browser).

---
# Tips and Tricks

## .js Files as Modules
- [When you are using ECMAScript modules you are forced to provide the file extension](https://stackoverflow.com/a/68783000/418950).

## No 'node_modules' equivalent
- [StackOverflow: What is the es6 equivalent of node_modules?](https://stackoverflow.com/a/55676831/418950)

## SyntaxError

### Cannot use import statement outside a module
```cmd
SyntaxError: Cannot use import statement outside a module
```
Often this is because you lack a 'package.json' file and/or your 'package.json' file lacks the required ***ES Module (ESM)*** `"type": "module"`
- [ItsMyCode: Uncaught SyntaxError: cannot use import statement outside a module](https://itsmycode.com/solved-uncaught-syntaxerror-cannot-use-import-statement-outside-a-module/)
- [Blog: Fix - Cannot use import statement outside module in JS](https://bobbyhadz.com/blog/javascript-syntaxerror-cannot-use-import-statement-outside-module)
