[Home](/Slalom-LLC/Slalom-Consulting) | [Glossary](/Glossary) | [Tech Ref](/Tech-Ref) | [Software Development](/Tech-Ref/Software-Development) | [Java](/Tech-Ref/Software-Development/Java) | [Java Language](/Tech-Ref/Software-Development/Java/Java-Language)
**Disambiguation:** [NUnit](/Tech-Ref/Software-Development/NET-Framework/NUnit-Unit%2DTesting-Framework), [SUnit](https://en.wikipedia.org/wiki/SUnit), [xUnit](https://en.wikipedia.org/wiki/XUnit).

[[_TOC_]]

---
# Introduction
"_***JUnit*** is a unit testing framework for the [Java programming language](/Tech-Ref/Software-Development/Java/Java-Language). JUnit has been important in the development of [test-driven development](/Tech-Ref/Software-Development/QE-\(Quality-Engineering\)/TDD-\(Test-Driven-Development\)), and is one of a family of [unit testing](/Tech-Ref/Software-Development/QE-\(Quality-Engineering\)/Unit-Testing) frameworks which is collectively known as [xUnit](https://en.wikipedia.org/wiki/XUnit) that originated with [SUnit](https://en.wikipedia.org/wiki/SUnit)._"

## Reference
1. [Wikipedia: JUnit](https://en.wikipedia.org/wiki/JUnit)
1. [GitHub: JUnit Team](https://github.com/junit-team):
   - [JUnit5](https://github.com/junit-team/junit5#junit-5):
      - [JUnit5 r5.8.2](https://github.com/junit-team/junit5/releases/tag/r5.8.2)
      - [How do I install JUnit (Windows/*nix)?](https://junit.org/junit4/faq.html#started_1) 
         - [SWelker](/Individuals/Scott-Welker) Preference:
            - Create folder, `C:\Install\Java\jmock-junit5-2.12.0`, and extract the downloaded JUnit [JAR file](/Tech-Ref/Software-Development/Java/JAR-\(Java-ARchive\)) (`junit5-r5.8.2.zip`) contents to this new folder.
            - In [Windows](/Tech-Ref/Microsoft/Microsoft-Windows) `Control Panel` open `Edit the system environment variables`. 
               - In the resulting `System Properties` dialog, press the `Environment` button (bottom).
               - In the resulting `Environment Variables` dialog, `User variables for <user.name>`, press the `New` button:
                  - **Variable name:** `JUNIT_HOME`
                  - **Variable value:** `<path to your extracted JUnit JAR files>`
                     - E.g. `C:\Install\Java\jmock-junit5-2.12.0`.
                     - :+1: As a rule, [I (SWelker)](/Individuals/Scott-Welker) restart [Windows](/Tech-Ref/Microsoft/Microsoft-Windows) after such changes. In truth, I don't know whether this is still necessary, it's just a defensive measure with [Windows](/Tech-Ref/Microsoft/Microsoft-Windows) 
      - [JUnit5 User Guide:](https://junit.org/junit5/docs/current/user-guide/) 
         - **JUnit Platform:** Serves as a foundation for launching testing frameworks on the JVM. 
         - **JUnit Jupiter:** Is the combination of the new programming model and extension model for writing tests and extensions in JUnit 5. 
         - **JUnit Vintage:** Provides a TestEngine for running JUnit 3 and JUnit 4 based tests on the platform. It requires JUnit 4.12 or later to be present on the class path or module path.

---
# Asserts
|:warning: CAUTION!|
|:-|
| Incomplete draft! This is a work-in-progress.|
- [Junit Assert & AssertEquals](https://www.guru99.com/junit-assert.html).

## Assert
- [JUnit Assert methods](https://www.guru99.com/junit-assert.html#1)

## AssertEquals
- [Junit AssertEquals](https://www.guru99.com/junit-assert.html#8)

## Floating Point Assertions
- [Floating point assertions](https://www.guru99.com/junit-assert.html#9)

---
# Topics
1. [Java](/Tech-Ref/Software-Development/Java).
1. [Java Language](/Tech-Ref/Software-Development/Java/Java-Language).
1. [jMock](/Tech-Ref/Software-Development/Java/Java-Language/jMock).
1. [Test Driven Development (TDD)](/Tech-Ref/Software-Development/QE-\(Quality-Engineering\)/TDD-\(Test-Driven-Development\)).
1. [Unit Testing](/Tech-Ref/Software-Development/QE-\(Quality-Engineering\)/Unit-Testing).

