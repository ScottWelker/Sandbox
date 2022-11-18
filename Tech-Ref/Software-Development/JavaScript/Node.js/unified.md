[Home](/Slalom-LLC/Slalom-Consulting) | [Glossary](/Glossary) | [Tech Ref](/Tech-Ref) | [Software Development](/Tech-Ref/Software-Development) | [JavaScript](/Tech-Ref/Software-Development/JavaScript) | [Node.js](/Tech-Ref/Software-Development/JavaScript/Node.js) | [Markdown Parser](/Tech-Ref/Software-Development/Markup-Language/Markdown/Markdown-Parser)

[[_TOC_]]

---
# Introduction
"_***unified***, sometimes the '_unified collective_', is a friendly interface backed by an ecosystem of plugins built for creating and manipulating content. You don’t have to worry about parsing as you have the primitives to build on._"

"_We compile content to syntax trees and syntax trees to content. We also provide hundreds of packages to work on the trees in between. You can build on the unified collective to make all kinds of interesting things._"

## Reference
1. [Unified Collective](https://github.com/unifiedjs/collective#teams)
1. https://unifiedjs.com/
   1. [Learn Unified](https://unifiedjs.com/learn/)
      - [Introduction to Unified](https://unifiedjs.com/learn/guide/introduction-to-unified/).
      - :star: [Using Unified](https://unifiedjs.com/learn/guide/using-unified/)
      - [Tree Traversal](https://unifiedjs.com/learn/recipe/tree-traversal/)
      - [Find Node](https://unifiedjs.com/learn/recipe/find-node/)
      - [Using Plugins](https://unifiedjs.com/learn/guide/using-plugins/) 
      - [Create a Plugin](https://unifiedjs.com/learn/guide/create-a-plugin/)
1. [GitHub: Awesome Unified (references)](https://github.com/unifiedjs/awesome-unified)
1. [An Introduction to Unified and Remark](https://braincoke.fr/blog/2020/03/an-introduction-to-unified-and-remark/#the-unified-collective)
1. [How to Modify Nodes in an Abstract Syntax Tree](https://css-tricks.com/how-to-modify-nodes-in-an-abstract-syntax-tree/)

---
# Topics
1. [Hypertext Markup Language (HTML)](/Tech-Ref/WWW-\(World-Wide-Web\)/HTML-\(Hypertext-Markup-Language\)).
1. [JavaScript](/Tech-Ref/Software-Development/JavaScript) ![programming-sm.png](/.attachments/programming-sm-84511b90-2d77-4364-8b25-7bee99dd4060.png).
1. [Markdown](/Tech-Ref/Software-Development/Markup-Language/Markdown).
1. [Markdown Parser](/Tech-Ref/Software-Development/Markup-Language/Markdown/Markdown-Parser).
1. [Markup Language](/Tech-Ref/Software-Development/Markup-Language).
1. [Node.js](/Tech-Ref/Software-Development/JavaScript/Node.js).
1. [npm](/Tech-Ref/Software-Development/JavaScript/npm).
1. [Universal Syntax Tree (UST/unist)](/Tech-Ref/Software-Development/JavaScript/Node.js/unified/UST-\(Universal-Syntax-Tree\)).

---
# Usage
- https://github.com/unifiedjs/handbook#usage

With unified you don't handle syntax or parsing yourself. Instead you select your [processor(s)](#unified-collective-(ecosystems/processors)) and chain them together, with or without [plugin(s)](#unified-plugins) that you select or develop, and then initiate the "_unified process_" to accomplish your goals.

<details>
  <summary>Show/Hide Annotated Code Example (image).</summary>

## Code Example
The circled numbers, 1..4, correspond to the [Code Narration](#code-narration) top-level numbers below.
- ![image.png](/.attachments/image-9aa422ee-40bd-451b-9a4e-9d802ca02558.png)
</details>

<details>
  <summary>Show/Hide Code Narration.</summary>

## Code Narration
Top-level numbers here correspond to the [Code Example's](#code-narration) circled numbers, 1..4 above. This code illustrates just one example use-case. Many, many others are possible. Briefly:
1. Load required [modules](/Tech-Ref/Software-Development/JavaScript/Module-\(JavaScript\)), `require(...)`. Seven different ones in this use-case:
   1. [unified](/Tech-Ref/Software-Development/JavaScript/Node.js/unified).
   1. [remark-parse](/Tech-Ref/Software-Development/JavaScript/Node.js/unified/remark/remark%2Dparse).
   1. [remark-rehype](/Tech-Ref/Software-Development/JavaScript/Node.js/unified/remark/remark%2Drehype).
   1. [rehype-document](/Tech-Ref/Software-Development/JavaScript/Node.js/unified/rehype/rehype%2Ddocument).
   1. [rehype-format](/Tech-Ref/Software-Development/JavaScript/Node.js/unified/rehype/rehype%2Dformat).
   1. [rehype-stringify](/Tech-Ref/Software-Development/JavaScript/Node.js/unified/rehype/rehype%2Dstringify).
   1. [vfile-reporter (unified)](/Tech-Ref/Software-Development/JavaScript/Node.js/unified/vfile%2Dreporter).
1. Instantiate (construct) the unified [processor](#unified-collective-(ecosystems/processors)), `unified()`.
1. Chain the plugins together, `.use(...)`. Five in this use-case:
   1. [markdown (remark-parse)](/Tech-Ref/Software-Development/JavaScript/Node.js/unified/remark/remark%2Dparse).
   1. [remark2rehype (remark-rehype)](/Tech-Ref/Software-Development/JavaScript/Node.js/unified/remark/remark%2Drehype).
   1. [doc (rehype-document)](/Tech-Ref/Software-Development/JavaScript/Node.js/unified/rehype/rehype%2Ddocument).
   1. [format (rehype-format)](/Tech-Ref/Software-Development/JavaScript/Node.js/unified/rehype/rehype%2Dformat).
   1. [html (rehype-stringify)](/Tech-Ref/Software-Development/JavaScript/Node.js/unified/rehype/rehype%2Dstringify).
1. Kickoff the _unified_ process, `.process(...)`, passing your input and a function to handle and "_report_" the processing status.
   + "_Reporting_" leverages the [vfile-reporter](/Tech-Ref/Software-Development/JavaScript/Node.js/unified/vfile%2Dreporter) plugin.

</details>

---
# Processors (Parsers, Compilers, and Transpilers)
Typical use-cases generally require both a "_parser_" and a "_compiler_", which most "_[Processors](#unified-collective-(ecosystems/processors))_" provide. Although, strictly speaking, you might not need to use both a parser and a compiler.

The unified "_[Processor](#unified-collective-(ecosystems/processors))_" allows [plugins](#unified-plugins) to be chained together to transform content. The chain of [plugins](#unified-plugins) defines how your content flows through the [processor](#unified-collective-(ecosystems/processors)).

## Parsers
A parser takes a string and tokenizes it based on syntax. A [markdown parser](/Tech-Ref/Software-Development/Markup-Language/Markdown/Markdown-Parser) would turn `# Hello, world!` into a **heading** node.

## Compilers
A compiler turns an [UST/AST](/Tech-Ref/Software-Development/JavaScript/Node.js/unified/UST-\(Universal-Syntax-Tree\)) into its "output". This is typically a string. Again, most "_[Processors](#unified-collective-(ecosystems/processors))_" provide both a _Parser_ and a _Compiler_.

## Transpilers
Transpilers convert one [UST/AST](/Tech-Ref/Software-Development/JavaScript/Node.js/unified/UST-\(Universal-Syntax-Tree\)) syntax tree into to another.

---
# Unified Collective (Ecosystems/Processors)

## redot Graphviz
- [redot](/Tech-Ref/Software-Development/JavaScript/Node.js/unified/redot).

## rehype HTML
- [rehype](/Tech-Ref/Software-Development/JavaScript/Node.js/unified/rehype).

## remark Markdown
- [remark](/Tech-Ref/Software-Development/JavaScript/Node.js/unified/remark).

## retext Natural Language
- [retext](/Tech-Ref/Software-Development/JavaScript/Node.js/unified/retext).

---
# Syntax Tree Specifications (USTs)
- [Universal Syntax Tree (UST)](/Tech-Ref/Software-Development/JavaScript/Node.js/unified/UST-\(Universal-Syntax-Tree\)).

---
# Unified 'Utilities'
"_unified Utilities_" are simply functions that operate on nodes. 

## Syntax Tree Specific Utilities
There are several projects that deal with nodes from specifications implementing [unist](/Tech-Ref/Software-Development/JavaScript/Node.js/unified/UST-\(Universal-Syntax-Tree\)):
   - [hast utilities](https://github.com/syntax-tree/hast#list-of-utilities)
   - [mdast utilities](https://github.com/syntax-tree/mdast#list-of-utilities)
   - [nlcst utilities](https://github.com/syntax-tree/nlcst#list-of-utilities)
   - [xast utilities](https://github.com/syntax-tree/xast#list-of-utilities)

## General unified Utilities
- See [GitHub: unist, List of Utilities](https://github.com/syntax-tree/unist#list-of-utilities).

| Utility | Description |
|:-|:-|
| unist-util-ancestor | get the common ancestor of one or more nodes |
| unist-util-assert | assert nodes |
| unist-util-filter | create a new tree with all nodes that pass the given function |
| unist-util-find | find a node by condition |
| unist-util-find-after | find a node after another node |
| unist-util-find-all-after | find nodes after another node or index |
| unist-util-find-all-before | find nodes before another node or index |
| unist-util-find-all-between | find nodes between two nodes or positions |
| unist-util-find-before | find a node before another node |
| unist-util-flat-filter | flat map version of unist-util-filter |
| unist-util-flatmap | create a new tree by expanding a node into many |
| unist-util-generated | check if a node is generated |
| unist-util-index | index nodes by property or computed key |
| unist-util-inspect | node inspector |
| unist-util-is | check if a node passes a test |
| unist-util-map | create a new tree by mapping nodes |
| unist-util-modify-children | modify direct children of a parent |
| unist-util-parents | parent references on nodes |
| unist-util-position | get positional info of nodes |
| unist-util-reduce | recursively reduce a tree |
| unist-util-remove | remove nodes from trees |
| unist-util-remove-position | remove positional info from trees |
| unist-util-select | select nodes with CSS-like selectors |
| unist-util-size | calculate the number of nodes in a tree |
| unist-util-source | get the source of a value (node or position) in a file |
| unist-util-stringify-position | stringify a node, position, or point |
| unist-util-visit | recursively walk over nodes |
| unist-util-visit-parents | recursively walk over nodes, with a stack of parents |
| unist-util-visit-children | visit direct children of a parent |
| unist-util-visit-all-after | visit nodes after another node |
| unist-builder | helper for creating trees |
| unist-builder-blueprint | convert trees to unist-builder notation |
| unist-builder-blueprint-cli | CLI to convert trees to unist-builder notation |

---
# Unified Plugins

## Basic Structure
- [Transforming Markdown with Remark & Rehype](https://www.ryanfiller.com/blog/remark-and-rehype-plugins).

Your custom plugin works via a [JavaScript](/Tech-Ref/Software-Development/JavaScript) function that you create which returns a `transformer` method. That transformer method is run on each `node` found by the `unist-util-visit` package’s `visit` method. The plugin will be called by the `unified` process and will be passed the [AST tree](/Tech-Ref/Software-Development/Data-Structures/AST-\(Abstract-Syntax-Tree\)). There are many ways to directly mutate the tree.

---
# Tips and Tricks

## ANSI Colors (VS Code)
Elements of the [unified ecosystem](/Tech-Ref/Software-Development/JavaScript/Node.js/unified) may emit [ANSI Escape Codes](/Tech-Ref/ANSI-Escape-Codes) that aren't handled/displayed well in certain contexts. [VS Code (Visual Studio Code)](/Tech-Ref/Microsoft/Visual-Studio/VS-Code-\(Visual-Studio-Code\)), with the [ANSI Colors extension](/Tech-Ref/Microsoft/Visual-Studio/VS-Code-\(Visual-Studio-Code\)/ANSI-Colors-\(VS-Code\)) may be of use. 
- [ANSI Colors (VS Code)](/Tech-Ref/Microsoft/Visual-Studio/VS-Code-\(Visual-Studio-Code\)/ANSI-Colors-\(VS-Code\))

## How to Debug Unified Collective Components
- [How to debug unified, rehype, or remark and fix bugs in markdown processing](https://swizec.com/blog/how-to-debug-unified-rehype-or-remark-and-fix-bugs-in-markdown-processing-2/)