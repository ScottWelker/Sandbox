[Home](/Slalom-LLC/Slalom-Consulting) | [Glossary](/Glossary) | [Tech Ref](/Tech-Ref) | [Software Development](/Tech-Ref/Software-Development) | [Visual Studio](/Tech-Ref/Microsoft/Visual-Studio)
**Disambiguation:** [Project](/Tech-Ref/Microsoft/Visual-Studio/Project-\(Visual-Studio\)).

[[_TOC_]]

# Introduction
"_A ***Solution (.sln)*** is a structure for organizing [projects](/Tech-Ref/Microsoft/Visual-Studio/Project-\(Visual-Studio\)) in [Visual Studio](/Tech-Ref/Microsoft/Visual-Studio)._"

"_The `.sln` file contains text-based information the environment uses to find and load the name-value parameters for the persisted data and the [project](/Tech-Ref/Microsoft/Visual-Studio/Project-\(Visual-Studio\)) VSPackages it references._"

"_Each [project's](/Tech-Ref/Microsoft/Visual-Studio/Project-\(Visual-Studio\)) file contains additional information read by the environment to populate the hierarchy with that [project's](/Tech-Ref/Microsoft/Visual-Studio/Project-\(Visual-Studio\)) items. The hierarchy data persistence is controlled by the [project](/Tech-Ref/Microsoft/Visual-Studio/Project-\(Visual-Studio\)). The data is not normally stored in the `.sln` file, although you can intentionally write [project](/Tech-Ref/Microsoft/Visual-Studio/Project-\(Visual-Studio\)) information to the `.sln` file if you choose to do so._"

