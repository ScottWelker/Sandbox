[Home](/Slalom-LLC/Slalom-Consulting) | [Glossary](/Glossary) | [Tech Ref](/Tech-Ref) | [Fiserv](/Tech-Ref/Fiserv) | [InformEnt](/Tech-Ref/Fiserv/Fiserv-InformEnt)
**Disambiguation** [KnowledgeShare](/Tech-Ref/Fiserv/Fiserv-InformEnt/KnowledgeShare), [PowerShell](/Tech-Ref/Microsoft/PowerShell).

[[_TOC_]]

---
# Introduction
***PowerShare*** is an administrative tool which allows you to manage and extend the data model while providing greater ease of use and access, including customizable views and tables.

- :+1: Tips! 
   1. _PowerShare_ typically refers to ***PowerShare Information Manager*** but it may also refer instead to ***PowerShare Security Manager*** (other:question:).
   1. _PowerShare_ is a component of various [Fiserv](/Tech-Ref/Fiserv) offerings, including [InformEnt](/Tech-Ref/Fiserv/Fiserv-InformEnt).


## Reference
1. [Fiserv: iVue-brochure.pdf](http://solutions.fiserv.com/dialoguecleartouchq22019ivue/LPT.url?kn=3143322&vs=MGNjZGE0ODktNTFhOC00YjgwLTk0MjEtY2MzNDM3NzQ4NGFjOzsS1)
1. [Fiserv: Case Study, Luther Burbank Savings](http://solutions.fiserv.com/dialoguecleartouchq22019ivue/LPT.url?kn=3143322&vs=MGNjZGE0ODktNTFhOC00YjgwLTk0MjEtY2MzNDM3NzQ4NGFjOzsS1)

## Notes
1. [scuwkpdc90214 (PowerShare host)](/Clients/Safe-CU/Infrastructure-\(Safe-CU\)/Hosts-\(Safe-CU\)/scuwkpdc90214).
1. An administrative tool [Scott Vaughn](/Individuals/Scott-Vaughn) presented.
   - Create Views and Tables. Reports then leverage these views/tables.
1. `U_<name>` prefix signifies table (for import).
1. `WV_<name>` prefix signifies the view corresponding to table `U_<name>`

---
# Topics
1. [Fiserv](/Tech-Ref/Fiserv).
1. [scuwkpdc90214 (PowerShare host)](/Clients/Safe-CU/Infrastructure-\(Safe-CU\)/Hosts-\(Safe-CU\)/scuwkpdc90214).

---
# Tips and Tricks
## Error On PowerShare Information Manager Start-up
If you receive the following error dialog on PowerShare Information Manager start-up you may safely press \[No\] to dismiss/ignore it. 
- **InformEnt PowerShare: Information Manager** (dialog)
   - A DBMS name has not been defined in your Registry. Do you want to add this information? Admin Rights must be required to do this process.
