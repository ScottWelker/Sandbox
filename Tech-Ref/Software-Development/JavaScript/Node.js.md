[Home](/Slalom-LLC/Slalom-Consulting) | [Glossary](/Glossary) | [Tech Ref](/Tech-Ref) | [Software Development](/Tech-Ref/Software-Development) | [JavaScript](/Tech-Ref/Software-Development/JavaScript)
**AKA:** [Node](/Tech-Ref/Software-Development/JavaScript/Node.js/Node).
**Disambiguation:** [Deno](/Tech-Ref/Software-Development/JavaScript/Deno).

[[_TOC_]]

---
# Introduction
***Node.js*** "_...is an open-source, cross-platform, back-end [JavaScript](/Tech-Ref/Software-Development/JavaScript) runtime environment that runs on the V8 engine and executes [JavaScript](/Tech-Ref/Software-Development/JavaScript) code outside a [web browser](/Tech-Ref/WWW-\(World-Wide-Web\)/Web-Browser). Node.js lets developers use [JavaScript](/Tech-Ref/Software-Development/JavaScript) to write command line tools and for server-side scripting—running scripts server-side to produce dynamic [web page](/Tech-Ref/WWW-\(World-Wide-Web\)/Web-Page) content before the page is sent to the user's [web browser](/Tech-Ref/WWW-\(World-Wide-Web\)/Web-Browser). Consequently, Node.js represents a "[JavaScript](/Tech-Ref/Software-Development/JavaScript) everywhere" paradigm, unifying [web-application](/Tech-Ref/WWW-\(World-Wide-Web\)/Web-Application) development around a single programming language, rather than different languages for server-side and client-side scripts._"

