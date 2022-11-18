[Home](/Slalom-LLC/Slalom-Consulting) | [Glossary](/Glossary) | [Tech Ref](/Tech-Ref) | [Software Development](/Tech-Ref/Software-Development) | [DevOps](/Tech-Ref/Software-Development/DevOps-\(Development-and-IT-Operations\)) | [Modeling](/Tech-Ref/Software-Development/Modeling) | [IDE](/Tech-Ref/Software-Development/IDE-\(Integrated-Development-Environment\))
**Disambiguation:** [Visual Studio Code (VS Code)](/Tech-Ref/Microsoft/Visual-Studio/VS-Code-\(Visual-Studio-Code\)).

[[_TOC_]]

# Introduction
"_Microsoft ***Visual Studio*** is an [integrated development environment (IDE)](/Tech-Ref/Software-Development/IDE-\(Integrated-Development-Environment\)) from [Microsoft](/Tech-Ref/Microsoft). It is used to develop computer programs, as well as [websites](/Tech-Ref/WWW-\(World-Wide-Web\)/Web-Site), [web apps](/Tech-Ref/WWW-\(World-Wide-Web\)/Web-Application), [web services](/Tech-Ref/WWW-\(World-Wide-Web\)/Web-Service) and [mobile apps](/Tech-Ref/Software-Development/UX-\(User-Experience\)/Mobile-App-\(Mobile-Application\))._"

## Reference
1. [Wikipedia: Microsoft Visual Studio](https://en.wikipedia.org/wiki/Microsoft_Visual_Studio)
1. [Visual Studio: Analyze and model your architecture](https://docs.microsoft.com/en-us/visualstudio/modeling/analyze-and-model-your-architecture?view=vs-2022)

---
# Topics
1. [C#](/Tech-Ref/Software-Development/CSharp) ![programming-sm.png](/.attachments/programming-sm-84511b90-2d77-4364-8b25-7bee99dd4060.png).
1. [How We Work (HWW)](/Slalom-LLC/Slalom-Consulting/Terms-\(Slalom-Consulting\)/HWW-\(How-We-Work\)).
1. [Integrated Development Environment (IDE)](/Tech-Ref/Software-Development/IDE-\(Integrated-Development-Environment\)).
1. [Mobile Application](/Tech-Ref/Software-Development/UX-\(User-Experience\)/Mobile-App-\(Mobile-Application\)).
1. [Modeling](/Slalom-LLC/Slalom-Consulting/Modeling-\(Slalom\)).
1. [NuGet](/Tech-Ref/Microsoft/Microsoft-Windows/NuGet).
1. [Project](/Tech-Ref/Microsoft/Visual-Studio/Project-\(Visual-Studio\)). 
1. [Solution Explorer](/Tech-Ref/Microsoft/Visual-Studio/Solution-Explorer).
1. [Solution File (.sln)](/Tech-Ref/Microsoft/Visual-Studio/Solution-File-\(.sln\)).
1. [Solution Folder](/Tech-Ref/Microsoft/Visual-Studio/Solution-File-\(.sln\)/Solution-Folder).
1. [Visual Studio 2017](/Tech-Ref/Microsoft/Visual-Studio/Visual-Studio-2017).
1. [Visual Studio 2019 Community Edition](/Tech-Ref/Microsoft/Visual-Studio/Visual-Studio-2019-Community-Edition).
1. [Visual Studio Code (VS Code)](/Tech-Ref/Microsoft/Visual-Studio/VS-Code-\(Visual-Studio-Code\)).
1. [Web Site](/Tech-Ref/WWW-\(World-Wide-Web\)/Web-Site).
1. [Web Application](/Tech-Ref/WWW-\(World-Wide-Web\)/Web-Application).
1. [Web Service](/Tech-Ref/WWW-\(World-Wide-Web\)/Web-Service).

---
# Tips and Tricks

## Create an Empty Solution
- [Docs.Microsoft: Working with Visual Studio projects and solutions, Create Empty Solutions](https://docs.microsoft.com/en-us/visualstudio/ide/creating-solutions-and-projects?view=vs-2022#create-empty-solutions)
- [Stackoverflow: ](https://stackoverflow.com/a/3345762/418950)

### Steps
1. On the menu bar, select `File` > `New` > `Project`.
1. On the `New Project` page, type `solution` into the search box.
1. Select the `Blank Solution`, and then Enter `Name` and `Location` values for your solution, and then press `OK`.

After you create an empty solution, you can add new or existing projects or items to it by choosing Add New Item or Add Existing Item on the Project menu.

## Create an XML Schema from an XML Document
- [Create an XML schema from an XML document](https://docs.microsoft.com/en-us/visualstudio/xml-tools/how-to-create-an-xml-schema-from-an-xml-document)

## PlantUml Language Service
- [PlantUml Language Service](/Tech-Ref/Microsoft/Visual-Studio/PlantUml-Language-Service).

## Region Directive
Not all languages support this. At least [C# (CSharp)](/Tech-Ref/Software-Development/CSharp) supports it. However, some consider its use or overuse to be a "[code smell](https://en.wikipedia.org/wiki/Code_smell)".
- [Defining regions, Preprocessor Directive](https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/preprocessor-directives#defining-regions)

## Search for File Name in Visual Studio
`Ctrl` + `,`
- [StackOverflow: How to search for file names in Visual Studio?](https://stackoverflow.com/a/18728804/418950)

## Show Currently Active File in Visual Studio Solution Explorer
- [StackOverflow: Forcing the Solution Explorer to select the file in the editor](https://stackoverflow.com/questions/31163/forcing-the-solution-explorer-to-select-the-file-in-the-editor-in-visual-studio)
- https://mattferderer.com/show-current-active-file-in-vs-studio-explorer
   - **Tools** | **Options** | **Projects and Solutions**, check `Track Active Item in Solution Explorer`.
- ![image.png](/.attachments/image-d7a1176a-d21f-428f-8dae-c52f6c1d7a1d.png)

## Dependency Validation
- [Dependency Validation](/Tech-Ref/Microsoft/Visual-Studio/Dependency-Validation-\(Visual-Studio\))