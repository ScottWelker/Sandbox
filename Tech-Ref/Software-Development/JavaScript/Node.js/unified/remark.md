[Home](/Slalom-LLC/Slalom-Consulting) | [Glossary](/Glossary) | [Tech Ref](/Tech-Ref) | [Software Development](/Tech-Ref/Software-Development) | [Markdown Parser](/Tech-Ref/Software-Development/Markup-Language/Markdown/Markdown-Parser) | [JavaScript](/Tech-Ref/Software-Development/JavaScript) | [Node.js](/Tech-Ref/Software-Development/JavaScript/Node.js) | [unified](/Tech-Ref/Software-Development/JavaScript/Node.js/unified)
**Disambiguation:** [Markdown Parser](/Tech-Ref/Software-Development/Markup-Language/Markdown/Markdown-Parser#markdown-parser-implementations), [rehype](/Tech-Ref/Software-Development/JavaScript/Node.js/unified/rehype), [RegEx](/Tech-Ref/Software-Development/RegEx-\(Regular-Expression\)).

[[_TOC_]]

---
# Introduction
***remark,*** is the [unified](/Tech-Ref/Software-Development/JavaScript/Node.js/unified) "_processor_" plugin for handling [Markdown](/Tech-Ref/Software-Development/Markup-Language/Markdown) input, a part of the [unified collective](/Tech-Ref/Software-Development/JavaScript/Node.js/unified). remark is [Node.js-based](/Tech-Ref/Software-Development/JavaScript/Node.js). 

The power of remark resides in the fact that once the [markdown](/Tech-Ref/Software-Development/Markup-Language/Markdown) has been parsed, it is transformed to a [syntax tree](/Tech-Ref/Software-Development/Data-Structures/AST-\(Abstract-Syntax-Tree\)). You can then create [unified plugins](/Tech-Ref/Software-Development/JavaScript/Node.js/unified#unified-plugins), using _remark_, to do whatever you want to that [syntax tree](/Tech-Ref/Software-Development/Data-Structures/AST-\(Abstract-Syntax-Tree\)): check the code style, add or remove content, modify content, etc.

- :+1: **[SWelker](/Individuals/Scott-Welker):** It is necessary to understand the [unified ecosystem](/Tech-Ref/Software-Development/JavaScript/Node.js/unified) and create [plugin(s)](/Tech-Ref/Software-Development/JavaScript/Node.js/unified#unified-plugins) to fully leverage _remark's_ capabilities.
   - See the [unified](/Tech-Ref/Software-Development/JavaScript/Node.js/unified) page.

## Reference
1. [remark.js.org](https://remark.js.org/)
1. [GitHub: remark](https://github.com/remarkjs/remark)
   - `npm install remark-cli`
1. [braincoke.fr: An Introduction to Unified and Remark](https://braincoke.fr/blog/2020/03/an-introduction-to-unified-and-remark/#the-unified-collective)
1. [Having Fun with Markdown and Remark](https://gocardless.com/blog/fun-with-markdown-and-remark/)
1. [GitHub: Awesome Remark Resources](https://github.com/remarkjs/awesome-remark)
1. [CSS Tricks: How to Modify Nodes in an Abstract Syntax Tree](https://css-tricks.com/how-to-modify-nodes-in-an-abstract-syntax-tree/)

## Study (SWelker)
1. [Transforming Markdown with Remark & Rehype](https://www.ryanfiller.com/blog/remark-and-rehype-plugins#when-to-use-each)
1. [Having Fun with Markdown and Remark](https://gocardless.com/blog/fun-with-markdown-and-remark/)
1. [Writing plugins for remark...](https://www.huy.dev/2018-05-remark-gatsby-plugin-part-2/)

---
# Topics
1. [CommonMark](/Tech-Ref/Software-Development/Markup-Language/Markdown/CommonMark).
1. [JavaScript](/Tech-Ref/Software-Development/JavaScript) ![programming-sm.png](/.attachments/programming-sm-84511b90-2d77-4364-8b25-7bee99dd4060.png).
1. [Markdown](/Tech-Ref/Software-Development/Markup-Language/Markdown).
1. [Markdown Parser](/Tech-Ref/Software-Development/Markup-Language/Markdown/Markdown-Parser).
1. [Markdown Abstract Syntax Tree (mdast)](/Tech-Ref/Software-Development/JavaScript/Node.js/unified/UST-\(Universal-Syntax-Tree\)/mdast-\(Markdown-Abstract-Syntax-Tree\)).
1. [Node.js](/Tech-Ref/Software-Development/JavaScript/Node.js).
1. [npm](/Tech-Ref/Software-Development/JavaScript/npm).
1. [Unified Collective](/Tech-Ref/Software-Development/JavaScript/Node.js/unified).

---
# Third-Party Plugins
Here are the few [unified](/Tech-Ref/Software-Development/JavaScript/Node.js/unified), [remark](/Tech-Ref/Software-Development/JavaScript/Node.js/unified/remark) plugins about which we have some notes in [this Wiki](/Tech-Ref/Microsoft/Microsoft-Azure/ADO-\(Azure-DevOps\)/Wiki-\(Azure-DevOps\)).

## remark-cli
- [remark-cli](/Tech-Ref/Software-Development/JavaScript/Node.js/unified/remark/remark%2Dcli).

## remark-gfm
- [remark-gfm](/Tech-Ref/Software-Development/JavaScript/Node.js/unified/remark/remark%2Dgfm).

## remark-parse
- [remark-parse](/Tech-Ref/Software-Development/JavaScript/Node.js/unified/remark/remark%2Dparse).

## remark-lint
- [remark-lint](/Tech-Ref/Software-Development/JavaScript/Node.js/unified/remark/remark%2Dlint).

## remark-rehype
- [remark-rehype](/Tech-Ref/Software-Development/JavaScript/Node.js/unified/remark/remark%2Drehype).

---
# Tips and Tricks

## ANSI Colors (VS Code)
Elements of the [unified ecosystem](/Tech-Ref/Software-Development/JavaScript/Node.js/unified) may emit [ANSI Escape Codes](/Tech-Ref/ANSI-Escape-Codes) that aren't handled/displayed well in certain contexts. [VS Code (Visual Studio Code)](/Tech-Ref/Microsoft/Visual-Studio/VS-Code-\(Visual-Studio-Code\)), with the [ANSI Colors extension](/Tech-Ref/Microsoft/Visual-Studio/VS-Code-\(Visual-Studio-Code\)/ANSI-Colors-\(VS-Code\)) may be of use. 
- [ANSI Colors (VS Code)](/Tech-Ref/Microsoft/Visual-Studio/VS-Code-\(Visual-Studio-Code\)/ANSI-Colors-\(VS-Code\)).

## How to Debug Unified Collective Components
- [How to debug unified, rehype, or remark and fix bugs in markdown processing](https://swizec.com/blog/how-to-debug-unified-rehype-or-remark-and-fix-bugs-in-markdown-processing-2/)

## Linting THIS Wiki
- [Linting Azaure DevOps Wiki](/Tech-Ref/Software-Development/JavaScript/Node.js/unified/remark/remark%2Dcli/Linting-Azaure-DevOps-Wiki).

## Remark CLI
- [remark-cli](/Tech-Ref/Software-Development/JavaScript/Node.js/unified/remark/remark%2Dcli).
