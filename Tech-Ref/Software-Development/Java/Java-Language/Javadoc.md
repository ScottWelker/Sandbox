[Home](/Slalom-LLC/Slalom-Consulting) | [Glossary](/Glossary) | [Tech Ref](/Tech-Ref) | [Software Development](/Tech-Ref/Software-Development) | [Java](/Tech-Ref/Software-Development/Java) | [Java Language](/Tech-Ref/Software-Development/Java/Java-Language)

[[_TOC_]]

---
# Introduction
"_***Javadoc*** (originally cased JavaDoc) is a documentation generator created by Sun Microsystems for the [Java language](/Tech-Ref/Software-Development/Java/Java-Language) (now owned by [Oracle Corporation](/Tech-Ref/Oracle-Corporation)) for generating API documentation in [HTML](/Tech-Ref/WWW-\(World-Wide-Web\)/HTML-\(Hypertext-Markup-Language\)) format from [Java](/Tech-Ref/Software-Development/Java) source code. The [HTML](/Tech-Ref/WWW-\(World-Wide-Web\)/HTML-\(Hypertext-Markup-Language\)) format is used for adding the convenience of being able to hyperlink related documents together._"

"_The "doc comments" format used by Javadoc is the de facto industry standard for documenting Java classes. Some [IDEs](/Tech-Ref/Software-Development/IDE-\(Integrated-Development-Environment\)), like IntelliJ IDEA, [NetBeans](/Tech-Ref/Apache-Software-Foundation/Apache-NetBeans) and [Eclipse](/Tech-Ref/Eclipse-Foundation/Eclipse), automatically generate Javadoc [HTML](/Tech-Ref/WWW-\(World-Wide-Web\)/HTML-\(Hypertext-Markup-Language\)). Many file editors assist the user in producing Javadoc source and use the Javadoc info as internal references for the programmer._"

## Reference
1. [Wikipedia: Javadoc](https://en.wikipedia.org/wiki/Javadoc)

---
# Topics
1. [Eclipse](/Tech-Ref/Eclipse-Foundation/Eclipse).
1. [HTML](/Tech-Ref/WWW-\(World-Wide-Web\)/HTML-\(Hypertext-Markup-Language\)).
1. [IDEs](/Tech-Ref/Software-Development/IDE-\(Integrated-Development-Environment\)).
1. [Java](/Tech-Ref/Software-Development/Java). 
1. [Java language](/Tech-Ref/Software-Development/Java/Java-Language).
1. [NetBeans](/Tech-Ref/Apache-Software-Foundation/Apache-NetBeans).
1. [Oracle Corporation](/Tech-Ref/Oracle-Corporation).

---
# Tips and Tricks

## Adding JavaDoc Comments
- [Dummies: How to Use JavaDoc to Document Your Classes](https://www.dummies.com/programming/java/how-to-use-javadoc-to-document-your-classes/)

The basic rule for creating JavaDoc comments is that they begin with `/**` and end with `*/`. You can place JavaDoc comments in any of three different locations in a source file:
   1. Immediately before the declaration of a public class.
   1. Immediately before the declaration of a public field.
   1. Immediately before the declaration of a public method or constructor.

A JavaDoc comment can include text that describes the class, field, or method. Each subsequent line of a multiline JavaDoc comment usually begins with an asterisk. JavaDoc ignores this asterisk and any white space between it and the first word on the line.

The text in a JavaDoc comment can include [HTML markup](/Tech-Ref/WWW-\(World-Wide-Web\)/HTML-\(Hypertext-Markup-Language\)) if you want to apply fancy formatting. You should avoid using heading tags and the like because JavaDoc creates those, and your heading tags just confuse things. But you can use tags for boldface and italics or to format code examples. In addition, you can include special doc tags that provide specific information used by JavaDoc to format the documentation pages.

### Doc Tags
![image.png](/.attachments/image-7ccf86a8-b478-4787-8d5f-e92ace0e360f.png)

## Javadoc Tools for Visual Studio Code
- [Javadoc Tools for Visual Studio Code](/Tech-Ref/Microsoft/Visual-Studio/VS-Code-\(Visual-Studio-Code\)/Javadoc-Tools-for-Visual-Studio-Code).
