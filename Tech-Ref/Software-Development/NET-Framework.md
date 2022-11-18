[Home](/Slalom-LLC/Slalom-Consulting) | [Glossary](/Glossary) | [Tech Ref](/Tech-Ref) | [Software Development](/Tech-Ref/Software-Development) 
**Disambiguation:** [Java](/Tech-Ref/Software-Development/Java).

[[_TOC_]]

---
# Introduction
"_The ***.NET Framework*** (pronounced as "dot net") is a software framework developed by Microsoft that runs primarily on Microsoft [Windows](/Tech-Ref/Microsoft/Microsoft-Windows)._"

## Reference
1. [WikipediaL .NET Framework](https://en.wikipedia.org/wiki/.NET_Framework)
1. [Comparison of the .NET and Java platforms](https://en.wikipedia.org/wiki/Comparison_of_the_Java_and_.NET_platforms)
1. [.NET Glossary](https://docs.microsoft.com/en-us/dotnet/standard/glossary)

---
# Topics
1. [Plain Old CLR Object (POCO)](/Tech-Ref/Software-Development/Java/POJO-\(Plain-Old-Java-Object\)/POCO-\(Plain-Old-CLR-Object\)).
1. [Windows](/Tech-Ref/Microsoft/Microsoft-Windows).

---
# Example Uses
1. [Cox Automotive Inc's (CAI)](/Clients/CAI-\(Cox-Automotive-Inc\)):
   - [Title Management System (TMS)](/Clients/CAI-\(Cox-Automotive-Inc\)/Infrastructure-\(CAI\)/Systems-and-Services-\(CAI\)/TMS):
      - [cm.sln](/Clients/CAI-\(Cox-Automotive-Inc\)/Infrastructure-\(CAI\)/Systems-and-Services-\(CAI\)/TMS/cm.sln#third-party-components).

---
# Libraries and Other Tools

## ADO.NET
- [ADO.NET](/Tech-Ref/Software-Development/NET-Framework/ADO.NET).

### Entity Framework (EF)
- [Entity Framework (EF)](/Tech-Ref/Software-Development/NET-Framework/ADO.NET/EF-\(Entity-Framework\)).

## ASP.NET
- [ASP.NET](/Tech-Ref/Software-Development/NET-Framework/ASP.NET).

## Autofac
- [Autofac (.NET)](/Tech-Ref/Software-Development/NET-Framework/Autofac-\(.NET\)).

## C# (CSharp)
- [C#](/Tech-Ref/Software-Development/CSharp). ![programming-sm.png](/.attachments/programming-sm-84511b90-2d77-4364-8b25-7bee99dd4060.png)
- [DomainObjects for .NET](/Tech-Ref/Software-Development/NET-Framework/DomainObjects-for-.NET).

## Castle Project
- [Castle Project](/Tech-Ref/Software-Development/NET-Framework/Castle-Project).

### Castle Core
- [Castle Core](/Tech-Ref/Software-Development/NET-Framework/Castle-Project/Castle-Core).

## DomainObjects for .NET
- [DomainObjects for .NET](/Tech-Ref/Software-Development/NET-Framework/DomainObjects-for-.NET).

## Entity Framework (EF)
- [EF (Entity Framework)](/Tech-Ref/Software-Development/NET-Framework/ADO.NET/EF-\(Entity-Framework\)).

## Json.NET (Newtonsoft.Json)
- [Json.NET (Newtonsoft.Json)](/Tech-Ref/Software-Development/NET-Framework/Json.NET-\(Newtonsoft.Json\)). 

## log4net
- [Apache log4net](/Tech-Ref/Apache-Software-Foundation/Apache-log4net).

## Microsoft.Bcl
- [Microsoft.Bcl](/Tech-Ref/Software-Development/NET-Framework/Microsoft.Bcl).

## Microsoft.Bcl.Build
[Microsoft.Bcl.Build](/Tech-Ref/Software-Development/NET-Framework/Microsoft.Bcl.Build).

## Microsoft Graph
- [Microsoft Graph](/Tech-Ref/Microsoft/Microsoft-Graph).

## Microsoft.Net.Http
- [Microsoft.Net.Http](/Tech-Ref/Software-Development/NET-Framework/Microsoft.Net.Http).

## Microsoft.Web.Infrastructure
- [Microsoft.Web.Infrastructure](/Tech-Ref/Software-Development/NET-Framework/Microsoft.Web.Infrastructure).

## Moq
- [Moq](/Tech-Ref/Software-Development/NET-Framework/Moq).

## SharePoint Online Client Components SDK
- [SharePoint Online Client Components SDK](/Tech-Ref/Microsoft/SharePoint/SharePoint-Online/CSOM-\(SharePoint-Online-Client-Side-Object-Model\)/SharePoint-Online-Client-Components-SDK).

## SharePoint Online Client Side Object Model (CSOM)
- [SharePoint Online Client Side Object Model (CSOM)](/Tech-Ref/Microsoft/SharePoint/SharePoint-Online/CSOM-\(SharePoint-Online-Client-Side-Object-Model\)).

## System.Runtime.CompilerServices.Unsafe
- [System.Runtime.CompilerServices.Unsafe](/Tech-Ref/Software-Development/NET-Framework/System.Runtime.CompilerServices.Unsafe)

---
# Tips and Tricks

## .NET v1.1 not supported on Windows 8 or Above
- The [NET Framework 1.1](/Tech-Ref/Software-Development/NET-Framework) is not supported on [Windows 8](/Tech-Ref/Microsoft/Microsoft-Windows) or above.
   - [Migrate from the .NET Framework 1.1.](https://docs.microsoft.com/en-us/dotnet/framework/migration-guide/migrating-from-the-net-framework-1-1)
   - [Run .NET Framework 1.1 apps on Windows 8, Windows 8.1, or Windows 10.](https://docs.microsoft.com/en-us/dotnet/framework/install/run-net-framework-1-1-apps)

## How to Check Your .NET Framework Version(s)
|:warning: WARNING!|
|:-|
| You MUST use care when working with the [Registry Editor (regedt/regedit)](/Tech-Ref/Microsoft/Microsoft-Windows/Registry-Editor) it is relatively easy to "_brick your system_", i.e. render it inoperative. |

Using the [Registry Editor (regedt/regedit)](/Tech-Ref/Microsoft/Microsoft-Windows/Registry-Editor) inspect hive: `HKEY_LOCAL_MACHINE\Microsoft\NET Framework Setup\NDP`.

- [IBM: How to Determine Which Version of Microsoft .NET Framework Installed](https://www.ibm.com/support/pages/how-determine-which-version-microsoft-net-framework-installed)
- [How to: Determine which .NET Framework versions are installed](https://docs.microsoft.com/en-us/dotnet/framework/migration-guide/how-to-determine-which-versions-are-installed)
