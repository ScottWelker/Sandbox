[Home](/Slalom-LLC/Slalom-Consulting) | [Glossary](/Glossary) | [Tech Ref](/Tech-Ref) | [CI/CD](/Tech-Ref/Software-Development/DevOps-\(Development-and-IT-Operations\)/CI-CD-\(Continuous-Integration-%2D-Continuous-Delivery\)) | [Apache](/Tech-Ref/Apache-Software-Foundation) | [Java](/Tech-Ref/Software-Development/Java)
**Disambiguation:** [Build Automation](/Tech-Ref/Software-Development/DevOps-\(Development-and-IT-Operations\)/Build-Automation), [Scripting](/Tech-Ref/Software-Development/Scripting).

[[_TOC_]]

---
# Introduction
"_The ***Apache Maven*** is a build automation tool used primarily for [Java](/Tech-Ref/Software-Development/Java) projects. Maven can also be used to build and manage projects written in [C#](/Tech-Ref/Software-Development/CSharp), Ruby, Scala, and other languages. The Maven project is hosted by the [Apache Software Foundation](/Tech-Ref/Apache-Software-Foundation), where it was formerly part of the [Jakarta](/Tech-Ref/Software-Development/Java/Java-Platform-Editions/Jakarta-EE-\(Enterprise-Edition\)) Project._"

"_Maven addresses two aspects of building software: how software is built, and its dependencies. Unlike earlier tools like [Apache Ant](/Tech-Ref/Apache-Software-Foundation/Apache-Ant), it uses conventions for the build procedure, and only exceptions need to be written down. An [XML](/Tech-Ref/Software-Development/Markup-Language/XML-\(eXtensible-Markup-Language\)) file describes the software project being built, its dependencies on other external modules and components, the build order, directories, and required plug-ins. It comes with pre-defined targets for performing certain well-defined tasks such as compilation of code and its packaging._"

## Reference
1. [Wikipedia: Apache Maven](https://en.wikipedia.org/wiki/Apache_Maven)
1. [Apache Maven Project](https://maven.apache.org/what-is-maven.html)
1. [Installing Apache Maven](https://maven.apache.org/install.html)

---
# Topics
1. [Apache Software Foundation](/Tech-Ref/Apache-Software-Foundation).
1. [CI/CD (Continuous Integration / Continuous Delivery)](/Tech-Ref/Software-Development/DevOps-\(Development-and-IT-Operations\)/CI-CD-\(Continuous-Integration-%2D-Continuous-Delivery\)).
1. [Java](/Tech-Ref/Software-Development/Java).
1. [Maven Central Repository](/Tech-Ref/Apache-Software-Foundation/Apache-Maven/Maven-Central-Repository).
1. [Maven Wrapper (mvnw/mvnw.cmd)](/Tech-Ref/Apache-Software-Foundation/Apache-Maven/mvnw-\(Maven-Wrapper\)).
1. [Project Object Model (POM)](/Tech-Ref/Apache-Software-Foundation/Apache-Maven/POM-\(Project-Object-Model\)).
1. [Spring Boot Maven Plugin](/Tech-Ref/Software-Development/Java/Java-Platform-Editions/Jakarta-EE-\(Enterprise-Edition\)/Spring-Framework/Spring-Boot/Maven-Plugin-\(Spring-Boot\)).

---
# Introduction to the Build Lifecycle
- [Introduction to the Build Lifecycle](https://maven.apache.org/guides/introduction/introduction-to-the-lifecycle.html)

## Paraphrased Introduction
Maven is based around the concept of a **build lifecycle**. There are three built-in build lifecycles: 
1. **default:** The default lifecycle handles your project deployment.
1. **clean:** The clean lifecycle handles project cleaning. 
1. **site:** The site lifecycle handles the creation of your project's web site.

Each of these build lifecycles is defined by a different list of **build phases**, wherein a build phase represents a stage in the lifecycle.

For example, the `default` lifecycle is comprised of the following phases (for a complete list of the lifecycle phases, refer to the [Lifecycle Reference](https://maven.apache.org/guides/introduction/introduction-to-the-lifecycle.html#Lifecycle_Reference)):

- `validate` - validate the project is correct and all necessary information is available
- `compile - compile the source code of the project
- `test` - test the compiled source code using a suitable [unit testing](/Tech-Ref/Software-Development/QE-\(Quality-Engineering\)/Unit-Testing) framework. These tests should not require the code be packaged or deployed
- `package` - take the compiled code and package it in its distributable format, such as a JAR.
- `verify` - run any checks on results of integration tests to ensure quality criteria are met
- `install` - install the package into the local repository, for use as a dependency in other projects locally
- `deploy` - done in the build environment, copies the final package to the remote repository for sharing with other developers and projects.

These lifecycle phases (plus other lifecycle phases not shown here) are executed sequentially to complete the default lifecycle. Given the lifecycle phases above, this means that when the default lifecycle is used, Maven will first validate the project, then will try to compile the sources, run those against the tests, package the binaries (e.g. [jar](/Tech-Ref/Software-Development/Java/JAR-\(Java-ARchive\))), run integration tests against that package, verify the integration tests, install the verified package to the local repository, then deploy the installed package to a remote repository.

## A Build Phase is Made Up of Plugin Goals
However, even though a **build phase** is responsible for a specific step in the **build lifecycle**, the manner in which it carries out those responsibilities may vary. And this is done by declaring the **plugin goals** bound to those build phases.

A **plugin goal** represents a specific task (finer than a build phase) which contributes to the building and managing of a project. It may be bound to zero or more **build phases**. A goal not bound to any build phase could be executed outside of the build lifecycle by direct invocation. The order of execution depends on the order in which the goal(s) and the build phase(s) are invoked.
