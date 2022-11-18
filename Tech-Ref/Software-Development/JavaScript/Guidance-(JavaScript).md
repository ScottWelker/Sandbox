[Home](/Slalom-LLC/Slalom-Consulting) | [Glossary](/Glossary) | [Tech Ref](/Tech-Ref) | [Software Development](/Tech-Ref/Software-Development) | [JavaScript](/Tech-Ref/Software-Development/JavaScript)

[[_TOC_]]

---
# Introduction
|:warning: CAUTION!|
|:-|
|Information here is not guaranteed to be correct. **Question everything**. [I (SWelker)](/Individuals/Scott-Welker) am merely preserving research effort.|
| :seedling: [Wiki Gardening](/Tech-Ref/Wiki/Wiki-Gardening) Why not collapse this into the [JavaScript, Tips and Tricks](/Tech-Ref/Software-Development/JavaScript#tips-and-tricks)?|

This page is [my (SWelker)](/Individuals/Scott-Welker) collected [JavaScript](/Tech-Ref/Software-Development/JavaScript) wisdom. 
- :+1: See also [JavaScript, Tips and Tricks](/Tech-Ref/Software-Development/JavaScript#tips-and-tricks).

---
# Topics
1. [ECMAScript 2015](/Tech-Ref/Software-Development/JavaScript/ECMAScript/ECMAScript-2015).
1. [JavaScript ](/Tech-Ref/Software-Development/JavaScript).
1. [Programming 'Case' Types](/Tech-Ref/Software-Development/Programming-Case-Types).


---
# Tips and Tricks

## Dynamically Typed Language!
- "_[JavaScript (JS) is a dynamically typed language.](https://levelup.gitconnected.com/understanding-javascript-coercion-in-a-dynamically-typed-language-8807d6331fa2)._"

   - :star: **This has BIG implications!**
   - :+1: [TypeScript](/Tech-Ref/Software-Development/TypeScript) is said to support interfaces.

### No Interfaces
"_Instead, [JavaScript](/Tech-Ref/Software-Development/JavaScript) uses what's called [duck typing](https://en.wikipedia.org/wiki/Duck_typing). (If it walks like a duck, and quacks like a duck, as far as JS cares, it's a duck.) If your object has quack(), walk(), and fly() methods, code can use it wherever it expects an object that can walk, quack, and fly, without requiring the implementation of some "Duckable" interface._" ---[StackOverflow: Does JavaScript have... interface?](https://stackoverflow.com/a/3710367/418950)

## Iterating Arrays
- [How to Iterate Arrays (JavaScript)](/Tech-Ref/Software-Development/JavaScript/Guidance-\(JavaScript\)/How-to-Iterate-Arrays-\(JavaScript\)).

## String Interpolation
- [How can I do string interpolation in JavaScript?](https://stackoverflow.com/a/35984254/418950)
   - Since [ES6](/Tech-Ref/Software-Development/JavaScript/ECMAScript/ECMAScript-2015/ES6-\(ECMAScript-version-6\)), you can use [template literals](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Template_literals):

```javascript
const age = 3
console.log(`I'm ${age} years old!`)
```
