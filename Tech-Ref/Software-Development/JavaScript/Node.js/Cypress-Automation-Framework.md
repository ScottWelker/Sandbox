[Home](/Slalom-LLC/Slalom-Consulting) | [Glossary](/Glossary) | [Tech Ref](/Tech-Ref) | [Software Development](/Tech-Ref/Software-Development) | [JavaScript](/Tech-Ref/Software-Development/JavaScript) | [Node.js](/Tech-Ref/Software-Development/JavaScript/Node.js)
**Disambiguation:** [Quality Engineering (QE)](/Tech-Ref/Software-Development/QE-\(Quality-Engineering\)).

[[_TOC_]]

---
# Introduction
***Cypress Automation Framework*** is a [JavaScript](/Tech-Ref/Software-Development/JavaScript) / [Node.js](/Tech-Ref/Software-Development/JavaScript/Node.js) test automation solution used for [web](/Tech-Ref/WWW-\(World-Wide-Web\)) automation. It enables teams to create web test automation scripts. This solution aims to enable frontend developers and test automation engineers to write [web](/Tech-Ref/WWW-\(World-Wide-Web\)) tests in the de-facto web language that is [JavaScript](/Tech-Ref/Software-Development/JavaScript) for web test automation.

Cypress comes bundled with its own browser, a test runner, and the [chai assertion library](NameMe).

## Rererence
1. [Docs.Cypress: Why Cypress](https://docs.cypress.io/guides/overview/why-cypress)
1. [Cypress vs. Selenium](https://www.perfecto.io/blog/cypress-vs-selenium-whats-right-cross-browser-testing-solution-you)

---
# Topics
1. [JavaScript](/Tech-Ref/Software-Development/JavaScript).
1. [Node.js](/Tech-Ref/Software-Development/JavaScript/Node.js).
1. [Quality Engineering (QE)](/Tech-Ref/Software-Development/QE-\(Quality-Engineering\)). 
1. [Server Buyer Website Resiliency](/Clients/Amazon/AWS-Marketplace/SBUX-and-Containers/Server-Buyer-Website/Server-Buyer-Website-Resiliency).
1. [Software Development](/Tech-Ref/Software-Development).
1. [Test Driven Development (TDD)](/Tech-Ref/Software-Development/QE-\(Quality-Engineering\)/TDD-\(Test-Driven-Development\)).
1. [Web Application](/Tech-Ref/WWW-\(World-Wide-Web\)/Web-Application).

---
# Components
- ![image.png](/.attachments/image-920134ee-eb3c-4ab6-8f55-2a6bbddc692b.png)

## Desktop Application

## Chai Assertion Library
- [Chai Assertion Library](/Tech-Ref/Software-Development/JavaScript/Chai-Assertion-Library).

## Command Line Interface (CLI)

### Global vs Local Commands
- Cypress commands can either be run from a specific directory containing a Cypress installation and code, or run from the global Cypress installation. Globally installing Cypress ensures that users can run Cypress from any directory in the operating system, while with a local Cypress installation, Cypress can only be accessed from the single directory that it has been installed in.

## Test Runner
- “...Cypress has a unique test runner that allows us to see commands as they execute. Additionally, it also shows the real-time run of the application under test.” — [ToolsQA: Cypress Test Runner](https://www.toolsqa.com/cypress/cypress-test-runner/#:~:text=Cypress%20has%20a%20unique%20test%20runner%20that%20allows%20us%20to%20see%20commands%20as%20they%20execute.%20Additionally%2C%20it%20also%20shows%20the%20real%2Dtime%20run%20of%20the%20application%20under%20test.)
- “Cypress runs tests interactively, allowing you to see commands as they execute while also viewing the Application or Component Under Test, and exploring its DOM.” — [Docs.Cypress: Test Runner](https://docs.cypress.io/guides/core-concepts/cypress-app#The-Test-Runner)
- 👍 For some teams the Test Runner is the means by which tests are developed, run, and debugged in “headed mode”, i.e. test development is not supported by an IDE like [IntelliJ IDEA](NameMe) or other. For example, [AWSMPServerSoftwareRenderingServiceCanaryTests Package](NameMe) is such a package.
- 👍 Note the The [Test Runner’s Preview Disappeared Tip](NameMe) below.

### Selector Playground
“The Selector Playground is an interactive feature of the Cypress Test Runner. The Selector Playground gives you the ability to determine unique selectors, check elements that match a specific selector, and check the elements that match a specific text in the Cypress application.”  — [packtpub.com: Understanding the Selector Playground](https://subscription.packtpub.com/book/web-development/9781839213854/11/ch11lvl1sec61/understanding-the-selector-playground)


### Debug Mode

---
# Cypress Use
## Selectors - cy.get()
Given the this [HTML](/Tech-Ref/WWW-\(World-Wide-Web\)/HTML-\(Hypertext-Markup-Language\)):

```html
<h1>Shapes:</h1>
<div class="square"></div>
<div id="circle"></div>
<div shape="triangle"></div>
```

| Selection Method | Example | Notes |
|:-|:-|:-|
| tag | `cy.get('h1')` | |
| class | `cy.get('.square')` | |
| id | `cy.get('#circle')` | |
| attribute | `cy.get('[shape="triangle"]')` | |

## Database and Server Commands
- The Cypress commands of `cy.exec()`, `cy.request()`, or `cy.task()`, provide a way to expose the database or the server. Having tests run in the browser creates a great experience for running tests, but it is a little cumbersome to plug in functionality that needs to run outside the browser.

## Control Origin Limitations
- Cypress only supports visiting URLs that are from the same origin in the same test. The control origin limitation means that for any particular test, you are not able to visit different URLs that do not belong to the same origin.

---
# Tips and Tricks

## Cypress 'integration' and 'plugins' Folders Missing
- :skull: It is not uncommon to encounter out-of-date information and tutorials referencing the deprecated `integration` and `plugins` folders, or files within them. These folder and their files are no longer installed with later Cypress versions. 
- [Integration and Plugin folders missing in cypress](https://stackoverflow.com/questions/72947095/integration-and-plugin-folders-missing-in-cypress)