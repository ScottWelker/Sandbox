[Home](/Slalom-LLC/Slalom-Consulting) | [Glossary](/Glossary) | [Tech Ref](/Tech-Ref) | [Software Development](/Tech-Ref/Software-Development) | [Java](/Tech-Ref/Software-Development/Java) | [Java Language](/Tech-Ref/Software-Development/Java/Java-Language)
**Disambiguation:** [Namespace](/Tech-Ref/Software-Development/Namespace).

[[_TOC_]]

---
# Introduction
***Package*** in the [Java Language](/Tech-Ref/Software-Development/Java/Java-Language) is a   Namespace. A package in [Java](/Tech-Ref/Software-Development/Java) is used to group related classes. We use packages to avoid name conflicts, and to write a better maintainable code. 

## Reference
1. [Docs.Oracle: What Is a Package?](https://docs.oracle.com/javase/tutorial/java/concepts/package.html)
   - [Naming a Package](https://docs.oracle.com/javase/tutorial/java/package/namingpkgs.html)
1. [w3schools: Java Packages](https://www.w3schools.com/java/java_packages.asp)
1. [JavaTpoint: Package](https://www.javatpoint.com/package)

---
# Topics
## From Other Wiki Pages
1. [Java](/Tech-Ref/Software-Development/Java).
1. [Java Language](/Tech-Ref/Software-Development/Java/Java-Language).
1. [Namespace](/Tech-Ref/Software-Development/Namespace).

## Naming Conventions
Package names are written in all lower case to avoid conflict with the names of classes or interfaces.

Companies use their reversed Internet domain name to begin their package names—for example, com.example.mypackage for a package named mypackage created by a programmer at example.com.

Name collisions that occur within a single company need to be handled by convention within that company, perhaps by including the region or the project name after the company name (for example, com.example.region.mypackage).

Packages in the Java language itself begin with java. or javax.

In some cases, the internet domain name may not be a valid package name. This can occur if the domain name contains a hyphen or other special character, if the package name begins with a digit or other character that is illegal to use as the beginning of a Java name, or if the package name contains a reserved Java keyword, such as "int". In this event, the suggested convention is to add an underscore. 