## Reference
1. [Docs.Microsoft: Solution (.sln) file](https://docs.microsoft.com/en-us/visualstudio/extensibility/internals/solution-dot-sln-file)

---
# Topics
1. [Project](/Tech-Ref/Microsoft/Visual-Studio/Project-\(Visual-Studio\)). 
1. [Visual Studio](/Tech-Ref/Microsoft/Visual-Studio).
1. [Solution Explorer](/Tech-Ref/Microsoft/Visual-Studio/Solution-Explorer).

---
# Solution File and Format
- [FileFormat: What is SLN file?](https://docs.fileformat.com/programming/sln/)

## Project Declaration
- [FileFormat: SLN file, Project Declaration](https://docs.fileformat.com/programming/sln/#project-declaration)

A solution file can contain more than one projects declaration and that too of difference project types. For example, a single solution file can contain a CSharp as well as a VB.NET project. These types are distinguished in a solution using the Project-Type-GUID. The above project declaration can be generalized as follow for clear understanding.

```
Project("{Project-Type-GUID}") # "Project-Name", "Project-Path.extension", "{Project-GUID}"
```
### Project-Type-GUID
The `Project-Type-GUID` is unique for different project types and is used by the solution reader to identify the type of project. In this case, F184B08F-C81C-45F6-A57F-5ABD9991F28F shows that it is a VB.NET project.

#### Listing (Project Types & GUIDs)
<details>
   <summary>Click to expand/collapse listing.</summary>

- **11/01/2021 [SWelker](/Individuals/Scott-Welker):** Found this reference but I haven't really consumed it: 
   - [Cake: ProjectTypes](https://cakebuild.net/api/Cake.Incubator.Project/ProjectTypes/)
- **11/01/2021 [SWelker](/Individuals/Scott-Welker):** Additional project types found here:
   - https://newbedev.com/visual-studio-project-type-guids
- [CodeProject: List of Visual Studio Project Type GUIDs](https://www.codeproject.com/Reference/720512/List-of-Visual-Studio-Project-Type-GUIDs)

| Project Type												| Project Type GUID									 |
|:-|:-|
| ASP.NET 5                                      | 8BB2217D-0F2D-49D1-97BC-3654ED321F3B |
| ASP.NET MVC 1                                  | 603C0E0B-DB56-11DC-BE95-000D561079B0 |
| ASP.NET MVC 2                                  | F85E285D-A4E0-4152-9332-AB1D724D3325 |
| ASP.NET MVC 3                                  | E53F8FEA-EAE0-44A6-8774-FFD645390401 |
| ASP.NET MVC 4                                  | E3E379DF-F4C6-4180-9B81-6769533ABE47 |
| ASP.NET MVC 5                                  | 349C5851-65DF-11DA-9384-00065B846F21 |
| [C#](/Tech-Ref/Microsoft/Visual-Studio/Solution-File-\(.sln\)/CSharp-Project)                                             | FAE04EC0-301F-11D3-BF4B-00C04F79EFBC |
| [C# (forces use of SDK project system)](/Tech-Ref/Microsoft/Visual-Studio/Solution-File-\(.sln\)/CSharp-SDK-Project-System)<br/><br/>:warning: [Cake: ProjectTypes](https://cakebuild.net/api/Cake.Incubator.Project/ProjectTypes/) lists as [.NET Core](/Tech-Ref/Software-Development/NET-Framework) | 9A19103F-16F7-4668-BE54-9A1E7A4F7556 |
| C++                                            | 8BC9CEB8-8B4A-11D0-8D11-00A0C91BC942 |
| CPS barebones project                          | 13B669BE-BB05-4DDF-9536-439F39A36129 |
| Database                                       | A9ACE9BB-CECE-4E62-9AA4-C7E7C5BD2124 |
| Database                                       | C8D11400-126E-41CD-887F-60BD40844F9E |
| Database (other project types)                 | 4F174C21-8C12-11D0-8340-0000F80270F8 |
| Deployment Cab                                 | 3EA9E505-35AC-4774-B492-AD1749C4943A |
| Deployment Merge Module                        | 06A35CCD-C46D-44D5-987B-CF40FF872267 |
| Deployment Setup                               | 978C614F-708E-4E1A-B201-565925725DBA |
| Deployment Smart Device Cab                    | AB322303-2255-48EF-A496-5904EB18DA55 |
| Distributed System                             | F135691A-BF7E-435D-8960-F99683D2D49C |
| Dynamics 2012 AX C# in AOT                     | BF6F8E12-879D-49E7-ADF0-5503146B24B8 |
| Extensibility                                  | 82B43B9B-A64C-4715-B499-D71E9CA2BD60 |
| F#                                             | F2A71F9B-5D33-465A-A702-920D77279786 |
| F# (forces use of SDK project system)          | 6EC3EE1D-3C4E-46DD-8F32-0CC8E7565705 |
| IL project                                     | 95DFC527-4DC1-495E-97D7-E94EE1F7140D |
| J#                                             | E6FDF86B-F3D1-11D4-8576-0002A516ECE8 |
| JScript                                        | 262852C6-CD72-467D-83FE-5EEB1973A190 |
| Legacy (2003) Smart Device (C#)                | 20D4826A-C6FA-45DB-90F4-C717570B9F32 |
| Legacy (2003) Smart Device (VB.NET)            | CB4CE8C6-1BDB-4DC7-A4D3-65A1999772F8 |
| LightSwitch                                    | 8BB0C5E8-0616-4F60-8E55-A43933E57E9C |
| LightSwitch Project                            | 581633EB-B896-402F-8E60-36F3DA191C85 |
| Micro Framework                                | b69e3092-b931-443c-abe7-7e7b65f2a37f |
| Model-View-Controller v2 (MVC 2)               | F85E285D-A4E0-4152-9332-AB1D724D3325 |
| Model-View-Controller v3 (MVC 3)               | E53F8FEA-EAE0-44A6-8774-FFD645390401 |
| Model-View-Controller v4 (MVC 4)               | E3E379DF-F4C6-4180-9B81-6769533ABE47 |
| Model-View-Controller v5 (MVC 5)               | 349C5851-65DF-11DA-9384-00065B846F21 |
| Mono for Android                               | EFBA0AD7-5A72-4C68-AF49-83D382785DCF |
| MonoTouch                                      | 6BC8ED88-2882-458C-8E55-DFD12B67127B |
| MonoTouch Binding                              | F5B4F3BC-B597-4E2B-B552-EF5D8A32436F |
| Office/SharePoint App                          | C1CDDADD-2546-481F-9697-4EA41081F2FC |
| Portable Class Library                         | 786C830F-07A1-408B-BD7F-6EE04809D6DB |
| Project Folders                                | 66A26720-8FB5-11D2-AA7E-00C04F688DDE |
| Shared Project                                 | D954291E-2A0B-460D-934E-DC6B0785DB48 |
| SharePoint (C#)                                | 593B0543-81F6-4436-BA1E-4747859CAAE2 |
| SharePoint (VB.NET)                            | EC05E597-79D4-47f3-ADA0-324C4F7C7484 |
| SharePoint Workflow                            | F8810EC1-6754-47FC-A15F-DFABD2E3FA90 |
| Silverlight                                    | A1591282-1198-4647-A2B1-27E5FF5F6F3B |
| Smart Device (C#)                              | 4D628B5B-2FBC-4AA6-8C16-197242AEB884 |
| Smart Device (VB.NET)                          | 68B1623D-7FB9-47D8-8664-7ECEA3297D4F |
| [Solution Folder](/Tech-Ref/Microsoft/Visual-Studio/Solution-File-\(.sln\)/Solution-Folder)                                | 2150E333-8FDC-42A3-9474-1A3956D46DE8 |
| Test                                           | 3AC096D0-A1C2-E12C-1390-A8335801FDAB |
| Universal Windows Class Library                | A5A43C5B-DE2A-4C0C-9213-0A381AF9435A |
| VB.NET                                         | F184B08F-C81C-45F6-A57F-5ABD9991F28F |
| VB.NET (forces use of SDK project system)      | 778DAE3C-4631-46EA-AA77-85C1314464D9 |
| Visual Database Tools                          | C252FEB5-A946-4202-B1D4-9916A0590387 |
| Visual Studio 2015 Installer Project Extension | 54435603-DBB4-11D2-8724-00A0C9A8B90C |
| Visual Studio Tools for Applications (VSTA)    | A860303F-1F3F-4691-B57E-529FC101A107 |
| Visual Studio Tools for Office (VSTO)          | BAA0C2D2-18E2-41B9-852F-F413020CAA33 |
| Web Application                                | 349C5851-65DF-11DA-9384-00065B846F21 |
| Web Deployment                                 | 2CFEAB61-6A3B-4EB8-B523-560B4BEEF521 |
| Web Site                                       | E24C65DC-7377-472B-9ABA-BC803B73C61A |
| Windows (C#)                                   | FAE04EC0-301F-11D3-BF4B-00C04F79EFBC |
| Windows (VB.NET)                               | F184B08F-C81C-45F6-A57F-5ABD9991F28F |
| Windows (Visual C++)                           | 8BC9CEB8-8B4A-11D0-8D11-00A0C91BC942 |
| Windows Communication Foundation (WCF)         | 3D9AD99F-2412-4246-B90B-4EAA41C64699 |
| Windows Phone 8/8.1 App (C#)                   | C089C8C0-30E0-4E22-80C0-CE093F111A43 |
| Windows Phone 8/8.1 App (VB.NET)               | DB03555F-0C8B-43BE-9FF9-57896B3C5E56 |
| Windows Phone 8/8.1 Blank/Hub/Webview App      | 76F1466A-8B6D-4E39-A767-685A06062A39 |
| Windows Presentation Foundation (WPF)          | 60DC8134-EBA5-43B8-BCC9-BB4BC16C2548 |
| Windows Store (Metro) Apps & Components        | BC8A1FFA-BEE3-4634-8014-F334798102B3 |
| Windows Store App Universal                    | D954291E-2A0B-460D-934E-DC6B0785DB48 |
| WiX Setup                                      | 930C7802-8A8C-48F9-8165-68863BCCD9DD |
| Workflow (C#)                                  | 14822709-B5A1-4724-98CA-57A101D1B079 |
| Workflow (VB.NET)                              | D59BE175-2ED0-4C54-BE3D-CDAA9F3214C8 |
| Workflow Foundation                            | 32F31D43-81CC-4C15-9DE6-3FC5453562B6 |
| Xamarin.Android                                | EFBA0AD7-5A72-4C68-AF49-83D382785DCF |
| Xamarin.iOS                                    | 6BC8ED88-2882-458C-8E55-DFD12B67127B |
| XNA (Windows)                                  | 6D335F3A-9D43-41b4-9D22-F6F17C4BE596 |
| XNA (XBox)                                     | 2DF5C3F4-5A5F-47a9-8E94-23B4456F55E2 |
| XNA (Zune)                                     | D399B71A-8929-442a-A9AC-8BEC78BB2433 |

</details>

### Project Name
- [TBD (To Be Determined)](/Glossary/TBD-\(To-Be-Determined\)).

### Project Path.extension
- [TBD (To Be Determined)](/Glossary/TBD-\(To-Be-Determined\)).

### Project GUID
The unique GUID of the project that differentiates it from other projects in the solution. The unique ID of a project in the solution makes it possible for other projects in the solution to access it.

Based on the information contained in the project section of the .sln file, the environment loads each project file. The project itself is then responsible for populating the project hierarchy and loading any nested projects. Any changes made to the solution are saved back to the solution file upon saving or closing the project.
