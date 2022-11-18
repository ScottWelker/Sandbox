[Home](/Slalom-LLC/Slalom-Consulting) | [Glossary](/Glossary) | [Tech Ref](/Tech-Ref) | [Software Development](/Tech-Ref/Software-Development) | [Jakarta EE](/Tech-Ref/Software-Development/Java/Java-Platform-Editions/Jakarta-EE-\(Enterprise-Edition\)) | [Spring Framework](/Tech-Ref/Software-Development/Java/Java-Platform-Editions/Jakarta-EE-\(Enterprise-Edition\)/Spring-Framework) | [Spring Boot](/Tech-Ref/Software-Development/Java/Java-Platform-Editions/Jakarta-EE-\(Enterprise-Edition\)/Spring-Framework/Spring-Boot)

[[_TOC_]]

---
# Introduction
[My (SWelker)](/Individuals/Scott-Welker) notes, working through [Building an Application with Spring Boot](https://spring.io/guides/gs/spring-boot/).

[I (SWelker)](/Individuals/Scott-Welker) opted for a [RESTful](/Tech-Ref/Software-Development/REST-\(Representational-State-Transfer\)), [MVC (Model View Controller)](/Tech-Ref/Software-Development/Software-Design-Pattern/MVC-\(Model-View-Controller\)), [Web Application](/Tech-Ref/WWW-\(World-Wide-Web\)/Web-Application).

## Reference
1. [Building an Application with Spring Boot](https://spring.io/guides/gs/spring-boot/).

## Install, Configure, and Dragons
### Prerequisites
These are the things [my (SWelker)](/Individuals/Scott-Welker) [Windows](/Tech-Ref/Microsoft/Microsoft-Windows) system lacked, or that I recall installing. Your mileage may vary. Because of prior work in [React](/Tech-Ref/Software-Development/JavaScript/React), I might have installed some things not listed here.

   1. [JDK (Java Development Kit)](/Tech-Ref/Software-Development/Java/JDK-\(Java-Development-Kit\)).
      - :+1: Includes the [JRE (Java Runtime Environment)](/Tech-Ref/Software-Development/Java/JRE-\(Java-Runtime-Environment\)) / [JVM (Java Virtual Machine)](/Tech-Ref/Software-Development/Java/JRE-\(Java-Runtime-Environment\)/JVM-\(Java-Virtual-Machine\)).
   1. [Visual Studio Code](/Tech-Ref/Microsoft/Visual-Studio/VS-Code-\(Visual-Studio-Code\)).
   1. [Git](/Tech-Ref/Software-Development/DevOps-\(Development-and-IT-Operations\)/Git).
      - I am also using my [Azure DevOps Services](/Tech-Ref/Microsoft/Microsoft-Azure/ADO-\(Azure-DevOps\)/Azure-DevOps-Services) but it isn't strictly necessary.
   1. [Apache Maven](/Tech-Ref/Apache-Software-Foundation/Apache-Maven).

### Project Setup
When you advance to the point of having a [VS Code](/Tech-Ref/Microsoft/Visual-Studio/VS-Code-\(Visual-Studio-Code\)) project, you'll need to:
1. Configure the [VS Code](/Tech-Ref/Microsoft/Visual-Studio/VS-Code-\(Visual-Studio-Code\)) '_build task_', see [Java with Spring and Spring Boot Tips, Build (Ctl+Sft+b)](/Tech-Ref/Microsoft/Visual-Studio/VS-Code-\(Visual-Studio-Code\)/VS-Code-Java-with-Spring-and-Spring-Boot-Tips#build-(ctl%2Bsft%2Bb)).
1. Had to configure the [VS Code](/Tech-Ref/Microsoft/Visual-Studio/VS-Code-\(Visual-Studio-Code\)) project's debugger. See [Debugger for Java, Tips and Tricks, Running and Debugging Java](/Tech-Ref/Microsoft/Visual-Studio/VS-Code-\(Visual-Studio-Code\)/Debugger-for-Java#running-and-debugging-java).

### Here be Dragons!
Here are some gotchas [I (SWelker)](/Individuals/Scott-Welker) encountered:
1. Pay careful attention to your chosen [Spring Initializr](/Tech-Ref/Software-Development/Java/Java-Platform-Editions/Jakarta-EE-\(Enterprise-Edition\)/Spring-Framework/Spring-Boot/Spring-Initializr) options. If you chose options that don't match your environment you can waste a bunch of time chasing down build/compile failures.
1. The long-lived [Windows](/Tech-Ref/Microsoft/Microsoft-Windows) zip failure "_[File path too long](https://community.spiceworks.com/topic/174820-cannot-unzip-file-file-path-too-long)_" still plagues us. You may or may not encounter this.
1. [VS Code](/Tech-Ref/Microsoft/Visual-Studio/VS-Code-\(Visual-Studio-Code\)) extensions can cause problems. See see [Java with Spring and Spring Boot Tips, Couldn't start client Java Language Server](/Tech-Ref/Microsoft/Visual-Studio/VS-Code-\(Visual-Studio-Code\)/VS-Code-Java-with-Spring-and-Spring-Boot-Tips#couldn%27t-start-client-java-language-server).
1. The environment can be flakey. See [Failed to execute goal...](#failed-to-execute-goal...)

---
# Topics
1. [Java](/Tech-Ref/Software-Development/Java).
1. [Apache Maven](/Tech-Ref/Apache-Software-Foundation/Apache-Maven).
1. [Maven Central Repository](/Tech-Ref/Apache-Software-Foundation/Apache-Maven/Maven-Central-Repository).
1. [Model View Controller (MVC)](/Tech-Ref/Software-Development/Software-Design-Pattern/MVC-\(Model-View-Controller\)).
1. [REST (Representational State Transfer)](/Tech-Ref/Software-Development/REST-\(Representational-State-Transfer\)).
1. [Spring Framework](/Tech-Ref/Software-Development/Java/Java-Platform-Editions/Jakarta-EE-\(Enterprise-Edition\)/Spring-Framework).
1. [Spring Boot](/Tech-Ref/Software-Development/Java/Java-Platform-Editions/Jakarta-EE-\(Enterprise-Edition\)/Spring-Framework/Spring-Boot).
1. [Visual Studio Code](/Tech-Ref/Microsoft/Visual-Studio/VS-Code-\(Visual-Studio-Code\)).
1. [Web Application](/Tech-Ref/WWW-\(World-Wide-Web\)/Web-Application).

---
# TrialApp
Developing [my (SWelker)](/Individuals/Scott-Welker) trial application (TrialApp) following "_[Building an Application with Spring Boot](https://spring.io/guides/gs/spring-boot/)_".

## Start from scratch

### Starting with Spring Initializr
1. [Starting with Spring Initializr](https://spring.io/guides/gs/spring-boot/#scratch).
   - [spring initializr](https://start.spring.io/)
   - :+1: To enlarge, open the image below in a new tab/window.
   - ![image.png](/.attachments/image-10aeeeb3-e1e4-478d-81a4-77f62a3f0f34.png =500x300)
   - :+1: [I (SWelker)](/Individuals/Scott-Welker) used this reference in setting ***Project Metadata***: [Spring: Getting Started, Advanced Options](https://docs.spring.io/initializr/docs/0.4.x/reference/htmlsingle/#getting-started-advanced-options).
1. The initializer provided/generated `TrialApp.zip` which I downloaded and unziped the full `TrialApp` to my `C:\SourceCode\com.Slalom.rsw` folder. I then opened the 
   - :+1: Had to work-around the well-known [Windows](/Tech-Ref/Microsoft/Microsoft-Windows) zip `File path too long" issue, noted here: https://community.spiceworks.com/topic/174820-cannot-unzip-file-file-path-too-long.
1. Opened the `TrialApp` folder in [Visual Studio Code](/Tech-Ref/Microsoft/Visual-Studio/VS-Code-\(Visual-Studio-Code\)) and it imported the [Java](/Tech-Ref/Software-Development/Java) project for me:
   - ![image.png](/.attachments/image-d738ffbe-7287-4e2b-8b9a-7f51ef42250a.png)
1. Now the project should build.
   - :+1: [Java with Spring and Spring Boot Tips, Build](/Tech-Ref/Microsoft/Visual-Studio/VS-Code-\(Visual-Studio-Code\)/VS-Code-Java-with-Spring-and-Spring-Boot-Tips#build-(ctl%2Bsft%2Bb)).
1. [Committed and pushed](/Tech-Ref/Software-Development/DevOps-\(Development-and-IT-Operations\)/Git) this code before moving on to [Create a Simple Web Application](#Create-a-Simple-Web-Application)

### Lessons Learned \#1
1. [Spring Initializr](/Tech-Ref/Software-Development/Java/Java-Platform-Editions/Jakarta-EE-\(Enterprise-Edition\)/Spring-Framework/Spring-Boot/Spring-Initializr) saves a bunch of setup work.
1. Pay careful attention to your chosen [Spring Initializr](/Tech-Ref/Software-Development/Java/Java-Platform-Editions/Jakarta-EE-\(Enterprise-Edition\)/Spring-Framework/Spring-Boot/Spring-Initializr) options. If you chose options that don't match your environment you can waste a bunch of time chasing down build/compile failures.
1. The long-lived [Windows](/Tech-Ref/Microsoft/Microsoft-Windows) zip failure "_[File path too long](https://community.spiceworks.com/topic/174820-cannot-unzip-file-file-path-too-long)_" still plagues us.
1. Had to configure the [VS Code](/Tech-Ref/Microsoft/Visual-Studio/VS-Code-\(Visual-Studio-Code\)) '_build task_', see [Java with Spring and Spring Boot Tips, Build (Ctl+Sft+b)](/Tech-Ref/Microsoft/Visual-Studio/VS-Code-\(Visual-Studio-Code\)/VS-Code-Java-with-Spring-and-Spring-Boot-Tips#build-(ctl%2Bsft%2Bb)).
1. [VS Code](/Tech-Ref/Microsoft/Visual-Studio/VS-Code-\(Visual-Studio-Code\)) extensions can cause problems. See see [Java with Spring and Spring Boot Tips, Couldn't start client Java Language Server](/Tech-Ref/Microsoft/Visual-Studio/VS-Code-\(Visual-Studio-Code\)/VS-Code-Java-with-Spring-and-Spring-Boot-Tips#couldn%27t-start-client-java-language-server).

## Create a Simple Web Application
- [Create a Simple Web Application](https://spring.io/guides/gs/spring-boot/#initial).

### Add Controller (MVC/Java)
- Per the instructions I added a [Java class](/Tech-Ref/Software-Development/Java) to `TrialApp`, `TrialAppController` with this code. It just worked :)
   - [Web Browser](/Tech-Ref/WWW-\(World-Wide-Web\)/Web-Browser), `localhost:800`
      - ![image.png](/.attachments/image-3d569475-30e7-4349-8a59-fda0ed70d082.png)

### Lessons Learned \#2
1. It was trivial to add the [MVC controller](/Tech-Ref/Software-Development/Software-Design-Pattern/MVC-\(Model-View-Controller\)) and it just worked.

```Java
package com.example.springboot;

import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.RestController;

@RestController
public class HelloController {

	@GetMapping("/")
	public String index() {
		return "Greetings from Spring Boot TrialApp!";
	}

}
```

## Create an Application class
- [Create an Application class](https://spring.io/guides/gs/spring-boot/#_create_an_application_class)

Following these instructions I encountered two issues:
1. Build-time error "[Failed to execute goal...](#failed-to-execute-goal...)"
1. The debugger did not seem to be working correctly. Specifically I was [unable to locate a call stack](#where-is-the-debugger%27s-call-stack%3F).

### Failed to execute goal...
[I (SWelker)](/Individuals/Scott-Welker) encountered this mysterious error after fleshing out my application, as per the instructions.
- `Failed to execute goal org.springframework.boot:spring-boot-maven-plugin:2.5.4:run (default-cli) on project`
- **Resolution:**
   - Ultimately it seems you **MUST** run `mvn clean` from time-to-time. The problem is recurring. It is unclear what the source of the error really is. [I (SWelker)](/Individuals/Scott-Welker) swerved into the following article to get the idea of running `mvn clean`:
      - [StackOverflow: How to run Spring-boot-sample project from GIT?](https://stackoverflow.com/q/31741594/418950).
         - Before resolution via `mvn clean` something suggested trying the following. Neither fully resolved or revealed the root cause:
            1. Running [Maven](/Tech-Ref/Apache-Software-Foundation/Apache-Maven) with preview enabled, `$MAVEN_OPTS="--enable-preview"`.
               - :+1: I've kept this option in place.
            1. Running [Maven](/Tech-Ref/Apache-Software-Foundation/Apache-Maven) in full-debug mode, `./mvnw -X spring-boot:run`.

### Where is the Debugger's Call Stack?
After a bit of digging [I (SWelker)](/Individuals/Scott-Welker) determined that my project required some configuration to fully enable the debugger. See [Debugger for Java, Tips and Tricks, Running and Debugging Java](/Tech-Ref/Microsoft/Visual-Studio/VS-Code-\(Visual-Studio-Code\)/Debugger-for-Java#running-and-debugging-java).

### Lessons Learned \#3
1. The environment can be flakey. See [Failed to execute goal...](#failed-to-execute-goal...)
1. Had to configure the [VS Code](/Tech-Ref/Microsoft/Visual-Studio/VS-Code-\(Visual-Studio-Code\)) project's debugger. See [Debugger for Java, Tips and Tricks, Running and Debugging Java](/Tech-Ref/Microsoft/Visual-Studio/VS-Code-\(Visual-Studio-Code\)/Debugger-for-Java#running-and-debugging-java).
1. [Spring Boot Annotations (AKA Decorations or Tags)](/Tech-Ref/Software-Development/Java/Java-Platform-Editions/Jakarta-EE-\(Enterprise-Edition\)/Spring-Framework/Spring-Boot/Annotations) are powerful and voluminous but their names don't always reflect all that they do.
   - In (at least) [VS Code](/Tech-Ref/Microsoft/Visual-Studio/VS-Code-\(Visual-Studio-Code\)) mouse-over help pops up a large dialog with a good `Overview`.
1. :white_large_square: [I (SWelker)](/Individuals/Scott-Welker) need to study the [Spring Boot CommandLineRunner](/Tech-Ref/Software-Development/Java/Java-Platform-Editions/Jakarta-EE-\(Enterprise-Edition\)/Spring-Framework/Spring-Boot/CommandLineRunner) / [Functional Interfaces In Java](https://www.geeksforgeeks.org/functional-interfaces-java/).
1. This trivial application ends up with 133 [Spring Beans](/Tech-Ref/Software-Development/Java/Java-Platform-Editions/Jakarta-EE-\(Enterprise-Edition\)/Spring-Framework/Spring-Bean) added by the [Spring Framework](/Tech-Ref/Software-Development/Java/Java-Platform-Editions/Jakarta-EE-\(Enterprise-Edition\)/Spring-Framework).
1. [Maven Wrapper (mvnw/mvnw.cmd)](/Tech-Ref/Apache-Software-Foundation/Apache-Maven/mvnw-\(Maven-Wrapper\)) is a handy project-specific wrapper that facilitates sharing a project with others.
1. The [Maven Plugin 'Goal'](/Tech-Ref/Software-Development/Java/Java-Platform-Editions/Jakarta-EE-\(Enterprise-Edition\)/Spring-Framework/Spring-Boot/Maven-Plugin-\(Spring-Boot\)#spring-boot-plugin-maven-%27goals%27), `spring-boot:run`, can be used with the [Maven Wrapper (mvnw)](/Tech-Ref/Apache-Software-Foundation/Apache-Maven/mvnw-\(Maven-Wrapper\)) to execute your application from the [terminal/command line](/Tech-Ref/CLI-\(Command-Line-Interface\)), e.g. `./mvnw spring-boot:run`.
1. [cURL](/Tech-Ref/Software-Development/cURL-\(Client-URL\)) may be used to exercise the [Spring Boot](/Tech-Ref/Software-Development/Java/Java-Platform-Editions/Jakarta-EE-\(Enterprise-Edition\)/Spring-Framework/Spring-Boot) [Web Application](/Tech-Ref/WWW-\(World-Wide-Web\)/Web-Application) from the [terminal/command prompt](/Tech-Ref/CLI-\(Command-Line-Interface\)), e.g.:
   - `curl localhost:8080`

## Add Unit Tests
- [Add Unit Tests](https://spring.io/guides/gs/spring-boot/#_add_unit_tests)

### Lessons Learned \#4
1. The [Maven](/Tech-Ref/Apache-Software-Foundation/Apache-Maven) `pom.xml` config was already done, presumably by the [Spring Initializr](/Tech-Ref/Software-Development/Java/Java-Platform-Editions/Jakarta-EE-\(Enterprise-Edition\)/Spring-Framework/Spring-Boot/Spring-Initializr).
1. A [Java Package](/Tech-Ref/Software-Development/Java/Java-Language/Package-\(Java\)) is (mostly) just a [Namespace](/Tech-Ref/Software-Development/Namespace). This caused me some confusion as mine differs from the examples because I used a name that made sense to me but that resulted in differing [namespaces](/Tech-Ref/Software-Development/Namespace). Confusingly (at first) [VS Code](/Tech-Ref/Microsoft/Visual-Studio/VS-Code-\(Visual-Studio-Code\)) kept suggesting I move class files to match the [namespaces](/Tech-Ref/Software-Development/Java/Java-Language/Package-\(Java\)).
1. :+1: Don't make stupid mistakes! [I (SWelker)](/Individuals/Scott-Welker) forgot I was developing in a branch. Normally I don't do this with a test/trial app. Ordinarily I'd just work in `master`. For some reason I followed the example's directions and instead worked in a branch. During the aforementioned "[Package (Java)](/Tech-Ref/Software-Development/Java/Java-Language/Package-\(Java\)) / [Namespace](/Tech-Ref/Software-Development/Namespace) confusion, I reset my branch to `master`, neglecting to recall that my changes are all in a branch, `SpringBootRESTfulMVCWebAppFromScratch`. That just created more confusion. Doh! :confounded:
1. :+1: [I (SWelker)](/Individuals/Scott-Welker) want the [VS Code Javadoc Tools](/Tech-Ref/Microsoft/Visual-Studio/VS-Code-\(Visual-Studio-Code\)/Javadoc-Tools-for-Visual-Studio-Code) extension! I am an advocate of such tools and code for it habitually.
   - :warning: **Warning!** Seems a bit flakey - or I am not using it correctly. Specifically:
      1. :white_large_square: I get an error attempting to run command `Javadoc Tools: Export JavaDoc`. See [Javadoc Tools for Visual Studio Code, Tips and Tricks, Unexpected Token '-public' in expression or statement.](/Tech-Ref/Microsoft/Visual-Studio/VS-Code-\(Visual-Studio-Code\)/Javadoc-Tools-for-Visual-Studio-Code#unexpected-token-%27-public%27-in-expression-or-statement.).
         -  :skull: **09/07/2021 [SWelker](/Individuals/Scott-Welker):** Abandoned attempts to address this - for now. It's an unwelcome distraction.
      1. Initially, I could not get the `Javadoc Tools: Generate Javadoc Comments for Open File` command to work (command palette, `Ctrl`+`Shift`+`P`). Later (after a restart) it just seemed to work - mostly. For a particular file containing a public class comprised of just one public static member, it continues to fail to generate the JavaDocs comment stub.
1. [Test Runner for Java](/Tech-Ref/Microsoft/Visual-Studio/VS-Code-\(Visual-Studio-Code\)/Test-Runner-for-Java) is an intuitive and useful extension for [JUnit](/Tech-Ref/Software-Development/Java/Java-Language/JUnit-Unit%2DTesting-Framework) tests.
1. :white_large_square: Integration tests seem worthy of further study. I skipped over them for now.

## Add Production-grade Services
- [Add Production-grade Services](https://spring.io/guides/gs/spring-boot/#_add_production_grade_services)
