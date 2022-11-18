[Home](/Slalom-LLC/Slalom-Consulting) | [Glossary](/Glossary) | [Tech Ref](/Tech-Ref) | [Software Development](/Tech-Ref/Software-Development) | [JavaScript](/Tech-Ref/Software-Development/JavaScript) | [Node.js](/Tech-Ref/Software-Development/JavaScript/Node.js)
**Disambiguation:** [Package Manager](/Tech-Ref/Package-Manager).

[[_TOC_]]

---
# Introduction
Originally npm was simply the package manager for the "_[Node.js](/Tech-Ref/Software-Development/JavaScript/Node.js)_" [JavaScript](/Tech-Ref/Software-Development/JavaScript) library i.e., the ***Node Package Manager (npm)*** . 

The term and the package manager's use have expanded. 
- The package manager is now a prominent package manager for the [JavaScript](/Tech-Ref/Software-Development/JavaScript) ecosystem, including [React](/Tech-Ref/Software-Development/JavaScript/React). 
- The term ***npm*** may now refer to any or all of the following.

|#|npm Component| Notes |
|:-|:-|:-|
|1. <span id="npm-registry"/>| Software Library (Registry) | Known as the ***npm Registry*** this is an online database of public and paid-for private packages. |
|2. | Software Package Manager | "_***npm*** is the default package manager for the [JavaScript](/Tech-Ref/Software-Development/JavaScript) runtime environment [Node.js](/Tech-Ref/Software-Development/JavaScript/Node.js)._"|
|3. | Installer| Performs package installations via a command line interface (CLI). |

