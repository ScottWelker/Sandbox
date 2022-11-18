[Home](/Slalom-LLC/Slalom-Consulting) | [Glossary](/Glossary) | [Tech Ref](/Tech-Ref) | [Software Development](/Tech-Ref/Software-Development) | [Visual Studio Code](/Tech-Ref/Microsoft/Visual-Studio/VS-Code-\(Visual-Studio-Code\))

[[_TOC_]]

# Introduction
The ***Javadoc Tools for [Visual Studio Code](/Tech-Ref/Microsoft/Visual-Studio/VS-Code-\(Visual-Studio-Code\))*** extension allows you to generate [Javadoc](/Tech-Ref/Software-Development/Java/Java-Language/Javadoc) comments for all methods within a class.

- ![image.png](/.attachments/image-2da297f9-4739-4b78-bb64-50c831fca544.png)

## Reference
1. [Visual Studio Marketplace: Javadoc Tools for Visual Studio Code](https://marketplace.visualstudio.com/items?itemName=madhavd1.javadoc-tools)
1. https://github.com/madhavd1/vscode-javadoc-tools

---
# Topics
1. [Java](/Tech-Ref/Software-Development/Java).
1. [Javadoc](/Tech-Ref/Software-Development/Java/Java-Language/Javadoc).
1. [Visual Studio Code](/Tech-Ref/Microsoft/Visual-Studio/VS-Code-\(Visual-Studio-Code\)).

---
# Commands
| :warning: Warning! |
|:-|
| **08/30/2021 [SWelker](/Individuals/Scott-Welker):** May be dated! This is a static image captured from a [Reference](#Reference) above. |

Here are some [VS Code 'command pallette'](/Tech-Ref/Microsoft/Visual-Studio/VS-Code-\(Visual-Studio-Code\)#command-palette) commands for this extension.

- Open image in a new tab/window to enlarge.
- ![image.png](/.attachments/image-41f4e2a3-1a1c-4f08-b57a-84f65d3c44b0.png)

---
# Tips and Tricks

## Unexpected Token '-public' in expression or statement.
Although [I've (SWelker)](/Individuals/Scott-Welker) not yet found the fix, this seems to be a [PowerShell](/Tech-Ref/Microsoft/PowerShell) error message. Likely a script that is engaged by the extension.
   - :+1: []() This is definitely a [PowerShell](/Tech-Ref/Microsoft/PowerShell) error. Although it's not shown in the image below, text above clearly indicates it is [PowerShell](/Tech-Ref/Microsoft/PowerShell). Mucking with the command line reveals that the extension (v1.4.0) is attempting to execute a malformed [PowerShell](/Tech-Ref/Microsoft/PowerShell) command. When corrected other project related [Javadoc](/Tech-Ref/Software-Development/Java/Java-Language/Javadoc) errors occur, seemingly related to [Spring Boot](/Tech-Ref/Software-Development/Java/Java-Platform-Editions/Jakarta-EE-\(Enterprise-Edition\)/Spring-Framework/Spring-Boot).
- :warning: **09/07/2021 [SWelker](/Individuals/Scott-Welker):** Abandoned attempts to address this - for now. It's an unwelcome distraction.

- ![image.png](/.attachments/image-154f136f-0ee9-496e-afe6-100650c71a2c.png)
