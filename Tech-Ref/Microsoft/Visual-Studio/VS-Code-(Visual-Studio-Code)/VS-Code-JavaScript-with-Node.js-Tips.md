[Home](/Slalom-LLC/Slalom-Consulting) | [Glossary](/Glossary) | [Tech Ref](/Tech-Ref) | [Software Development](/Tech-Ref/Software-Development) | [Visual Studio Code](/Tech-Ref/Microsoft/Visual-Studio/VS-Code-\(Visual-Studio-Code\))

[[_TOC_]]

# Introduction
***Visual Studio Code*** tips and tricks for [JavaScript](/Tech-Ref/Software-Development/JavaScript) with [Node.js](/Tech-Ref/Software-Development/JavaScript/Node.js).

## Reference
1. [Node.js tutorial in Visual Studio Code](https://code.visualstudio.com/docs/nodejs/nodejs-tutorial) 

---
# Topics
1. [JavaScript](/Tech-Ref/Software-Development/JavaScript).
1. [Node.js](/Tech-Ref/Software-Development/JavaScript/Node.js).
1. [Visual Studio Code](/Tech-Ref/Microsoft/Visual-Studio/VS-Code-\(Visual-Studio-Code\)).

---
# Tips and Tricks

## Action Suggestions

### File is a CommonJS module...may be converted to an ES Module. (80001)
You'll likely have to just ignore this unless you are willing and able to upgrade the [module system](/Tech-Ref/Software-Development/JavaScript/Module-\(JavaScript\)) from [CommonJS](/Tech-Ref/Software-Development/JavaScript/Module-\(JavaScript\)/CJS-\(CommonJS\)) to [ES Modules (ESM)](/Tech-Ref/Software-Development/JavaScript/Module-\(JavaScript\)/ESM-\(ES-Modules\)) or, turn off all VS Code '_Action Suggestions._'
- ![image.png](/.attachments/image-a67590c8-d991-407c-b410-8cfc7cd00bdb.png)
   - [VS Code Issue #47299: File is a CommonJS module; it may be converted to an ES6 module.](https://github.com/Microsoft/vscode/issues/47299)
   - [StackOverflow: File is a commonJS module; it may be converted to an ES6 module. ts(80001)](https://stackoverflow.com/q/56627958/418950)
