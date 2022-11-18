[Home](/Slalom-LLC/Slalom-Consulting) | [Glossary](/Glossary) | [Tech Ref](/Tech-Ref) | [Software Development](/Tech-Ref/Software-Development) | [Java](/Tech-Ref/Software-Development/Java)

[[_TOC_]]

---
# Introduction
|:mask: Not using.|
|:-|
| [I (SWelker)](/Individuals/Scott-Welker) switched to [VS Code](/Tech-Ref/Microsoft/Visual-Studio/VS-Code-\(Visual-Studio-Code\)). [VS Code](/Tech-Ref/Microsoft/Visual-Studio/VS-Code-\(Visual-Studio-Code\)) more seamlessly allowed me to pickup an existing project and run with it. ***NetBeans*** required up-front decisions for which I was not yet prepared. |

"_NetBeans is an integrated development environment (IDE) for [Java](/Tech-Ref/Software-Development/Java)_"

## Reference
1. [Wikipedia: NetBeans](https://en.wikipedia.org/wiki/NetBeans)
1. [NetBeans: Introduction to GUI Building](https://netbeans.apache.org/kb/docs/java/gui-functionality.html)
1. [DZone: Gradle vs Maven (and Ant)](https://dzone.com/articles/gradle-vs-maven)

## Notes
1. Had to enable [Java SE (Standard Edition)](/Tech-Ref/Software-Development/Java/Java-Platform-Editions/Java-SE-\(Standard-Edition\)): `Tools` | `Plugins` | `Installed` (tab), `Java SE`, select (check) and press `Activate`.

---
# Topics
1. [Java](/Tech-Ref/Software-Development/Java).
1. [Java IDE](/Tech-Ref/Software-Development/Java/Java-IDE).

---
# Tips and Tricks

## New Project Category?
[I (SWelker)](/Individuals/Scott-Welker) was initially confused by NetBeans v12.4 `Categories:` choice. Gone is the simple and familiar `Java` option which implicitly chose, I believe, [Ant](/Tech-Ref/Apache-Software-Foundation/Apache-Ant). Now you need to think about the choice and pick one up-front ([Maven](/Tech-Ref/Apache-Software-Foundation/Apache-Maven), [Gradle](/Tech-Ref/Software-Development/DevOps-\(Development-and-IT-Operations\)/Gradle), or [Ant](/Tech-Ref/Apache-Software-Foundation/Apache-Ant)).
- ![image.png](/.attachments/image-fa9c6e5f-d590-4852-8ff5-bff1a61e8a50.png)

## Windows

### Java SE Development Kit (JDK) was not found...
#### JDK 8 or newer is required...
This proved to be due to [faulty JDK install](/Tech-Ref/Software-Development/Java#java-development-kit-(jdk)-with-jre), i.e. forgot to set `JAVA_HOME` environment variable.
- ![image.png](/.attachments/image-83315c14-7651-4551-a3b8-1da0a95f5222.png)

### JavaFX
1. :no_entry: Don't do this. See the [JavaFX](/Tech-Ref/Software-Development/Java/Java-Platform-Editions/JavaFX) page's introduction.
   - To create a new [JavaFX](/Tech-Ref/Software-Development/Java/Java-Platform-Editions/JavaFX) project from sources: `File` | `Net Project` | `Choose Project`, expand `Java with Ant`, select (categories) `JavaFX`, select (Projects) `JavaFX Project with Existing Sources`, press `Next`:
      - `In order to use this functionality, support for JavaFX 2 must be activated.`
         - Press `Download and Activate`
