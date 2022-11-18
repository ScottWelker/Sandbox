[Home](/Slalom-LLC/Slalom-Consulting) | [Glossary](/Glossary) | [Tech Ref](/Tech-Ref) | [Markup Language](/Tech-Ref/Software-Development/Markup-Language)
**Disambiguation:** [HTML](/Tech-Ref/WWW-\(World-Wide-Web\)/HTML-\(Hypertext-Markup-Language\)), [Markup Language](/Tech-Ref/Software-Development/Markup-Language), [Markup (Apple)](/Tech-Ref/Apple-Inc/Markup-\(Apple\)), [Wikitext](/Tech-Ref/Software-Development/Markup-Language/Wikitext).

[[_TOC_]]

---
# Introduction
"_***Markdown*** is a lightweight markup language for creating formatted text using a plain-text editor. John Gruber and Aaron Swartz created Markdown in 2004 as a markup language that is appealing to human readers in its source code form. Markdown is widely used in blogging, instant messaging, online forums, collaborative software, documentation pages, and readme files._"

"_The initial description of Markdown contained ***ambiguities and raised unanswered questions***. To correct these problems, later implementations introduced subtle differences from the original version as well as syntax extensions._"

## Reference
1. [Wikipedia: Markdown](https://en.wikipedia.org/wiki/Markdown)
1. [A Guide to Markdown, the Formatting Language of the Internet](https://medium.com/swlh/a-guide-to-markdown-the-formatting-language-of-the-internet-3cbec2f388f3)
1. [For focused writing, Markdown is your best friend](https://www.fastcompany.com/40586767/for-focused-writing-markdown-is-your-best-friend)
1. [Awesome Markdown](https://github.com/BubuAnabelas/awesome-markdown)

### Tech. Reference
1. [Choosing the Right Markdown Parser](https://css-tricks.com/choosing-right-markdown-parser/)
1. [Is markdown even a regular language?](https://dannykong12.com/blog/writing-a-markdown-compiler-part-1.html)

### Study
1. [Transforming Markdown with Remark & Rehype](https://www.ryanfiller.com/blog/remark-and-rehype-plugins#when-to-use-each)

---
# Topics
1. [CommonMark](/Tech-Ref/Software-Development/Markup-Language/Markdown/CommonMark).
1. [markdown link check](/Tech-Ref/Software-Development/JavaScript/Node.js/markdown%2Dlink%2Dcheck).
1. [GitHub Flavored Markdown (GFM)](/Tech-Ref/Software-Development/Markup-Language/Markdown/GFM-\(GitHub-Flavored-Markdown\)).
1. [Markdown Parser](/Tech-Ref/Software-Development/Markup-Language/Markdown/Markdown-Parser).
1. [Markup Language](/Tech-Ref/Software-Development/Markup-Language).
1. [Quip](/Tech-Ref/Quip).
1. [Wiki](/Tech-Ref/Wiki).
1. [XSL (Extensible Stylesheet Language Family)](/Tech-Ref/Software-Development/Markup-Language/XML-\(eXtensible-Markup-Language\)/XSL-\(Extensible-Stylesheet-Language-Family\)).

---
# Features

## Core Features
The core markdown language supports a number of default features that are quite useful. Although different implementations support a range of extended features, they should all support at least these. 

### Inline HTML

### Automatic Paragraphs

### Headers

### Blockquotes

### Lists

### Code Blocks

### Horizontal Rules

### Links

### Emphasis

### Inline Code

### Images.

## Noteworthy Extensions
This section is by no means complete. Just jotting down some [I've (SWelker)](/Individuals/Scott-Welker) heard of or used.

### CommonMark
- [CommmonMark](/Tech-Ref/Software-Development/Markup-Language/Markdown/CommonMark). 

### Github Flavored Markdown (GFM)
- [GitHub Flavored Markdown (GFM)](/Tech-Ref/Software-Development/Markup-Language/Markdown/GFM-\(GitHub-Flavored-Markdown\)).

### Markdown Extra
- [TBD (To Be Determined)](/Glossary/TBD-\(To-Be-Determined\)).

### Multi-Markdown
A project that has Multi-Markdown support probably has most of these features.
- :question: Is this [Wikipedia: MultiMark](https://en.wikipedia.org/wiki/MultiMarkdown) the same thing?

#### Fenced Codeblocks

#### Syntax Highlighting

#### Tables

#### Metadata

#### Fragments/Cross References Links

#### Footnotes

#### Strikethrough

#### Definition Lists

#### Math

---
# Tips and Tricks

## Lists Tips and Tricks

### Continue List Item
- [Markdown custom numbered list](https://stackoverflow.com/a/71158230/418950)

Adding four spaces before "_continuation text_" associates that text with the preceding list item and preserves list numbering e.g. 

**E.g.**
```
1. One
    Continuation text here.
1. Two
```
**Yields:**

1. One
    Continuation text here.
1. Two

### Set Starting Number
- [Markdown custom numbered list](https://stackoverflow.com/a/71158230/418950)

You can specify a starting list number.

**E.g.**
```
5. Start at Five (5).
1. Now Six
1. Seven

```
**Yields:**
5. Start at Five (5).
1. Now Six
1. Seven

## Markdown Guide, Basic Syntax
- [MarkdownGuide: Basic Syntax](https://www.markdownguide.org/basic-syntax/)
  :+1: Some of these rules are new to [me (SWelker)](/Individuals/Scott-Welker) and I've not always followed them (12/2021), especially the rules for headings and line breaks.

## Markdown Transformation (remark)
- [Remark](/Tech-Ref/Software-Development/JavaScript/Node.js/unified/remark).

## Writing a Markdown Compiler

### Part 1: What's in a Language
- [Writing a Markdown Compiler Part 1: What's in a Language](https://dannykong12.com/blog/writing-a-markdown-compiler-part-1.html)

## Markdown Here (add-on)
- [Markdown Here](https://markdown-here.com/features.html)