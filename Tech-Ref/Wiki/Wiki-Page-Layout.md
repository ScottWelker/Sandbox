[Home](/Slalom-LLC/Slalom-Consulting) | [Glossary](/Glossary) | [Tech Ref](/Tech-Ref) | [Wiki](/Tech-Ref/Wiki) | [Wiki Gardening](/Tech-Ref/Wiki/Wiki-Gardening)

[[_TOC_]]

---
# Introduction
The image below illustrated a suggested page layout. It was created for [Confluence](/Tech-Ref/Atlassian/Confluence) but can be readily adapted to most any [Wiki Engine](/Tech-Ref/Wiki).

![WikiPageLayout.png](/.attachments/WikiPageLayout-b0edd796-d32b-4252-b798-3a84b3471989.png)

---
# Topics
1. [Azure DevOps Wiki](/Tech-Ref/Microsoft/Microsoft-Azure/ADO-\(Azure-DevOps\)/Wiki-\(Azure-DevOps\)).
1. [Linkify](/Tech-Ref/Wiki/Linkify).
1. [Wiki Gardening](/Tech-Ref/Wiki/Wiki-Gardening).

---
# Tips and Tricks

## Tagging, Labeling, or Categories
|:warning: Warning!|
|:-|
| The [Azure DevOps Wiki](/Tech-Ref/Microsoft/Microsoft-Azure/ADO-\(Azure-DevOps\)/Wiki-\(Azure-DevOps\)) engine underling this [Wiki](/Tech-Ref/Wiki) does not support page categorization (tagging/labeling). |

If the hosting Wiki engine has adequate support for “taging” - sometimes termed labels or categories - it might be possible to make the major sections’ content dynamic, eliminating the need for active curation. For example, using [Confluence](/Tech-Ref/Atlassian/Confluence) page “labels” in conjunction with its `Content by Label` macro and a label naming scheme.

### Example
Using the aforementioned [Confluence](/Tech-Ref/Atlassian/Confluence) example, properly labeling pages enables other pages’ to employ “major section” `Content by Label` macros that automatically list the labeled content, eliminating the need to manually curate.
   - **Label Naming Convention:** `<topic or pageName><majorSection>`

So, if this page was a [Confluence](/Tech-Ref/Atlassian/Confluence) page, we’d have `Content by Label` macros in both the **Topics** and **Tips and Tricks** sections. Their corresponding, respective page labels might be `WikiPageLayoutTopic` and `WikiPageLayoutTip`. This enables any [Wiki Gardener](/Tech-Ref/Wiki/Wiki-Gardening) to cause a page to be listed here in the appropriate section just by applying the correct label.
