[Home](/Slalom-LLC/Slalom-Consulting) | [Glossary](/Glossary) | [Tech Ref](/Tech-Ref) | [Software Development](/Tech-Ref/Software-Development) | [JavaScript](/Tech-Ref/Software-Development/JavaScript) | [Node.js](/Tech-Ref/Software-Development/JavaScript/Node.js) | [unified](/Tech-Ref/Software-Development/JavaScript/Node.js/unified) | [remark](/Tech-Ref/Software-Development/JavaScript/Node.js/unified/remark) | [remark-lint](/Tech-Ref/Software-Development/JavaScript/Node.js/unified/remark/remark%2Dlint)

[[_TOC_]]

---
# Introduction
This page was born of [my (SWelker)](/Individuals/Scott-Welker) desire to use [unified ecosystem](/Tech-Ref/Software-Development/JavaScript/Node.js/unified) elements to help maintain and eventually export and transform [this Azure DevOps Wiki](/Tech-Ref/Microsoft/Microsoft-Azure/ADO-\(Azure-DevOps\)/Wiki-\(Azure-DevOps\)). 

This arose out of last minute requests to transfer [formalized](/Glossary/KM-\(Knowledge-Management\)#formalized) knowledge, first to [SAFE Credit Union (SAFE CU)](/Clients/Safe-CU) and, later to [Cox Automotive Inc. (CAI)](/Clients/CAI-\(Cox-Automotive-Inc\)/Infrastructure-\(CAI\)/Systems-and-Services-\(CAI\)/GitHub-\(CAI\)/GHE%2Dbased-Knowledge-Store-\(CAI\)/Import-Slalom-Knowledge-\(CAI-GHE%2Dbased-Knowledge-Store\)). 

With the later, [Cox Automotive Inc. (CAI)](/Clients/CAI-\(Cox-Automotive-Inc\)/Infrastructure-\(CAI\)/Systems-and-Services-\(CAI\)/GitHub-\(CAI\)/GHE%2Dbased-Knowledge-Store-\(CAI\)/Import-Slalom-Knowledge-\(CAI-GHE%2Dbased-Knowledge-Store\)), initiative it became clear that new tools were needed, largely due to the recognition that [Markdown](/Tech-Ref/Software-Development/Markup-Language/Markdown) is a "_non-regular language_." See [RegEx to Transform Markdown Links](/Clients/CAI-\(Cox-Automotive-Inc\)/Infrastructure-\(CAI\)/Systems-and-Services-\(CAI\)/GitHub-\(CAI\)/GHE%2Dbased-Knowledge-Store-\(CAI\)/Import-Slalom-Knowledge-\(CAI-GHE%2Dbased-Knowledge-Store\)#regex-to-transform-markdown-links).

## Notable Tools
1. [Command Line Interface (CLI)](/Tech-Ref/CLI-\(Command-Line-Interface\)).
1. [grep](/Tech-Ref/Software-Development/UnxUtils/grep).
1. [remark procesor](/Tech-Ref/Software-Development/JavaScript/Node.js/unified/remark).
   - [remark-lint plugin](/Tech-Ref/Software-Development/JavaScript/Node.js/unified/remark/remark%2Dlint):
      - [remark-lint-no-undefined-references rule](/Tech-Ref/Software-Development/JavaScript/Node.js/unified/remark/remark%2Dlint/remark%2Dlint%2Dno%2Dundefined%2Dreferences).
1. [remark-cli](/Tech-Ref/Software-Development/JavaScript/Node.js/unified/remark/remark%2Dcli).

## Reference
1. [StackOverflow: Configure remark-lint-no-undefined-references plugin/rule 'Allow' option for remark-cli?](https://stackoverflow.com/questions/71417416/configure-remark-lint-no-undefined-references-plugin-rule-allow-option-for-rem)
   - **Solved:** 03/30/2022
   - **Updated:** 03/30/2022
   - **Updated:** 03/28/2022
   - **Updated:** 03/14/2022

---
# Topics
1. [Markdown](/Tech-Ref/Software-Development/Markup-Language/Markdown).
1. [Node.js](/Tech-Ref/Software-Development/JavaScript/Node.js).
1. [unified](/Tech-Ref/Software-Development/JavaScript/Node.js/unified):
   - [remark](/Tech-Ref/Software-Development/JavaScript/Node.js/unified/remark):
      - [remark-lint](/Tech-Ref/Software-Development/JavaScript/Node.js/unified/remark/remark%2Dlint):
         - [remark-lint-no-undefined-references](/Tech-Ref/Software-Development/JavaScript/Node.js/unified/remark/remark%2Dlint/remark%2Dlint%2Dno%2Dundefined%2Dreferences).
   - [remark-cli](/Tech-Ref/Software-Development/JavaScript/Node.js/unified/remark/remark%2Dcli).

---
# Linting THIS Wiki
Here are some commands used to check [this Wiki](/Tech-Ref/Microsoft/Microsoft-Azure/ADO-\(Azure-DevOps\)/Wiki-\(Azure-DevOps\)) using _remark-cli_, [remark-lint](/Tech-Ref/Software-Development/JavaScript/Node.js/unified/remark/remark%2Dlint), and various [remark-lint](/Tech-Ref/Software-Development/JavaScript/Node.js/unified/remark/remark%2Dlint) rules.

## Setup
1. [Git](/Tech-Ref/Software-Development/DevOps-\(Development-and-IT-Operations\)/Git) repository housing [this Wiki](/Tech-Ref/Microsoft/Microsoft-Azure/ADO-\(Azure-DevOps\)/Wiki-\(Azure-DevOps\)) cloned to a `KM.wiki` sub-folder.
   - :+1: Make sure the local repository is up-to-date, `git pull`.
1. [remark](/Tech-Ref/Software-Development/JavaScript/Node.js/unified/remark) and  [remark-cli](/Tech-Ref/Software-Development/JavaScript/Node.js/unified/remark/remark%2Dcli) each installed ([npm](/Tech-Ref/Software-Development/JavaScript/npm)) globally (`-g`).
1. [remark-lint](/Tech-Ref/Software-Development/JavaScript/Node.js/unified/remark/remark%2Dlint) **NOT** installed globally. 
   - Avoided global install due to suspected, but unsubstantiated, concerns. See [Multiple globally installed presets and plugins don’t work #165](https://github.com/remarkjs/remark-lint/issues/165). 
   - :+1: [Lint Undefined References](#Lint-Undefined-References) also requires [remark-lint-no-undefined-references](/Tech-Ref/Software-Development/JavaScript/Node.js/unified/remark/remark%2Dlint/remark%2Dlint%2Dno%2Dundefined%2Dreferences). Future examples may require installation of their own third-party or custom plugins or rules.
1. [Windows Command Prompt](/Tech-Ref/CLI-\(Command-Line-Interface\)) opened with the working folder set (`cd`) to the `KM.wiki` folder's parent.

## Lint Presets
In the command that follows we use only [remark-lint's](/Tech-Ref/Software-Development/JavaScript/Node.js/unified/remark/remark%2Dlint) presets. This finds no issues. 

### Command
```dos
remark --use remark-lint KM.wiki 2>&1 > c:\temp\KM.ansi
```

Here is what the command does:
1. `remark` invokes the [remark-cli](/Tech-Ref/Software-Development/JavaScript/Node.js/unified/remark/remark%2Dcli) (and the [remark processor](/Tech-Ref/Software-Development/JavaScript/Node.js/unified/remark)).
1. `--use remark-lint` tells the [remark processor](/Tech-Ref/Software-Development/JavaScript/Node.js/unified/remark) to _lint_ the input files.
1. `KM.wiki` tells the [remark processor](/Tech-Ref/Software-Development/JavaScript/Node.js/unified/remark) to recurse this folder and operate on every `.md` file found.

### Output
Output will be something like the following. [I've (SWelker)](/Individuals/Scott-Welker) cut this down to just two lines and shown it as seen in the [VS Code editor](#ansi-colors-(vs-code)). No issues on any of the roughly 1000 pages.
- ![image.png](/.attachments/image-bfd5e8a4-afe2-4cab-a62f-ae5808471842.png)

### Improved Command
A slight improvement is to run the same command but pipe the results into [grep](/Tech-Ref/Software-Development/UnxUtils/grep) to strip out all the `no issues found` "_noise._" This makes it easier to tell that there are indeed no issues found. 
   - `remark --use remark-lint KM.wiki 2>&1 | grep -v "no issues found"`

## Lint Undefined References
|:construction: Under Construction!|
|:-|
| This is and incomplete work-in-progress.|

After considerable struggles, see [remark lint question](/Tech-Ref/Software-Development/JavaScript/Node.js/unified/remark/remark%2Dcli/remark-lint-question), 

[remark-lint-no-undefined-references](/Tech-Ref/Software-Development/JavaScript/Node.js/unified/remark/remark%2Dlint/remark%2Dlint%2Dno%2Dundefined%2Dreferences)

- :+1: Notes:
   1. For some undetermined reason I keep having to reinstall `remark-lint-no-undefined-references` globally. Otherwise I am getting a run-time error.
      - :new: **Update:** don't install globally. See [remark lint question](/Tech-Ref/Software-Development/JavaScript/Node.js/unified/remark/remark%2Dcli/remark-lint-question).

```dos
remark --use remark-lint-no-undefined-references KM.wiki 2>&1 1>c:\temp\KM.ansi
```
