[Home](/Slalom-LLC/Slalom-Consulting) | [Glossary](/Glossary) | [Tech Ref](/Tech-Ref) | [CI/CD](/Tech-Ref/Software-Development/DevOps-\(Development-and-IT-Operations\)/CI-CD-\(Continuous-Integration-%2D-Continuous-Delivery\)) | [Java](/Tech-Ref/Software-Development/Java) | [Maven](/Tech-Ref/Apache-Software-Foundation/Apache-Maven)

[[_TOC_]]

---
# Introduction
"_***Project Object Model (POM)*** is the fundamental unit of work in [Maven](/Tech-Ref/Apache-Software-Foundation/Apache-Maven). It is an [XML](/Tech-Ref/Software-Development/Markup-Language/XML-\(eXtensible-Markup-Language\)) file that contains information about the project and configuration details used by [Maven](/Tech-Ref/Apache-Software-Foundation/Apache-Maven) to build the project. It contains default values for most projects. Examples for this is the build directory, which is target; the source directory, which is `src/main/java`; the test source directory, which is `src/test/java`; and so on. When executing a **task** or **goal**, [Maven](/Tech-Ref/Apache-Software-Foundation/Apache-Maven) looks for the POM in the current directory. It reads the POM, gets the needed configuration information, then executes the **goal**._"

## Reference
1. [Introduction to the POM, What is a POM?](https://maven.apache.org/guides/introduction/introduction-to-the-pom.html#What_is_a_POM)

---
# Topics
1. [Java](/Tech-Ref/Software-Development/Java).
1. [Apache Maven](/Tech-Ref/Apache-Software-Foundation/Apache-Maven).
1. [Spring Boot](/Tech-Ref/Software-Development/Java/Java-Platform-Editions/Jakarta-EE-\(Enterprise-Edition\)/Spring-Framework/Spring-Boot).
1. [Spring Boot Maven Plugin](/Tech-Ref/Software-Development/Java/Java-Platform-Editions/Jakarta-EE-\(Enterprise-Edition\)/Spring-Framework/Spring-Boot/Maven-Plugin-\(Spring-Boot\)).

---
# Tips and Tricks

## Spring Boot RESTful MVC Web App from Scratch
- [Spring Boot RESTful MVC Web App from Scratch](/Tech-Ref/Software-Development/Java/Java-Platform-Editions/Jakarta-EE-\(Enterprise-Edition\)/Spring-Framework/Spring-Boot/App-from-Scratch,-Spring-Boot-RESTful-MVC-Web).

---
# Tips and Tricks

## Vulnerability / Dependency Analytics Report (VS Code)
In [VS Code](/Tech-Ref/Microsoft/Visual-Studio/VS-Code-\(Visual-Studio-Code\)) you can access a `Vulnerability Report`. To do so:
1. Open your _Project Object Model (POM)_ file, `pom.xml`.
1. Notice the pie chart icon that appears on the upper right-hand side of the screen. Point your mouse at the pie chart and click on it. 
1. `Dependency Analytics` executes. Be patient, it may be a bit slow to respond. Eventually it generates the `Dependency Analytics Report` list vulnerabilities found, if any.
- ![image.png](/.attachments/image-3afc517f-4be0-44ab-9c22-ac4afc68bf2d.png)
