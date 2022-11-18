[Home](/Slalom-LLC/Slalom-Consulting) | [Glossary](/Glossary) | [Tech Ref](/Tech-Ref) | [Software Development](/Tech-Ref/Software-Development) | [Scripting](/Tech-Ref/Software-Development/Scripting) | [DevOps](/Tech-Ref/Software-Development/DevOps-\(Development-and-IT-Operations\))
**Disambiguation:** [Scripting](/Tech-Ref/Software-Development/Scripting).
**AKA:** PS.

[[_TOC_]]

---
# Introduction
|:+1: 07/2021 Tip!|
|:-|
| **There are currently two versions of PowerShell:** a classic `Windows PowerShell` (the latest version is 5.1 and it is _no longer developed_) and a new `PowerShell Core` platform (version 7.1 is available now). Despite that PowerShell version numbering goes on from 5.1 (6.0, 6.1, 7.0, 7.1, etc.), these are two different products. -- http://woshub.com/install-update-powershell-windows/<br/><br/> From the command line: <ul><li>`pwsh` <mark>launches the PowerShell Core interpreter, v7.x.</mark></li><li>`PowerShell` <mark>launches the Windows PowerShell interpreter, v5.1.x.</mark></li></ul> |


"_***PowerShell*** is a task automation and configuration management framework from Microsoft, consisting of a command-line shell and the associated scripting language. Initially a [Windows](/Tech-Ref/Microsoft/Microsoft-Windows) component only, known as _Windows PowerShell_, it was made open-source and cross-platform on 18 August 2016 with the introduction of PowerShell Core. The former is built on the [.NET Framework](/Tech-Ref/Software-Development/NET-Framework), the latter on [.NET Core](/Tech-Ref/Software-Development/NET-Framework/NET-Core)._"

"_In PowerShell, administrative tasks are generally performed by cmdlets (pronounced command-lets), which are specialized [.NET](/Tech-Ref/Software-Development/NET-Framework) classes implementing a particular operation. These work by accessing data in different data stores, like the file system or registry, which are made available to PowerShell via providers. Third-party developers can add cmdlets and providers to PowerShell. Cmdlets may be used by scripts and scripts may be packaged into [modules](#Modules)._"

"_PowerShell provides full access to [COM](/Glossary/COM-\(Component-Object-Model\)) and [WMI](/Glossary/WMI-\(Windows-Management-Instrumentation\)), enabling administrators to perform administrative tasks on both local and remote [Windows](/Tech-Ref/Microsoft/Microsoft-Windows) systems as well as :seedling:WS-Management and :seedling:CIM enabling management of remote [Linux](/Tech-Ref/Linux) systems and network devices. PowerShell also provides a hosting API with which the PowerShell runtime can be embedded inside other applications._"

## Reference
1. [Wikipedia: PowerShell](https://en.wikipedia.org/wiki/PowerShell)

---
# Topics

## From Other Wiki Pages
1. [.NET Framework](/Tech-Ref/Software-Development/NET-Framework).
1. [Azure DevOps REST API](/Tech-Ref/Microsoft/Microsoft-Azure/ADO-\(Azure-DevOps\)/Azure-DevOps-REST-API).
1. [CSOM (SharePoint Online Client Side Object Model)](/Tech-Ref/Microsoft/SharePoint/SharePoint-Online/CSOM-\(SharePoint-Online-Client-Side-Object-Model\)).
1. [PowerShell Gallery](/Tech-Ref/Microsoft/PowerShell/PowerShell-Gallery).
1. [Windows](/Tech-Ref/Microsoft/Microsoft-Windows).
1. [Microsoft Graph](/Tech-Ref/Microsoft/Microsoft-Graph).

## Modules
A module is a package that contains PowerShell members, such as cmdlets, providers, functions, workflows, variables, and aliases.

Here are modules about which [Slalom](/Slalom-LLC/Slalom-Consulting) has some notes.

### Azure AD Module
- [Azure AD Module](/Tech-Ref/Microsoft/Microsoft-Azure/AAD-\(Azure-Active-Directory\)/Azure-AD-Connect/Azure-AD-Module).

### PowerShellGet Module
- [PowerShellGet](/Tech-Ref/Microsoft/PowerShell/PowerShellGet).

### PSDocs (create .md files)
- https://github.com/microsoft/PSDocs
   - `Install-Module -Name PSDocs -Scope CurrentUser`

## cmdlets
"_**cmdlets** (pronounced command-lets) are specialized [.NET](/Tech-Ref/Software-Development/NET-Framework) classes implementing a particular operation. These work by accessing data in different data stores, like the file system or registry, which are made available to PowerShell via [providers](#Providers). Third-party developers can add cmdlets and [providers](#Providers) to PowerShell. Cmdlets may be used by scripts, which may in turn be packaged into [modules](#Modules)._"

## Providers
"_[Cmdlets](#cmdlets) can use [.NET](/Tech-Ref/Software-Development/NET-Framework) data access APIs directly or use the PowerShell infrastructure of **PowerShell Providers**, which make data stores addressable using unique paths_"

---
# Tips and Tricks

## Bypass Execution Policy
- [StackOverflow: Bypass Execution Policy](https://stackoverflow.com/a/9167524/418950)

```powershell
powershell -ExecutionPolicy Bypass ./script.ps1
```

## Creating Azure DevOps Wiki Pages from within a Pipeline
- [Creating Azure DevOps WIKI Pages from within a pipeline](https://stefanstranger.github.io/2020/04/12/CreatingAzureDevOpsWIKIPagesFromWithApipeline/)

## Could not find a part of the path
- See [Maximum Path Length Limitation](#maximum-path-length-limitation). This is often the culprit.

## Floating-Point Arithmetic
- [Floating Point Arithmetic](/Tech-Ref/Software-Development/Floating%2DPoint-Arithmetic).

## Maximum Path Length Limitation
- [Maximum Path Length Limitation](https://docs.microsoft.com/en-us/windows/win32/fileio/naming-a-file#maximum-path-length-limitation)

The following registry key must exist and be set to 1 (reboot recommended):
```
Computer\HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\FileSystem\LongPathsEnabled (Type: REG_DWORD) 
```

## Parse a Comma-Delimited CSV Text File
- [PowerShell Import-CSV Cmdlet: Parse a Comma-Delimited CSV Text File](https://petri.com/powershell-import-csv-cmdlet-parse-comma-delimited-csv-text-file)

## PowerShell (Core) and Markdown
- [PowerShell (Core) and Markdown](https://ephos.github.io/posts/2018-8-1-PowerShell-Markdown)
