[Home](/Slalom-LLC/Slalom-Consulting) | [Glossary](/Glossary) | [Tech Ref](/Tech-Ref) | [Software Development](/Tech-Ref/Software-Development) | [JavaScript](/Tech-Ref/Software-Development/JavaScript) | [Node.js](/Tech-Ref/Software-Development/JavaScript/Node.js)

[[_TOC_]]

---
# Introduction
***Create React App*** is an officially supported way to create [single-page](/Tech-Ref/WWW-\(World-Wide-Web\)/Web-Application/SPA-\(Single-Page-Application\)) applications with [React](/Tech-Ref/Software-Development/JavaScript/React), using [npm](/Tech-Ref/Software-Development/JavaScript/npm):
   - `npm install -g create-react-app`

Create React App is an [npm](/Tech-Ref/Software-Development/JavaScript/npm) package that offers a modern build setup with no configuration needed. It doesn’t handle backend logic or databases; it just creates a frontend build pipeline, so you can use it with any backend you want. Under the hood, it uses [Babel](/Tech-Ref/Software-Development/JavaScript/Babel) and [webpack](/Tech-Ref/Software-Development/JavaScript/webpack), but you don’t need to know anything about them.

This is an excellent way to get started with [React](/Tech-Ref/Software-Development/JavaScript/React). However, eventually, you'll need to "_[Eject](#eject!-beyond-the-simple-setup)_" or to move to another, more configurable setup. This is a good starting point.

## Reference
1. https://github.com/facebook/create-react-app
1. [Create-React-App.Dev: Create React App](https://create-react-app.dev/).
1. [ReactJS.org: Create React App](https://reactjs.org/docs/create-a-new-react-app.html#create-react-app).
1. :bulb: [JavaScriptStuff: Create React App vs Other Starter Projects](https://www.javascriptstuff.com/create-react-app/)

---
# Topics
1. [Babel](/Tech-Ref/Software-Development/JavaScript/Babel).
1. [webpack](/Tech-Ref/Software-Development/JavaScript/webpack).

---
# Tips and Tricks

## Eject! Beyond the Simple Setup
If you want to move beyond the simplistic **Create React App** setup, you'll have to ***eject***. Running `npm run eject` spits out all the configuration files so you can edit them yourself.

If you do this, you may be in for a shock. Your project will go from 3 dependencies to 49 dependencies.