## Reference
1. [Wikipedia: Node.js](https://en.wikipedia.org/wiki/Node.js)
1. [Node.js](https://nodejs.org/en/):
   - [Introduction to Node.js](https://nodejs.dev/learn)
1. [Run Node.js scripts from the command line](https://nodejs.dev/learn/run-nodejs-scripts-from-the-command-line)

---
# Topics
1. [index.js file](/Tech-Ref/Software-Development/JavaScript/Node.js/index.js-file).
1. [JavaScript](/Tech-Ref/Software-Development/JavaScript) ![programming-sm.png](/.attachments/programming-sm-84511b90-2d77-4364-8b25-7bee99dd4060.png).
1. [npm package manager](/Tech-Ref/Software-Development/JavaScript/npm).
1. [package.json file](/Tech-Ref/Software-Development/JavaScript/Node.js/package.json-file).
1. [pkg (Vercel)](/Tech-Ref/Software-Development/JavaScript/Node.js/pkg-\(Vercel\)).
1. [REPL (Read-Eval-Print-Loop) virtual environment](/Tech-Ref/Software-Development/JavaScript/Node.js/REPL-\(Read%2DEval%2DPrint%2DLoop\)) **AKA:**
   - [Node Shell](/Tech-Ref/Software-Development/JavaScript/Node.js/REPL-\(Read%2DEval%2DPrint%2DLoop\)/Node-Shell).
   - [Node.js Console](/Tech-Ref/Software-Development/JavaScript/Node.js/REPL-\(Read%2DEval%2DPrint%2DLoop\)/Node.js-Console).

1. [TypeScript](/Tech-Ref/Software-Development/TypeScript). ![programming-sm.png](/.attachments/programming-sm-84511b90-2d77-4364-8b25-7bee99dd4060.png)
1. [Yarn Package Manager](/Tech-Ref/Software-Development/JavaScript/Yarn).

---
# Objects (Node.js)

## Process
The ***process*** object provides information about, and control over, the current Node.js process.
- [Nodejs.org: Process object](https://nodejs.org/docs/latest/api/process.html#process)

### argv Property
- [Nodejs.org: process.argv](https://nodejs.org/docs/latest/api/process.html#processargv)

|Element|Description|Example|
|:-|:-|:-|
| 0 | The absolute pathname of the executable that started the Node.js process.| `C:\Program Files\nodejs\node.exe` |
| 1 | Path to the JavaScript file being executed. | `C:\SourceCode\Wiki\WikiTools\index.js` |
| N... |The remaining \[0...N\] elements are the additional command-line arguments (parameters).| Whatever was passed on the command line. For example the command line `node index.js one two three four`, yields `one`, `two`, `three`, and `four` for elements \[2..5\] respectively. See [Tips and Tricks, Command Line Parameters](#Command-Line-Parameters).|

---
# Node.js Frameworks and Tools
Node.js is a low-level platform. Thousands of community libraries are built upon Node.js. Here are just a few about which we have some notes in [this Wiki](/Tech-Ref/Microsoft/Microsoft-Azure/ADO-\(Azure-DevOps\)/Wiki-\(Azure-DevOps\)). 
- See also [this listing](https://nodejs.dev/learn#nodejs-frameworks-and-tools)

## JSDoc
- [JSDoc](/Tech-Ref/Software-Development/JavaScript/JSDoc).

## pkg (compile JS to EXE)
- [pkg (Vercel)](/Tech-Ref/Software-Development/JavaScript/Node.js/pkg-\(Vercel\)).

## markdown-it
- [markdown-it](/Tech-Ref/Software-Development/JavaScript/Node.js/markdown%2Dit).

## markdown-it-replace link
- [markdown-it-replace link](/Tech-Ref/Software-Development/JavaScript/Node.js/markdown%2Dit/markdown%2Dit%2Dreplace%2Dlink).

## markdown-link-check
- [markdown-link-check](/Tech-Ref/Software-Development/JavaScript/Node.js/markdown%2Dlink%2Dcheck).

## Serverless Framework (sls)
- [Serverless Framework (sls)](/Tech-Ref/Software-Development/JavaScript/Node.js/sls-\(Serverless-Framework\)).

## unified
- [unified](/Tech-Ref/Software-Development/JavaScript/Node.js/unified).

### remark (unified)
- [remark](/Tech-Ref/Software-Development/JavaScript/Node.js/unified/remark).

---
# Tips and Tricks

## Node.js Tips and Tricks

### Command Line Parameters
Within your invoked Node.js code, the invoking command line is accessed via the [Process](#Process) object's [argv property](#argv-property), e.g.: 

```javascript
process.argv.forEach(function (val, index, array) {
  console.log(index + ': ' + val);
});
```
### Exit Node.js Program
There are various ways to terminate a Node.js application. The `process.exit()` method is a common programmatic method.
- [How to exit from a Node.js program](https://nodejs.dev/learn/how-to-exit-from-a-nodejs-program)

### 'node_modules' Folder - Check-in or NOT?
**Generally, NO.** You do not check-in the `node_modules` folder. [npm](/Tech-Ref/Software-Development/JavaScript/npm) can reliably resolve these dependencies for your package users. However, there are exceptions to this rule, see [StackOverflow: Should I check in folder "node_modules"?](https://stackoverflow.com/a/19416403/418950)

Add this folder to your [git ignore file (.gitignore)](/Tech-Ref/Software-Development/DevOps-\(Development-and-IT-Operations\)/Git).

### Read Files with Node.js
   - [Read Files with Node.js](https://stackabuse.com/read-files-with-node-js/).

## Related Tools and Technologies

### JavaScript Tips and Tricks
   - [JavaScript Tips and Tricks](/Tech-Ref/Software-Development/JavaScript#tips-and-tricks).

#### Null and Undefined
- [JavaScript, Null and Undefined](/Tech-Ref/Software-Development/JavaScript#null-and-undefined) 

#### String Interpolation
- [JavaScript, String Interpolation](/Tech-Ref/Software-Development/JavaScript#string-interpolation) 

### npm Tips and Tricks
   - [npm Tips and Tricks](/Tech-Ref/Software-Development/JavaScript/npm#tips-and-tricks).

### VS Code JavaScript with Node.js Tips
   - [VS Code JavaScript with Node.js Tips](/Tech-Ref/Microsoft/Visual-Studio/VS-Code-\(Visual-Studio-Code\)/VS-Code-JavaScript-with-Node.js-Tips).
