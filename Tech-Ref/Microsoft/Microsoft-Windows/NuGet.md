[Home](/Slalom-LLC/Slalom-Consulting) | [Glossary](/Glossary) | [Tech Ref](/Tech-Ref) | [Windows](/Tech-Ref/Microsoft/Microsoft-Windows)
**Disambiguation:** [Package Manager](/Tech-Ref/Package-Manager).

[[_TOC_]]

---
# Introduction
| :+1: Tip! |
|:-|
| The term **NuGet** is often used ambiguously. Generally it is a short-hand reference to some [NuGet client](/Tech-Ref/Microsoft/Microsoft-Windows/NuGet/NuGet-Client), e.g. the one [Visual Studio](/Tech-Ref/Microsoft/Visual-Studio) contains, the [NuGet CLI](/Tech-Ref/Microsoft/Microsoft-Windows/NuGet/NuGet-CLI), or other.<br/><br/>However, the term might instead refer to any other NuGet component, e.g. [NuGet Server](/Tech-Ref/Microsoft/Microsoft-Windows/NuGet/NuGet-Server), [NuGet Server API](/Tech-Ref/Microsoft/Microsoft-Windows/NuGet/NuGet-Server/NuGet-Server-API), etc. |


***NuGet*** (pronounced "New Get") is a [Windows](/Tech-Ref/Microsoft/Microsoft-Windows) packaging system. It is designed to enable [.NET](/Tech-Ref/Software-Development/NET-Framework) developers to share reusable code. It is a software-plus-service solution for which free and open-source [client applications](/Tech-Ref/Microsoft/Microsoft-Windows/NuGet/NuGet-Client) are available.

NuGet is comprised of two main components; a [client](/Tech-Ref/Microsoft/Microsoft-Windows/NuGet/NuGet-Client) and a [server](/Tech-Ref/Microsoft/Microsoft-Windows/NuGet/NuGet-Server). 
   1. The [NuGet server](/Tech-Ref/Microsoft/Microsoft-Windows/NuGet/NuGet-Server) hosts a repository which then contains packages for distribution. 
   1. The [NuGet client](/Tech-Ref/Microsoft/Microsoft-Windows/NuGet/NuGet-Client) is often used primarily to access a [NuGet Server](/Tech-Ref/Microsoft/Microsoft-Windows/NuGet/NuGet-Server) to download local copies of various packages. However, the client may be used to create local packages and upload them to the [server's](/Tech-Ref/Microsoft/Microsoft-Windows/NuGet/NuGet-Server) repositories. Various other clients then can download these packages over [HTTP/HTTPS](/Tech-Ref/WWW-\(World-Wide-Web\)/HTTP-\(Hypertext-Transfer-Protocol\)).

## Overview
- ![image.png](/.attachments/image-44fc9b6d-7541-46f5-ba7c-8437ca7f08af.png)

## Reference
1. [Wikipedia: NuGet](https://en.wikipedia.org/wiki/NuGet)
1. [An introduction to NuGet](https://docs.microsoft.com/en-us/nuget/what-is-nuget)

---
# Topics
1. [.NET Framework](/Tech-Ref/Software-Development/NET-Framework).
1. [Chocolatey](/Tech-Ref/Microsoft/Microsoft-Windows/Chocolatey).
1. [HTTP/HTTPS](/Tech-Ref/WWW-\(World-Wide-Web\)/HTTP-\(Hypertext-Transfer-Protocol\)).
1. [Windows](/Tech-Ref/Microsoft/Microsoft-Windows).
1. [Visual Studio](/Tech-Ref/Microsoft/Visual-Studio).

---
# Tips and Tricks

## Difference between Chocolatey and NuGet
- [StackOverflow: Difference between Chocolatey and NuGet](https://stackoverflow.com/questions/24662550/difference-between-chocolatey-and-nuget#:~:text=1%20Answer&text=NuGet%20is%20designed%20to%20allow,to%20fill%20a%20different%20need.)
   - "_NuGet is designed to allow you to easily add code libraries to your project. Things like JSON.NET, Entity Framework, etc._"
   - "_Chocolatey is actually built on top of the NuGet package system, but it is designed to fill a different need. Chocolatey wraps up applications and other executables and makes it easy to install them on your computer._"