## Reference
1. [w3Schools: What is npm](https://www.w3schools.com/whatis/whatis_npm.asp)
1. [Wikipedia: npm (software)](https://en.wikipedia.org/wiki/Npm_(software))
1. [Blog: Npm (Node Package Manager)](https://mirzaleka.medium.com/exploring-javascript-ecosystem-popular-tools-frameworks-libraries-7901703ec88f#7eba).
1. [Beginner's Guide to NPM](https://dzone.com/articles/an-absolute-beginners-guide-to-using-npm-1)
1. [When to use Yarn over NPM?](https://stackoverflow.com/questions/40027819/when-to-use-yarn-over-npm-what-are-the-differences/40028313)

---
# Topics

## From Other Wiki Pages
1. [Chocolatey](/Tech-Ref/Microsoft/Microsoft-Windows/Chocolatey).
1. [Lerna](/Tech-Ref/Software-Development/DevOps-\(Development-and-IT-Operations\)/Monorepo-\(Disambiguation\)/Lerna).
1. [Node.js](/Tech-Ref/Software-Development/JavaScript/Node.js).

## npm init (Initialize npm Package)
- The `npm init` command initializes the working folder as an npm package. It is a step-by-step tool (a '_[Wizard](/Tech-Ref/Software-Development/Wizard)_') used to scaffold out your [Node.js](/Tech-Ref/Software-Development/JavaScript/Node.js) project. It will prompt you for input for a few aspects of the project and populate your starting [package.json file](/Tech-Ref/Software-Development/JavaScript/Node.js/package.json-file) accordingly.
   - [npm-init](https://docs.npmjs.com/cli/v8/commands/npm-init)

## npm install
- Installs a package and any packages that it depends on.
   - [npm-install](https://docs.npmjs.com/cli/v8/commands/npm-install)
      - The `--save-dev` option adds the third-party package to the package's development dependencies. It won't be installed when someone runs npm install directly to install your package. It's typically only installed if someone clones your source repository first and then runs npm install in it. --[What is the difference between --save and --save-dev?](https://stackoverflow.com/a/42247824/418950)

## npx (Node Package Execute)
-  Added in ***npm*** version 5.2, ***Node Package Execute (npx)*** runs code built with [Node.js](/Tech-Ref/Software-Development/JavaScript/Node.js) and published through the [npm registry](#npm-registry).

---
# Tips and Tricks

## Create React App
- [Create React App](/Tech-Ref/Software-Development/JavaScript/npm/Create-React-App).

## Install Output (03/22/2021)
|:seedling: [Wiki Gardening](/Tech-Ref/Wiki/Wiki-Gardening)! |
|:-|
| [I (SWelker)](/Individuals/Scott-Welker) failed to record sufficient context. Presumably this section relates to my initial `npm` installation. However, I can't be sure. That requires verification or pruning (deletion). |

[I (SWelker)](/Individuals/Scott-Welker) noted these updates:

<details>
  <summary>Show/hide</summary>

```dos
Chocolatey v0.10.15
python;visualstudio2017-workload-vctools
chocolatey-core.extension v1.3.5.1 [Approved]
chocolatey-windowsupdate.extension v1.0.4 [Approved]
KB3035131 v1.0.3 [Approved]
KB3033929 v1.0.5 [Approved]
KB2919442 v1.0.20160915 [Approved]
KB2919355 v1.0.20160915 [Approved]
KB2999226 v1.0.20181019 [Approved] - Possibly broken
vcredist140 v14.28.29913 [Approved]
vcredist2015 v14.0.24215.20170201 [Approved]
python3 v3.9.2 [Approved]
chocolatey-visualstudio.extension v1.9.0 [Approved]
visualstudio-installer v2.0.1 [Approved]
chocolatey-dotnetfx.extension v1.0.1 [Approved]
dotnetfx v4.8.0.20190930 [Approved]
visualstudio2017buildtools v15.9.34.0 [Approved]
visualstudio2017-workload-vctools v1.3.3 [Approved]
```
</details>
<br/>

[Chocolatey](/Tech-Ref/Microsoft/Microsoft-Windows/Chocolatey) noted:
<details>
  <summary>Show/hide</summary>

```dos
chocolatey upgraded 17/17 packages.
 See the log for details (C:\ProgramData\chocolatey\logs\chocolatey.log).

Upgraded:
 - chocolatey-dotnetfx.extension v1.0.1
 - kb3033929 v1.0.5
 - python3 v3.9.2
 - visualstudio2017buildtools v15.9.34.0
 - chocolatey-windowsupdate.extension v1.0.4
 - vcredist140 v14.28.29913
 - kb2999226 v1.0.20181019
 - visualstudio-installer v2.0.1
 - kb2919355 v1.0.20160915
 - chocolatey-core.extension v1.3.5.1
 - kb2919442 v1.0.20160915
 - visualstudio2017-workload-vctools v1.3.3
 - chocolatey-visualstudio.extension v1.9.0
 - vcredist2015 v14.0.24215.20170201
 - dotnetfx v4.8.0.20190930
 - kb3035131 v1.0.3
 - python v3.9.2

Packages requiring reboot:
 - vcredist140 (exit code 3010)

The recent package changes indicate a reboot is necessary.
```
</details>

## npm ERROR

### Error: Could not find module...

## npm WARN

### No repository field.
- ![image.png](/.attachments/image-f60e2b21-748d-468a-a7df-62cd1f341409.png)

This warning indicates your package ([package.json file](/Tech-Ref/Software-Development/JavaScript/Node.js/package.json-file)) could play nicer with others. Unless you are collaborating with others this is probably no concern and can be suppressed by adding the `private` [key-value pair (KVP)](/Tech-Ref/Software-Development/JSON-\(JavaScript-Object-Notation\)/KVP-\(Key%2DValue-Pair\)) to your [package.json file](/Tech-Ref/Software-Development/JavaScript/Node.js/package.json-file), e.g. `"private": true,`

- [StackOverflow: npm WARN ... No repository field](https://stackoverflow.com/a/16827990/4189500)
   - [repository KVP (Docs.npmjs)](https://docs.npmjs.com/cli/v8/configuring-npm/package-json#repository).
   - [private KVP (Docs.npmjs)](https://docs.npmjs.com/cli/v8/configuring-npm/package-json#private).

## What is the difference between –save and –save-dev
- [What is the difference between –save and –save-dev](https://www.geeksforgeeks.org/what-is-the-difference-between-save-and-save-dev-in-node-js/)
   - `npm install [package-name] –save`: When `–save` is used without `-dev`, it signifies that the package is core dependency. A **core dependency** is any package without which the application cannot perform its intended work. In package.json file under the dependencies section contains the list of core dependencies.
   - `npm install [package-name] –save-dev`: When `–save-dev` is used with npm install, it signifies that the package is a **development dependency**. A development dependency is any package that absence will not affect the work of the application. In package.json file under the devDependencies section contains the list of all development dependencies. 

## Where does npm install packages?
:+1: [I (SWelker)](/Individuals/Scott-Welker) am unsure of best practices but, I tend to perform **Non-global** install unless or until I am certain that I need something globally.
- [StackOverflow: Where does npm install packages?](https://stackoverflow.com/questions/5926672/where-does-npm-install-packages/5926706#5926706)

### Non-global libraries
Non-global libraries are installed the node_modules sub folder in the folder you are currently in.
   - `npm list`

### Global Libraries (npm install -g <package_name>)

#### Where?
Where are global packages installed?
   - `npm root -g`:
   - ![image.png](/.attachments/image-285ed720-425a-4b7b-b527-b767c438ce00.png)

#### What/Where?
What global packages are installed and where? 
- :warning: If you are on a developer's system, you'll probably find **way more** globally installed packages than you suspect. Many, many "_things_" rely on, and install, global packages. I've truncated the image below as it scrolled for several "_screens_."

   - `npm list -g`:
   - ![image.png](/.attachments/image-4a1f84be-10e6-422e-9135-0c8dd296ee33.png)
