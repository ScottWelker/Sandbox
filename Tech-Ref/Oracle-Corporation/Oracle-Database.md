[Home](/Slalom-LLC/Slalom-Consulting) | [Glossary](/Glossary) | [Tech Ref](/Tech-Ref) | [Oracle](/Tech-Ref/Oracle-Corporation) | [Relational Database](/Tech-Ref/Software-Development/Database/Relational-Database) | [Software Development](/Tech-Ref/Software-Development) | [DevOps](/Tech-Ref/Software-Development/DevOps-\(Development-and-IT-Operations\))
**AKA:** Oracle DBMS, Oracle.

[[_TOC_]]

---
# Introduction
"_***Oracle Database*** is a multi-model database management system produced and marketed by Oracle Corporation._"

"_It is a database commonly used for running [online transaction processing (OLTP)](/Tech-Ref/OLTP-\(Online-Transaction-Processing\)), [data warehousing (DW)](/Tech-Ref/Software-Development/Database/Data-Warehouse) and mixed (OLTP & DW) database workloads. Oracle Database is available by several service providers on-prem, on-cloud, or as hybrid cloud installation. It may be run on third party servers as well as on Oracle hardware (Exadata on-prem, on Oracle Cloud or at Cloud at Customer)._"

## Reference
1. [Wikipedia: Oracle Database](https://en.wikipedia.org/wiki/Oracle_Database)

---
# Topics
1. [Data Warehouse](/Tech-Ref/Software-Development/Database/Data-Warehouse).
1. [Fiserv InformEnt](/Tech-Ref/Fiserv/Fiserv-InformEnt).
1. [News Entity Model Update (NEMU)](/Clients/Apple/FruitCo-\(Apple\)/FruitCo-FnB/NEMU-\(News-Entity-Model-Update\)) project.
1. [PL/SQL](/Tech-Ref/Oracle-Corporation/Oracle-Database/PL-SQL-\(Procedural-Language-for-SQL\)).
1. [Relational Database](/Tech-Ref/Software-Development/Database/Relational-Database).

---
# Tips and Tricks
- See also [Oracle SQL Developer, Tips and Tricks](/Tech-Ref/Oracle-Corporation/Oracle-SQL-Developer#tips-and-tricks).

## Data Dictionary
- [Oracle9i Database Concepts, The Data Dictionary](https://docs.oracle.com/cd/B10501_01/server.920/a96524/c05dicti.htm)

### List views in Oracle database
- [List views in Oracle database](https://dataedo.com/kb/query/oracle/list-views-in-a-database)

```SQL
select owner as schema_name, 
       view_name
from sys.all_views
order by owner, 
         view_name;
```

## Database Version
```sql
select * from v$version
```
