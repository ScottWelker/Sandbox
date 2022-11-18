[Home](/Slalom-LLC/Slalom-Consulting) | [Glossary](/Glossary) | [Tech Ref](/Tech-Ref) | [Modeling](/Tech-Ref/Software-Development/Modeling) | [Mermaid](/Tech-Ref/Software-Development/Modeling/Mermaid) | [Modeling (Slalom)](/Slalom-LLC/Slalom-Consulting/Modeling-\(Slalom\))
**Disambiguation:** [How We Work (Slalom)](/Slalom-LLC/Slalom-Consulting/Terms-\(Slalom-Consulting\)/HWW-\(How-We-Work\)), [Balsamiq](/Tech-Ref/Software-Development/Modeling/Balsamiq), [Visio](/Tech-Ref/Software-Development/Modeling/Visio).

[[_TOC_]]

---
# Introduction
|:+1: Update!|
|:-|
|**11/06/2022:** [DeveloperCommunity: Finally other diagrams are supported](https://developercommunity.visualstudio.com/t/Mermaid-support-for-class-diagrams-and-s/883356#T-N10191758).<ul><li>**:new: [Class Diagram](https://mermaid-js.github.io/mermaid/#/classDiagram) added ([Markdown syntax for wikis](https://learn.microsoft.com/en-us/azure/devops/project/wiki/wiki-markdown-guidance?view=azure-devops)).**</ul>|
| **[02/28/2022 Microsoft:](https://docs.microsoft.com/en-us/azure/devops/release-notes/2022/sprint-200-update#support-for-additional-diagram-types-in-wiki-pages):** We have upgraded the version of mermaid charts used in wiki pages to **8.13.9**. With this upgrade, you can now include the following diagrams and visualizations in your Azure DevOps wiki pages:
<ol><li>[Flowcharts](#flowcharts)</li><li>[Sequence diagrams](#sequence-diagrams)</li><li>[Gantt charts](#gantt-charts)</li><li>:new:**[Pie charts](https://mermaid-js.github.io/mermaid/#/pie)**</li><li>**:new:[Requirement diagrams](https://mermaid-js.github.io/mermaid/#/requirementDiagram)**</li><li>**:new:[State diagrams](https://mermaid-js.github.io/mermaid/#/stateDiagram)**</li><li>**:new:[User Journey](https://mermaid-js.github.io/mermaid/#/user-journey)**</li></ol>|

This page begins to collect information specific the [Azure DevOps Wiki (ADO Wiki)](/Tech-Ref/Microsoft/Microsoft-Azure/ADO-\(Azure-DevOps\)/Wiki-\(Azure-DevOps\)) implementation of [Mermaid](/Tech-Ref/Software-Development/Modeling/Mermaid). 

---
# Topics
1. [Mermaid](/Tech-Ref/Software-Development/Modeling/Mermaid).
1. [Modeling](/Slalom-LLC/Slalom-Consulting/Modeling-\(Slalom\)).

---
# Tips and Tricks

## Supported Diagrams
- :+1: See the noted update in the [Introduction](#Introduction) above. This section does not yet reflect those additional supported diagrams.

As of 02/2022 only a small number of the [Mermaid's](/Tech-Ref/Software-Development/Modeling/Mermaid) diagrams are supported by the [Azure DevOps Wiki](/Tech-Ref/Microsoft/Microsoft-Azure/ADO-\(Azure-DevOps\)/Wiki-\(Azure-DevOps\)) implementation 
- [#10956 'Add Mermaid diagrams to a Wiki page' links to incorrect Mermaid documentation.](https://github.com/MicrosoftDocs/azure-devops-docs/issues/10956)
- [StackOverflow: erDiagram is not presently supported.](https://stackoverflow.com/a/67696918/418950)

### Gantt Charts
- [Mermaid Gantt Chart](https://mermaid-js.github.io/mermaid/#/gantt)

### Flowcharts
- [Mermaid Flowchart](https://mermaid-js.github.io/mermaid/#/flowchart)

#### Example(s)
- [DocForm Client Wrapper, Exercise Print Pull Report (Letter)](/Clients/CAI-\(Cox-Automotive-Inc\)/Infrastructure-\(CAI\)/Systems-and-Services-\(CAI\)/DocForm-\(CAI-%2D-TMS\)/DocForm-Client-Wrapper#exercise-print-pull-report-(letter)).

### Sequence diagrams
- [Mermaid Sequence Diagrams](https://mermaid-js.github.io/mermaid/#/sequenceDiagram)
- :+1: [I (SWelker)](/Individuals/Scott-Welker) recommend you use [PlantUML](/Tech-Ref/Software-Development/Modeling/PlantUML) for all but the simplest of sequence diagrams. ADO Wiki's [Mermaid](/Tech-Ref/Software-Development/Modeling/Mermaid) implementation is well behind the current release and it's impractical to create worthwhile sequence diagrams.

#### Example(s)
- [Decoupling TMS & Letter Teams, 52:12 Scenario to Ensure We've Addressed](/Clients/CAI-\(Cox-Automotive-Inc\)/Infrastructure-\(CAI\)/Systems-and-Services-\(CAI\)/DocForm-\(CAI-%2D-TMS\)/Decoupling-TMS-&-Letters-Teams#52%3A12-scenario-to-ensure-we%27ve-addressed)

#### No Participant as 'Actor'
- Specifying the "_Participant_" as an actor doesn't work, e.g. `actor <participantName>`. Oddly you can explicitly specify the "_Participant_" as (presumably an ordered) participant, e.g. `participant <participantName>`.

#### No Line Breaks in Participant Name
- None of the customary line break techniques seem to be supported within the "_participants_" name, `<br/>`, `<br>`, or `\n`.

## Too Much Leading and Trailing Whitespace
|:warning: CAUTION!|
|:-|
| The [Before diagram](#before) is not exhibiting this issue anymore, except while in edit/preview. The issue may have been addressed. |
| **02/17/2022 [SWelker](/Individuals/Scott-Welker):** This issue remains for (at least) [Sequence Diagrams](#sequence-diagrams). However, this fix doesn't work with [Sequence Diagrams](#sequence-diagrams). |

- [Adjust mermaid diagram white space in Azure devops wiki](https://stackoverflow.com/a/70763225/418950)

### Before
<details><summary>Click to Show/Hide Diagram.</summary>

::: mermaid
graph TD
A[Author sends a review to the customer success email] -->|Dynamics 365 creates a review case based on the Knowledge Base Article Review Template| B[[Automation]]
B --> D[D365 creates a review case based on the Knowledge Base Article Review Template]
B --> E[D365 places the review article in the Article Review Queue]
D -->F[Dynamics 365 creates a review case based on the Knowledge Base Article Review Template]
E -->F[A customer success agent assigns themself as the owner for the article]
F -->G[[D365 sends a notification of the new owner to the TDT email]]
G -->H[In Madcap Central, the Flare author reassigns article review from the cus success email to the assigned Owner for the review case]
H -->I[Agent completes review in Madcap Central and submit it to Flare Author]
I -->J[Agent closes the review case in D365]
J -->K[Flare author receives notification of returned review via Madcap Central email]
K -->L[Flare author implements changes in Flare and accepts the file]
L -->M[Flare author synchronizes project with source control]
:::

</details>

### After (Fix)
<details><summary>Click to Show/Hide Diagram.</summary>

Edit the page to see the source line (\#3) that works-around the issue.
::: mermaid
graph TD
%%{init: {"flowchart": { "useMaxWidth": false } }}%%
A[Author sends a review to the customer success email] -->|Dynamics 365 creates a review case based on the Knowledge Base Article Review Template| B[[Automation]]
B --> D[D365 creates a review case based on the Knowledge Base Article Review Template]
B --> E[D365 places the review article in the Article Review Queue]
D -->F[Dynamics 365 creates a review case based on the Knowledge Base Article Review Template]
E -->F[A customer success agent assigns themself as the owner for the article]
F -->G[[D365 sends a notification of the new owner to the TDT email]]
G -->H[In Madcap Central, the Flare author reassigns article review from the cus success email to the assigned Owner for the review case]
H -->I[Agent completes review in Madcap Central and submit it to Flare Author]
I -->J[Agent closes the review case in D365]
J -->K[Flare author receives notification of returned review via Madcap Central email]
K -->L[Flare author implements changes in Flare and accepts the file]
L -->M[Flare author synchronizes project with source control]
:::

</details>