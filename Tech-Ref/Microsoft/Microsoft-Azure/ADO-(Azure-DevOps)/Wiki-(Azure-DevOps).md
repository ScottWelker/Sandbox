[Home](/Slalom-LLC/Slalom-Consulting) | [Glossary](/Glossary) | [Tech Ref](/Tech-Ref) | [Modeling](/Slalom-LLC/Slalom-Consulting/Modeling-\(Slalom\))
**AKA:** ADO Wiki.
**Disambiguation:** [How We Work (Slalom)](/Slalom-LLC/Slalom-Consulting/Terms-\(Slalom-Consulting\)/HWW-\(How-We-Work\)).

[[_TOC_]]

---
# Introduction
***Wiki ([Azure DevOps](/Tech-Ref/Microsoft/Microsoft-Azure/ADO-\(Azure-DevOps\)))*** typically refers to the [Wiki engine](/Tech-Ref/Wiki) built into the [Azure DevOps](/Tech-Ref/Microsoft/Microsoft-Azure/ADO-\(Azure-DevOps\)) products. For example, this very [Wiki](/Tech-Ref/Wiki) is hosted within [Azure DevOps Services](/Tech-Ref/Microsoft/Microsoft-Azure/ADO-\(Azure-DevOps\)/Azure-DevOps-Services).

