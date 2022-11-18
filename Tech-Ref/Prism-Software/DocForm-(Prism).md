[Home](/Slalom-LLC/Slalom-Consulting) | [Glossary](/Glossary) | [Tech Ref](/Tech-Ref) | [Prism Software](/Tech-Ref/Prism-Software)

[[_TOC_]]

---
# Introduction
"_***DocForm™,*** a [Prism Software](/Tech-Ref/Prism-Software) product, enables automated generation of high volume electronic, mobile, email, and print variable data-driven business communications._"

"_DocForm is designed for organizations that need to generate high volumes of highly personalized electronic, mobile, email, and print business communications. It’s ideal for eStatement and printed statements, customer notifications, and other types of complex communications._"

"_DocForm includes a project **design interface** that allows the creation of a wide range of print and electronic communications. Projects can range from simple notifications to complex conditionally processed customer offers._"

## Reference
1. [PrismSoftware: DocForm](https://prismsoftware.com/products/docform/)
1. [PrismSupport: User Guide](https://prismsupport.com/documentation/Content/A_IntroTopics/DocForm-Home.htm)
1. [Prism-DocForm-GeneralLit.pdf](/.attachments/prism-docform-generallit-e9afb879-125f-4706-8988-5b98fce79287.pdf)

## Notes
1. :+1: Notable because if its use in [CAI's](/Clients/CAI-\(Cox-Automotive-Inc\)) [Title Management System (TMS)](/Clients/CAI-\(Cox-Automotive-Inc\)/Infrastructure-\(CAI\)/Systems-and-Services-\(CAI\)/TMS).
1. Some extensibility provided via [JScript](/Tech-Ref/Software-Development/JavaScript/JScript).

---
# Topics
1. [DocForm (CAI - TMS)](/Clients/CAI-\(Cox-Automotive-Inc\)/Infrastructure-\(CAI\)/Systems-and-Services-\(CAI\)/DocForm-\(CAI-%2D-TMS\)).
1. [JScript](/Tech-Ref/Software-Development/JavaScript/JScript).
1. [Prism Software](/Tech-Ref/Prism-Software).

---
# Concepts

## DocForm Server
The **DocForm server** is a [Windows](/Tech-Ref/Microsoft/Microsoft-Windows) service that executes the projects which were created with the [DocForm Designer](#docform-designer).

## DocForm Designer
The **DocForm Designer** is an [Integrated Development Environment (IDE)](/Tech-Ref/Software-Development/IDE-\(Integrated-Development-Environment\)) for creating and testing a [project](#project).

### Project
- "_DocForm has a **project** [design interface](#docform-designer) that allows the creation of a wide range of print and electronic communications. Projects can range from simple notifications to complex conditionally processed customer offers._"
- The DocForm Project encapsulates one to many forms, and each form's definition.
- DocForm Projects are persisted to disk as [XML](/Tech-Ref/Software-Development/Markup-Language/XML-\(eXtensible-Markup-Language\)) files with the `.dfproj` extension.

### Form
- Per [Duc Le](/Clients/CAI-\(Cox-Automotive-Inc\)#ducle) "_The form is an [XML](/Tech-Ref/Software-Development/Markup-Language/XML-\(eXtensible-Markup-Language\)) driven configuration/data structure used by DocForm to generate a [PDF](/Tech-Ref/PDF-\(Portable-Document-Format\)). Users utilize a [DocForm Studio utility/UI](#docform-designer) to edit the "_Form._" Form's are encapsulated by DocForm projects._"
