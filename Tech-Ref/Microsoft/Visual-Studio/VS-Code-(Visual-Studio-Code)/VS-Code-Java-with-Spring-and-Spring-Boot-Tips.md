[Home](/Slalom-LLC/Slalom-Consulting) | [Glossary](/Glossary) | [Tech Ref](/Tech-Ref) | [Software Development](/Tech-Ref/Software-Development) | [Visual Studio Code](/Tech-Ref/Microsoft/Visual-Studio/VS-Code-\(Visual-Studio-Code\))

[[_TOC_]]

# Introduction
***Visual Studio Code*** tips and tricks for [Java](/Tech-Ref/Software-Development/Java) and [Spring Framework](/Tech-Ref/Software-Development/Java/Java-Platform-Editions/Jakarta-EE-\(Enterprise-Edition\)/Spring-Framework) / [Spring Boot](/Tech-Ref/Software-Development/Java/Java-Platform-Editions/Jakarta-EE-\(Enterprise-Edition\)/Spring-Framework/Spring-Boot).
- :+1: Developed during [Spring Boot RESTful MVC Web App from Scratch](/Tech-Ref/Software-Development/Java/Java-Platform-Editions/Jakarta-EE-\(Enterprise-Edition\)/Spring-Framework/Spring-Boot/App-from-Scratch,-Spring-Boot-RESTful-MVC-Web).

## Reference
1. [Getting Started with Java in VS Code](https://code.visualstudio.com/docs/java/java-tutorial)
1. [Spring Boot in Visual Studio Code](https://code.visualstudio.com/docs/java/java-spring-boot)

---
# Topics
1. [Java](/Tech-Ref/Software-Development/Java).
1. [Apache Maven](/Tech-Ref/Apache-Software-Foundation/Apache-Maven):
   - [Maven Wrapper (mvnw/mvnw.cmd)](/Tech-Ref/Apache-Software-Foundation/Apache-Maven/mvnw-\(Maven-Wrapper\)).
   - [Maven Plugin (Spring Boot)](/Tech-Ref/Software-Development/Java/Java-Platform-Editions/Jakarta-EE-\(Enterprise-Edition\)/Spring-Framework/Spring-Boot/Maven-Plugin-\(Spring-Boot\)).
1. [Spring Framework](/Tech-Ref/Software-Development/Java/Java-Platform-Editions/Jakarta-EE-\(Enterprise-Edition\)/Spring-Framework) / [Spring Boot](/Tech-Ref/Software-Development/Java/Java-Platform-Editions/Jakarta-EE-\(Enterprise-Edition\)/Spring-Framework/Spring-Boot):
   - [Spring Boot Tools](/Tech-Ref/Software-Development/Java/Java-Platform-Editions/Jakarta-EE-\(Enterprise-Edition\)/Spring-Framework/Spring-Boot/Spring-Boot-Tools).
   - [Spring Initializr](/Tech-Ref/Software-Development/Java/Java-Platform-Editions/Jakarta-EE-\(Enterprise-Edition\)/Spring-Framework/Spring-Boot/Spring-Initializr):
      - [Spring Initializr Java Support (VS Code)](/Tech-Ref/Microsoft/Visual-Studio/VS-Code-\(Visual-Studio-Code\)/Spring-Initializr-Java-Support).
1. [Visual Studio Code](/Tech-Ref/Microsoft/Visual-Studio/VS-Code-\(Visual-Studio-Code\)).
1. [Spring Boot RESTful MVC Web App from Scratch](/Tech-Ref/Software-Development/Java/Java-Platform-Editions/Jakarta-EE-\(Enterprise-Edition\)/Spring-Framework/Spring-Boot/App-from-Scratch,-Spring-Boot-RESTful-MVC-Web).

---
# Tips and Tricks

## Build (Ctl+Sft+b)

### No build task to run found. Configure Build task...
- ![image.png](/.attachments/image-4c48ebe0-da0c-4a38-9b19-b93fcd3e2aa6.png)
- Select `...Configure Build task...`, `Create task.json file from template`
   - ![image.png](/.attachments/image-8d0bbb7f-3740-4db8-961b-6888c2378bb4.png)
   - [I'm (SWelker)](/Individuals/Scott-Welker) using [Apache Maven](/Tech-Ref/Apache-Software-Foundation/Apache-Maven), see [Spring Boot RESTful MVC Web App from Scratch](/Tech-Ref/Software-Development/Java/Java-Platform-Editions/Jakarta-EE-\(Enterprise-Edition\)/Spring-Framework/Spring-Boot/App-from-Scratch,-Spring-Boot-RESTful-MVC-Web). Select `maven Executes common maven commands`:
      - ![image.png](/.attachments/image-788fa733-659d-4bf0-a355-9213c9ef1b59.png)
   - The `tasks.json` file is generated and opened. Save it.
      - :+1: Because this generated file is in the `.vscode/`, [.gitignore](/Tech-Ref/Software-Development/DevOps-\(Development-and-IT-Operations\)/Git) folder it won't be available for version control. 
      - ![image.png](/.attachments/image-db7c529e-5e3d-41e9-a1e5-07d7a4d208f3.png)
- Now you should be able to build successfully, `Ctl+Sft+b`.

## Couldn't start client Java Language Server
- [GitHub: Windows 10 Couldn't start client Java Language Server even with java_home](https://github.com/redhat-developer/vscode-java/issues/785)

The aforementioned article suggested the `georgewfraser.vscode-javac extension` extension is at fault and recommended uninstalling it then installing or re-installing `RedHat vscode-java` (pictured below). The uninstall was all [I (SWelker)](/Individuals/Scott-Welker) required.

### Uninstall georgewfraser.vscode-javac extension
   - ![image.png](/.attachments/image-80eaf05b-2b68-4b3d-a15c-be3e63cc121e.png =500x210)

### Install/Re-Install RedHat vscode-java
:+1: [I (SWelker)](/Individuals/Scott-Welker) did not have to do this. Just the uninstall.
   - ![image.png](/.attachments/image-6cf3d2d8-4c3f-418b-b03d-be34fc36068f.png =500x210)

## Spring Boot RESTful MVC Web App from Scratch
- [App from Scratch, Spring Boot RESTful MVC Web](/Tech-Ref/Software-Development/Java/Java-Platform-Editions/Jakarta-EE-\(Enterprise-Edition\)/Spring-Framework/Spring-Boot/App-from-Scratch,-Spring-Boot-RESTful-MVC-Web).
