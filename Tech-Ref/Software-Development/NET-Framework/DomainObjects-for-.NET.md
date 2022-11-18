[Home](/Slalom-LLC/Slalom-Consulting) | [Glossary](/Glossary) | [Tech Ref](/Tech-Ref) | [ORM](/Tech-Ref/Software-Development/ORM-\(Object–Relational-Mapping\)) | [Software Development](/Tech-Ref/Software-Development) | [.NET Framework](/Tech-Ref/Software-Development/NET-Framework)
**AKA:** DomainObjects **(ambiguous short-hand)**.

[[_TOC_]]

---
# Introduction
"_***DomainObjects for .NET*** is an object-relational mapping tool that generates your [.NET](/Tech-Ref/Software-Development/NET-Framework) data layer source code, manages transactions, provides IntelliSense(tm) assisted query building, has excellent performance and enables easy maintenance of a rich domain layer._"

## Reference
1. https://ghe.coxautoinc.com/CMS/CMS-TMS-Domain-Objects
1. [SourceForge: DomainObjects for .NET](https://sourceforge.net/projects/domainobjects/)
1. [DomainObjects for .NET Web Site](http://domainobjects.sourceforge.net/)

---
# Topics
1. [.NET Framework](/Tech-Ref/Software-Development/NET-Framework).
1. [ORM (Object–Relational Mapping)](/Tech-Ref/Software-Development/ORM-\(Object–Relational-Mapping\)).
1. [Title Management System (TMS/CAI)](/Clients/CAI-\(Cox-Automotive-Inc\)/Infrastructure-\(CAI\)/Systems-and-Services-\(CAI\)/TMS).

---
# Fundamentals
Here are selected excerpts, and sometimes [SWelker's](/Individuals/Scott-Welker) annotations, from the [DomainObjects: Quick Start](http://domainobjects.sourceforge.net/Documentation/QuickStart.html). 
- :warning: This is not meant to be complete. Just the notes [I (SWelker)](/Individuals/Scott-Welker) wanted to take.

## Transaction Facade Class
"_This is the class where, in a real-world application, you define those activities that need to occur within the context of a **single transaction**. The complete TransactionFacade class is here._"

"_All creation, modification, and deletion of persistable objects occur within the context of an [DomainObjects](/Tech-Ref/Software-Development/NET-Framework/DomainObjects-for-.NET) object transaction. This 'transactional' behavior is accomplished by a class-level custom attribute_ \[(decoration)\] _defined by [DomainObjects](/Tech-Ref/Software-Development/NET-Framework/DomainObjects-for-.NET):_"

 	[Transaction(TransactionOption.Required)]
	public sealed class TransactionFacade : Service<TransactionFacade>_"

---
# Example Uses
1. [Cox Automotive Inc's (CAI)](/Clients/CAI-\(Cox-Automotive-Inc\)):
   - [Title Management System (TMS)](/Clients/CAI-\(Cox-Automotive-Inc\)/Infrastructure-\(CAI\)/Systems-and-Services-\(CAI\)/TMS):
      - [cm.sln](/Clients/CAI-\(Cox-Automotive-Inc\)/Infrastructure-\(CAI\)/Systems-and-Services-\(CAI\)/TMS/cm.sln#third-party-components).

