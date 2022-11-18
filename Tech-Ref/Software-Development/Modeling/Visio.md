[Home](/Slalom-LLC/Slalom-Consulting) | [Glossary](/Glossary) | [Tech Ref](/Tech-Ref) | [Software Development](/Tech-Ref/Software-Development) | [DevOps](/Tech-Ref/Software-Development/DevOps-\(Development-and-IT-Operations\)) | [Modeling](/Tech-Ref/Software-Development/Modeling)

[[_TOC_]]

---
# Introduction
| :warning: CAUTION! |
|:-|
| Unless noted otherwise this information pertains to **Visio 2201 (Build 14827.20192)**, as seen in `File`\| `Account` , `Product Information`, `About Visio`. |

"_Microsoft ***Visio***  is a diagramming and vector graphics application and is part of the Microsoft Office family._"

## Reference
1. [Wikipedia: Microsoft Visio](https://en.wikipedia.org/wiki/Microsoft_Visio)

---
# Topics
1. [Modeling](/Slalom-LLC/Slalom-Consulting/Modeling-\(Slalom\)).

---
# Tips and Tricks

## Diagram Specific Tips

### Use Case Diagram

#### Change Connector Arrows
- [Can't change connector Begin Arrow or End Arrow](https://answers.microsoft.com/en-us/msoffice/forum/all/cant-change-connector-begin-arrow-or-end-arrow-in/477ecf82-c260-4028-81fe-01472e26dccf)
   1. Enable [Enable Developer Mode](#enable-developer-mode).
   1. Right Click the Connector  (or 'Association' object).
      - Select `Show ShapeSheet`.
      - Scroll down to the `Line Format` section.
      - Change the fields `BeginArrow`, `BeginArrowSize`, `EndArrow`, and/or `EndArrowSize` as needed.
         - The `guard(0)` function is what is preventing you from making the change.
      - [I (SWelker)](/Individuals/Scott-Welker) generally just change `EndArrow` to `13` from `=GUARD(0)` for a _normal_ filled arrowhead.

## General Diagramming Tips

### Fix Connector Line Pattern
- Using the same basic fix as [Fix Shape Text Obscured by Connector Line]() below, change the `LinePattern`.
   - Values from \[`3`..`9`\] give various dashed lines. 

### Fix Shape Text Obscured by Connector Line
- This tip is derived from [SuperUser: Draw a line in Visio between objects without obscuring the text in the label](https://superuser.com/questions/773902/draw-a-line-in-visio-between-objects-without-obscuring-the-text-in-the-label). However the steps didn't match `Visio 2201`.
   1. Select the shape and right-click, `Edit Text`.
   1. Right click within the resulting selected text and select `Paragraph`.
   1. In the resulting `Text` dialog, select the `Text Block` tab.
   1. Within tab's `Text Background` section, select `Solid color:`
      - Use the color dropdown to change the color to your desired background color, e.g. `white, white`.
   1. You may also need to select the connector line and `Send to Back`, `Send backward`.

## Enable Developer Mode
- `File` | `Options`, `Advanced`, Scroll all the way down to `General`, Select `Run in developer mode`.

## Fix Shape Search (Visio 2201 & Windows 11)
- [Fixing Shape Search in the Visio desktop app on Windows 11](https://support.microsoft.com/en-us/office/use-the-shapes-window-to-organize-and-find-shapes-2e468457-1059-49d3-8955-32b2527cce98):
   1. Open registry editor (`regedit.exe`).
   1. In the tree view on the left, navigate to `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows Search\PluginResourceData\{FAEA5B46-761B-400E-B53E-E805A97A543E}`.
   1. Double-click the `PenaltyBox` element to edit it. Set `Value data` to `0`, then select OK.
   1. On the taskbar, select Search The Search ![image.png](/.attachments/image-832039ad-a4b9-41f9-b027-adeec63379ce.png) icon on the taskbar in Windows 11., then enter `Indexing Options` in the search box. Under `Best Match`, select the `Indexing Options` control panel.
   1. In the `Indexing Options` dialog box, select `Advanced`. Then, under Troubleshooting, select `Rebuild`.
   1. Once indexing is complete, Shape search should start working properly again.

## Format Date/Time
- `Insert`, `Field` ![image.png](/.attachments/image-ef128113-586d-4dfa-bc06-544db1bc079a.png), 
   - `Date/Time`
   - `Last Edit Date/Time`
   - `Data Format`:  `{{M/d/yyyy h:m am/pm}}`

## Open Stencil

- ![image.png](/.attachments/image-f11955eb-8bb7-472c-a9c0-f4d637a24689.png)