## Reference
1. [StackOverflow: Azure DevOps Wiki](https://stackoverflow.com/questions/tagged/azure-devops-wiki)
1. [Provisioned wikis vs. published code as a wiki](https://docs.microsoft.com/en-us/azure/devops/project/wiki/provisioned-vs-published-wiki?view=azure-devops)
1. [Add Mermaid diagrams to a Wiki page](https://docs.microsoft.com/en-us/azure/devops/project/wiki/wiki-markdown-guidance?view=azure-devops#add-mermaid-diagrams-to-a-wiki-page)

## Notes
1. _[Azure DevOps](/Tech-Ref/Microsoft/Microsoft-Azure/ADO-\(Azure-DevOps\)) Wikis_ are available in ***Provisioned*** and ***Published*** forms. This page is exclusively about the _provisioned_ Wiki because the _published_ wiki is only supported with the seldom desired/chosen _Azure Repos_. [Git](/Tech-Ref/Software-Development/DevOps-\(Development-and-IT-Operations\)/Git) is generally preferred.
1. The provisioned _[Azure DevOps](/Tech-Ref/Microsoft/Microsoft-Azure/ADO-\(Azure-DevOps\)) Wiki_ is optional but, if used, it is provisioned at the "_project level._" However project-level provisioning can be problematic as that fragments knowledge. Inevitably projects duplicate knowledge.
1. The provisioned _[Azure DevOps](/Tech-Ref/Microsoft/Microsoft-Azure/ADO-\(Azure-DevOps\)) Wiki_ provides a hierarchical storage roughly analogous to a file system. While helpful and familiar for some, others argue this is a harmful violation of the ['Unified' Wiki Design Principle](http://wiki.c2.com/?WikiDesignPrinciples). Notable harms:
   1. Having to address taxonomy, as forced by the Wiki's hierarchical nature, is often a barrier to new contributors, i.e. they sometimes are paralyzed by having to decide where a page belongs and then opt not to contribute.
   1. When an author needs to [link to another page (linkify)](https://en.wiktionary.org/wiki/linkify) they must know or determine that page's taxonomy. This sometimes prevents them from [linking](https://en.wiktionary.org/wiki/linkify). [Hyperlinks](/Tech-Ref/WWW-\(World-Wide-Web\)/Hyperlink) ([linking](https://en.wiktionary.org/wiki/linkify)) are a central value that [Wiki](/Tech-Ref/Wiki) provides.

---
# Topics
1. [markdown-link-check](/Tech-Ref/Software-Development/JavaScript/Node.js/markdown%2Dlink%2Dcheck). :wrench:
1. [Mermaid (Azure DevOps Wiki)](/Tech-Ref/Microsoft/Microsoft-Azure/ADO-\(Azure-DevOps\)/Wiki-\(Azure-DevOps\)/Mermaid-\(Azure-DevOps-Wiki\)).
1. [Modeling](/Slalom-LLC/Slalom-Consulting/Modeling-\(Slalom\)):
   - [Mermaid](/Tech-Ref/Software-Development/Modeling/Mermaid).
1. [Safe CU](/Clients/Safe-CU/Core).
1. [Wiki](/Tech-Ref/Wiki):
   - [Linkify](/Tech-Ref/Wiki/Linkify).
   - [Wiki Gardening](/Tech-Ref/Wiki/Wiki-Gardening).

---
# Tips and Tricks

## Adding Bookmarks
It is sometimes useful to link to a specific location in a page, especially when that location's heading anchor doesn't serve the purpose. [I (SWelker)](/Individuals/Scott-Welker) find that this is especially useful within tables when I want to link to a specific row. 

Within a given Wiki page, you can add an [HTML span element](/Tech-Ref/WWW-\(World-Wide-Web\)/HTML-\(Hypertext-Markup-Language\)) with an [id attribute](/Tech-Ref/WWW-\(World-Wide-Web\)/HTML-\(Hypertext-Markup-Language\)) whose value is the desired bookmark text, e.g.:

```html
<span id="scottwelker">
```
:warning: It is best to keep the id value, `scottwelker` in this example, simple i.e., all lower-case, no special characters. Other variations may work but, I've found them sometimes flaky.

The _bookmark_, `id` value,  is then accessed/referenced by appending one of the following to your URL, the first is the most common ([External](#External)). The later is used when the link you are forming is within one of this Wiki's pages ([Wiki Link](#wiki-link)).

### External
:warning: **This will not work for a Wiki link.** If your link is to be accessed from outside the Wiki, use this:
   - `#scottwelker`, e.g.:
      - `https://dev.azure.com/scottwelker/KM/_wiki/wikis/KM.wiki/2182/CAI-(Cox-Automotive-Inc)#scottwelker`
      - Here: [Scott Welker](https://dev.azure.com/scottwelker/KM/_wiki/wikis/KM.wiki/2182/CAI-(Cox-Automotive-Inc)#scottwelker).

### Wiki Link
If you link is to be accessed from a page in this Wiki, use this:
   - `anchor=scottwelker`, e.g.: 
      - `https://dev.azure.com/scottwelker/KM/_wiki/wikis/KM.wiki/2182/CAI-(Cox-Automotive-Inc)?anchor=scottwelker`
      - Here: [Scott Welker](https://dev.azure.com/scottwelker/KM/_wiki/wikis/KM.wiki/2182/CAI-(Cox-Automotive-Inc)?anchor=scottwelker).

## Careful with Rename/Move
Although the Wiki tries to fix links broken as a result of page rename or move, it often fails to do so, leaving broken links after the move/rename. I can't put my finger on why the Wiki sometimes does or does not self repair the breakage.

[I (SWelker)](/Individuals/Scott-Welker) have a hack'ish [PowerShell](/Tech-Ref/Microsoft/PowerShell) script to recurse the locally cloned repository and "_fix up_" broken links. Consider developing the same if you experience a lot of such breakage. 

## Creating Azure DevOps Wiki Pages from within a Pipeline
- [Creating Azure DevOps WIKI Pages from within a pipeline](https://stefanstranger.github.io/2020/04/12/CreatingAzureDevOpsWIKIPagesFromWithApipeline/)

## Fun With .order Files
- [Docs.Microsoft: .order File](https://docs.microsoft.com/en-us/azure/devops/project/wiki/wiki-file-structure?view=azure-devops#order-file)
   1. [#8966 You should note that removed .order files get recreated](https://github.com/MicrosoftDocs/azure-devops-docs/issues/8966)
   1. [Unwanted, deleted Wiki '.order' files are being regenerated](https://developercommunity.visualstudio.com/t/Unwanted-deleted-Wiki-order-files-ar/1514090)
   1. [Allow disabling of .order file in wiki subfolders](https://developercommunity.visualstudio.com/t/allow-disabling-of-order-file-in-wiki-subfolders/570941)

"_Behind the scenes_" `.order` files are created by the [Azure DevOps](/Tech-Ref/Microsoft/Microsoft-Azure/ADO-\(Azure-DevOps\)) Wiki to track your manual page ordering, i.e. the order in which child pages are listed in the left-hand tree view. In a large [Wiki](/Tech-Ref/Wiki) it is often preferable to remove all `.order` files so that the [Wiki](/Tech-Ref/Wiki) will simply order everything alphabetically. However, as noted [here (issue #8966)](https://github.com/MicrosoftDocs/azure-devops-docs/issues/8966), order files are eventually recreated. Consequently you may want to periodically remove all `.order` files e.g. (with a locally cloned repository):
   1. Open a command prompt and change (`cd`) to your cloned repository sub-folder.
   1. `git pull`
   1. `del /s .order`
   1. `git add .order`
   1. `git commit -m"remove unwanted .order files."`
   1. `git push`

## Linting THIS Azure DevOps Wiki
- [Linting THIS Wiki (remark-cli)](/Tech-Ref/Software-Development/JavaScript/Node.js/unified/remark/remark%2Dcli#linting-this-wiki).

## Mermaid Diagrams
- [Mermaid (Azure DevOps Wiki)](/Tech-Ref/Microsoft/Microsoft-Azure/ADO-\(Azure-DevOps\)/Wiki-\(Azure-DevOps\)/Mermaid-\(Azure-DevOps-Wiki\)).
