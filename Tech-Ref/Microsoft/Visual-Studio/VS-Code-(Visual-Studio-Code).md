[Home](/Slalom-LLC/Slalom-Consulting) | [Glossary](/Glossary) | [Tech Ref](/Tech-Ref) | [Software Development](/Tech-Ref/Software-Development) | [Visual Studio](/Tech-Ref/Microsoft/Visual-Studio)
**Disambiguation:** [Visual Studio](/Tech-Ref/Microsoft/Visual-Studio).

[[_TOC_]]

# Introduction
"_***Visual Studio Code*** or ***VS Code*** is a source-code editor made by Microsoft for [Windows](/Tech-Ref/Microsoft/Microsoft-Windows), [Linux](/Tech-Ref/Linux) and [macOS](/Tech-Ref/Apple-Inc/Mac-\(Macintosh\)/macOS). Features include support for debugging, syntax highlighting, intelligent code completion, snippets, [code refactoring](/Tech-Ref/Software-Development/Code-Refactoring), and embedded [Git](/Tech-Ref/Software-Development/DevOps-\(Development-and-IT-Operations\)/Git). Users can change the theme, keyboard shortcuts, preferences, and install extensions that add additional functionality._"

   - :warning: <mark>**VS Code** supports building and debugging .NET Framework projects but its support is very limited.</mark> Use [Visual Studio](/Tech-Ref/Microsoft/Visual-Studio) instead.
      - See [StackOverflow: Visual Studio Code for .Net Framework](https://stackoverflow.com/a/49824895/418950)
      - See [Working with C# (in VS Code)](https://code.visualstudio.com/docs/languages/csharp)

## Reference
1. [Wikipedia: Visual Studio Code](https://en.wikipedia.org/wiki/Visual_Studio_Code)
1. [VisualStudio: Why VS Code?](https://code.visualstudio.com/docs/editor/whyvscode)

## Reference (Java)
1. [Java build tools in VS Code](https://code.visualstudio.com/docs/java/java-build)
1. [Visual Studio Code for Java: The Ultimate Guide 2019](https://medium.com/@brunoborges/visual-studio-code-for-java-the-ultimate-guide-2019-8de7d2b59902)

---
# Topics
1. [Git](/Tech-Ref/Software-Development/DevOps-\(Development-and-IT-Operations\)/Git).
1. [Java IDE](/Tech-Ref/Software-Development/Java/Java-IDE).
1. [JavaScript](/Tech-Ref/Software-Development/JavaScript).
1. [Linux](/Tech-Ref/Linux).
1. [macOS](/Tech-Ref/Apple-Inc/Mac-\(Macintosh\)/macOS).
1. [Spring Boot Tools](/Tech-Ref/Software-Development/Java/Java-Platform-Editions/Jakarta-EE-\(Enterprise-Edition\)/Spring-Framework/Spring-Boot/Spring-Boot-Tools).
1. [Spring Initializr](/Tech-Ref/Software-Development/Java/Java-Platform-Editions/Jakarta-EE-\(Enterprise-Edition\)/Spring-Framework/Spring-Boot/Spring-Initializr).
   - [Spring Initializr Java Support](/Tech-Ref/Microsoft/Visual-Studio/VS-Code-\(Visual-Studio-Code\)/Spring-Initializr-Java-Support).
1. [TypeScript](/Tech-Ref/Software-Development/TypeScript).
1. [Visual Studio](/Tech-Ref/Microsoft/Visual-Studio).
1. [Windows](/Tech-Ref/Microsoft/Microsoft-Windows).

---
# Concepts

## Workspace
- [What is a VS Code "Workspace"](https://code.visualstudio.com/docs/editor/workspaces)
   - A Visual Studio Code "workspace" is the collection of one or more folders that are opened in a VS Code window (instance). In most cases, you will have a single folder opened as the workspace but, depending on your development workflow, you can include more than one folder, using an advanced configuration called [Multi-root workspaces](https://code.visualstudio.com/docs/editor/workspaces#_multiroot-workspaces).

## User and Workspace Settings
- [Code: User and Workspace Settings](https://code.visualstudio.com/docs/getstarted/settings)

### Settings Editor
- You use the _Settings editor_ to review and change VS Code settings.
   - On Windows/Linux: `File` > `Preferences` > `Settings`

#### User Settings 
- _User Settings_ are settings that apply globally to any instance of VS Code you open. These are your personal settings for customizing VS Code.

#### Workspace Settings
- _Workspace Settings_ settings are stored inside your workspace and only apply when the workspace is opened. These are settings specific to the project you're working on.

---
# Extensions
These are the relatively few extensions about which [I've (SWelker)](/Individuals/Scott-Welker) taken some notes.

## ANSI Colors
- [ANSI Colors (VS Code)](/Tech-Ref/Microsoft/Visual-Studio/VS-Code-\(Visual-Studio-Code\)/ANSI-Colors-\(VS-Code\))

## Debugger for Java
- [Debugger for Java](/Tech-Ref/Microsoft/Visual-Studio/VS-Code-\(Visual-Studio-Code\)/Debugger-for-Java).

## Javadoc Tools
- [Javadoc Tools for Visual Studio Code](/Tech-Ref/Microsoft/Visual-Studio/VS-Code-\(Visual-Studio-Code\)/Javadoc-Tools-for-Visual-Studio-Code).

## Java Language Support (georgewfraser.vscode-javac extension)
- :no_entry: As noted  [here (Java with Spring and Spring Boot Tips)](/Tech-Ref/Microsoft/Visual-Studio/VS-Code-\(Visual-Studio-Code\)/VS-Code-Java-with-Spring-and-Spring-Boot-Tips#uninstall-georgewfraser.vscode-javac-extension), I had to remove this extension.

## Language Support for Java (RedHat vscode-java)
- As noted  [here (Java with Spring and Spring Boot Tips)](/Tech-Ref/Microsoft/Visual-Studio/VS-Code-\(Visual-Studio-Code\)/VS-Code-Java-with-Spring-and-Spring-Boot-Tips#install%2Fre-install-redhat-vscode-java), this replaced the ***Java Language Support (georgewfraser.vscode-javac extension)*** extension.

---
# Tips and Tricks

## Change File Language
- [Changing the language for the selected file](https://code.visualstudio.com/docs/languages/overview#_changing-the-language-for-the-selected-file)

   - ![image.png](/.attachments/image-5b628db9-c32e-47fb-bb35-198228cc967c.png)

## Code Actions
"_***Code Actions*** is a Visual Studio Code feature providing the user with possible corrective actions right next to an error or warning. If actions are available, a :bulb: light bulb appears next to the error or warning. When the user clicks the light bulb (or presses Ctrl+.), a list of available code actions is presented._"

## Command Palette
"_The most important key combination to know is `Ctrl`+`Shift`+`P`, which brings up the Command Palette. From here, you have access to all of the functionality of VS Code, including keyboard shortcuts for the most common operations._
- [VS Code Command Palette](https://code.visualstudio.com/docs/getstarted/userinterface#_command-palette)

|:+1: Tips | Description |
|:-|:-|
| `?` | To get a list of available commands you can execute from here. |
| `Ctrl`+`P` | Navigate to any file or symbol by typing its name. |
| `Ctrl`+`Tab` | Cycle through the last set of files opened. |
| `Ctrl`+`Shift`+`P` | Editor commands. |
| `Ctrl`+`Shift`+`O` | Navigate to a specific symbol in a file. |
| `Ctrl`+`G` | Navigate to a specific line in a file. |

## Java with Spring and Spring Boot Tips
- See [Java with Spring and Spring Boot Tips](/Tech-Ref/Microsoft/Visual-Studio/VS-Code-\(Visual-Studio-Code\)/VS-Code-Java-with-Spring-and-Spring-Boot-Tips).

## Keyboard Shortcuts (Windows)
This is also available from the [IDE's](/Tech-Ref/Software-Development/IDE-\(Integrated-Development-Environment\)) `Help` menu.
- [Keyboard Shortcuts ](https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf)

## Maven Project Vulnerabilities Report
- See [Project Object Model (POM), Tips and Tricks, Vulnerability / Dependency Analytics Report](/Tech-Ref/Apache-Software-Foundation/Apache-Maven/POM-\(Project-Object-Model\)#vulnerability-%2F-dependency-analytics-report-(vs-code)).

## Node.js Tutorial in Visual Studio Code
- [Node.js tutorial in Visual Studio Code](https://code.visualstudio.com/docs/nodejs/nodejs-tutorial).

## User Interface
- [VS Code User Interface](https://code.visualstudio.com/docs/getstarted/userinterface)
   - To enlarge open the image in a new tab/window.
   - ![image.png](/.attachments/image-78308800-143a-42ee-95d2-b595149487a5.png)

## Windows Keyboard with macOS
Tips for using ***VS Code*** on [macOS with a Windows Keyboard](/Tech-Ref/Apple-Inc/Mac-\(Macintosh\)/macOS#windows-keyboard).

### Activities
| Activity | Key Combination (Win) | Notes |
|:-|:-|:-|
| Go to definition | Press and hold `Fn` + `F12`| |
| Fold (collapse to definitions) | `Win` + `k` + `0` | |
| UnFold  |  | |
| Search across all project files | `Win` + `Sft` + `f` | |
