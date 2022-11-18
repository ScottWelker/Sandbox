[Home](/Slalom-LLC/Slalom-Consulting) | [Glossary](/Glossary) | [DMI](/Tech-Ref/DMI-\(Dovenmuehle-Mortgage,-Inc.\)) | [Safe CU](/Clients/Safe-CU) | [DMI (SAFE CU)](/Clients/Safe-CU/Infrastructure-\(Safe-CU\)/Systems-and-Services-\(Safe-CU\)/DMI-\(SAFE-CU\))
**Disambiguation:** [Customer Information File (CIF)](/Tech-Ref/DMI-\(Dovenmuehle-Mortgage,-Inc.\)/CIF-\(Customer-Information-File\)), [DMI Teller Report (InformEnt)](/Clients/Safe-CU/Infrastructure-\(Safe-CU\)/Systems-and-Services-\(Safe-CU\)/InformEnt-\(Safe-CU\)/DMI-Teller-Report-\(InformEnt\)).

[[_TOC_]]

---
# Introduciton
***[DMI](/Tech-Ref/DMI-\(Dovenmuehle-Mortgage,-Inc.\)) Teller Report*** refers to either or both the [Fiserv DNA](/Tech-Ref/Fiserv/Fiserv-DNA) add-on "_batch application_" or the [DMI](/Tech-Ref/DMI-\(Dovenmuehle-Mortgage,-Inc.\)) data file it is meant to process. The [DMI](/Tech-Ref/DMI-\(Dovenmuehle-Mortgage,-Inc.\)) produced data file is available in ***standard*** and ***alternate*** formats.

- :warning: Use of the "_alternate format_" implies different application processing, as well as different data file fields.

## Reference
1. [SAFE Credit Union Teams, Project - Data Warehouse Replacement team, General Channel Files, WF #70201 Gap Analysis folder, #6: PS_DMI_TR.docx](/Clients/Safe-CU/Infrastructure-\(Safe-CU\)/Systems-and-Services-\(Safe-CU\)/Teams-\(Safe-CU\)/General-Channel/Files-\(General-Channel\)#wf-70201-gap-analysis):
   - [PS_DMI_TR.DOCX](https://teams.microsoft.com/l/file/A0F6A914-4466-4B71-9A30-3C31B5CC6D9A?tenantId=19746cbd-4387-4281-b3c5-5714dd76477d&fileType=docx&objectUrl=https%3A%2F%2Fsafecuorg.sharepoint.com%2Fsites%2FProject-DataWarehouseReplacement%2FShared%20Documents%2FGeneral%2FDEM%2FWorkfront%20Tasks%2FWF%2070201%20Gap%20Analysis%2FPS_DMI_TR.DOCX&baseUrl=https%3A%2F%2Fsafecuorg.sharepoint.com%2Fsites%2FProject-DataWarehouseReplacement&serviceName=teams&threadId=19%3Aee17d7691895439d9812514cc7c50c25%40thread.tacv2&groupId=c2b442d9-8049-4961-ba96-9a26450fc3d1)

## Notes
1. "_Don’t be fooled by the “teller report” name. It’s actually setting up the loan account (as an [external account](/Tech-Ref/Fiserv/Fiserv-DNA/External-Account-\(Fiserv-DNA\))) in [DNA](/Tech-Ref/Fiserv/Fiserv-DNA)._" -- [Alexis Fitzpatrick](/Individuals/Alexis-Fitzpatrick)

---
# Topics
1. [DMI (SAFE CU)](/Clients/Safe-CU/Infrastructure-\(Safe-CU\)/Systems-and-Services-\(Safe-CU\)/DMI-\(SAFE-CU\)).
1. [DMI to InformEnt versus DMI to DNA](/Clients/Safe-CU/DEM-\(Data-Engineering-&-Management\)/Data-Warehouse-Replacement/Reports/WF-70201:-Identify-data-gaps-between-Spectrum-&-ODS%2DM360/3.-DMI-to-InformEnt-versus-DMI-to-DNA).
1. [Dovenmuehle Mortgage, Inc. (DMI)](/Tech-Ref/DMI-\(Dovenmuehle-Mortgage,-Inc.\)).
1. [Fiserv DNA](/Tech-Ref/Fiserv/Fiserv-DNA).
1. [Fiserv DNA (Safe CU)](/Clients/Safe-CU/Infrastructure-\(Safe-CU\)/Systems-and-Services-\(Safe-CU\)/DNA-\(Safe-CU\)).

---
# Teller Report Process
This section details teller report file processing, as inferred from [PS_DMI_TR.docx (#6)](/Clients/Safe-CU/Infrastructure-\(Safe-CU\)/Systems-and-Services-\(Safe-CU\)/Teams-\(Safe-CU\)/General-Channel/Files-\(General-Channel\)#artifact6) and dialog with [SAFE CU](/Clients/Safe-CU) personnel.

|:warning:| Issues [PS_DMI_TR.docx (#6)](/Clients/Safe-CU/Infrastructure-\(Safe-CU\)/Systems-and-Services-\(Safe-CU\)/Teams-\(Safe-CU\)/General-Channel/Files-\(General-Channel\)#artifact6) Review|
|:-:|:-|
|1.| [I've (SWelker)](/Individuals/Scott-Welker) presumed the ***Configuration Checklist:*** and ***Installation:*** sub-sections are not relevant.|
|2. | The purpose and meaning of the ***Updating Applications*** and ***Report(s):*** sub-sections is not clear:<ul><li>:+1:[I've (SWelker)](/Individuals/Scott-Welker) determined that the ***Non-Transaction Updating Applications*** subsection of _Updating Applications_ merely repeats all fields defined in the ***Processing:*** subsection's ***Account Fields:*** section.</li><li>:+1:[I (SWelker)](/Individuals/Scott-Welker) cannot discern the meaning or value of the _Report(s):_ subsection.</li></ul> |
|3. | Phrases like "_the database_", "_external account_", "_the account_" are sometimes used without clear context.<ul><li>:+1:[I've (SWelker)](/Individuals/Scott-Welker) inferred that:</li><ul><li>"_the database_" means the [Fiserv DNA](/Tech-Ref/Fiserv/Fiserv-DNA) database.</li><li>"_the account_" means the [Fiserv DNA](/Tech-Ref/Fiserv/Fiserv-DNA) database record.</li><li>"_external account_" appears to be yet another term used in reference to the [Fiserv DNA](/Tech-Ref/Fiserv/Fiserv-DNA) database record. "_External Account Number_" is a specific [Fiserv DNA database field](#database-fields).</li></ul></ul>|
|5. | The source of a named field isn't always clear. It may refer to a Teller Report (batch application) '_parameter_', a Teller Report (file) field, or a [DNA](/Tech-Ref/Fiserv/Fiserv-DNA) (database) field:<br/><br/><ul><li>:+1:[I've (SWelker)](/Individuals/Scott-Welker) inferred that "_Account Field_" means [DNA](/Tech-Ref/Fiserv/Fiserv-DNA) Database Field.</li></ul>|
|6. | The following sentence can be interpreted multiple ways. The [Process Flow ("CAUTION! Ambiguity/Inference!" shape)](#process-flow) below illustrates the interpretation I've guessed is what was intended.<ul><li>`If there is a value in the Principal Balance (position 141-150), Interest Rate (position 183-189), Maturity Date field (position 262-269), Original Loan Date field (position 244-251), Original Loan Amount field (position 252-261), the Note Balance, Interest Rate, maturity date & contract date populated in DNA.`</li></ul>|

## Overview
::: mermaid
graph LR
dmi[DMI]-- Teller Report File -->SAFE[SAFE]
SAFE[SAFE]-- Teller Report File<br/><br/>'File Fields' -->DNATR(Fiserv DNA, DMI Teller Report<br/>Batch Application<br/><br/>'Parameters')
DNATR-->DNA("Fiserv DNA<br/>Database<br/>(Core)<br/><br/>'Account Fields'")
:::

- :+1: The [PS_DMI_TR.DOCX](https://teams.microsoft.com/l/file/A0F6A914-4466-4B71-9A30-3C31B5CC6D9A?tenantId=19746cbd-4387-4281-b3c5-5714dd76477d&fileType=docx&objectUrl=https%3A%2F%2Fsafecuorg.sharepoint.com%2Fsites%2FProject-DataWarehouseReplacement%2FShared%20Documents%2FGeneral%2FDEM%2FWorkfront%20Tasks%2FWF%2070201%20Gap%20Analysis%2FPS_DMI_TR.DOCX&baseUrl=https%3A%2F%2Fsafecuorg.sharepoint.com%2Fsites%2FProject-DataWarehouseReplacement&serviceName=teams&threadId=19%3Aee17d7691895439d9812514cc7c50c25%40thread.tacv2&groupId=c2b442d9-8049-4961-ba96-9a26450fc3d1) document's field names may refer to file fields, batch application parameters, or [DNA](/Tech-Ref/Fiserv/Fiserv-DNA) database fields.

## Process Flow
::: mermaid
graph TD
trf[DMI Teller Report File]-->dnatr(Fiserv DNA Teller Report)
dnatr-->altf{Alternate File Format?}
altf-- Yes -->altp(Alternate File Process)
altf-- No -->stdp(Standard File Process)
stdp-->getrec(Read First/Next Record)
getrec-->taxId1(Std. Tax ID Look Up:<br/>Tax ID in file looked up in database.)
taxId1-->taxidLk{Exactly 1<br/>Tax Id Found?}
taxidLk-- No<br/>Exception Report -->getrec
taxidLk-- Yes -->getact(Get Account Number)
getact-->actf{Account Found?}
actf-- No -->crearec(Create Account:<br>1. Product specified by<br/>'Minor Account Type Code'.<br/><br/>2. Assigned to branch specified<br/>in 'Branch Org Number'.<br/><br/>3. Tax reported for owner found<br/>in the first step is assigned to the<br/>new account.)
actf-- Yes -->updrec(Update Account With File Info.<br/>Account level user fields populated:<br/>- External Account Number.<br/>- Original Amount.<br/>- Last Activity Date.<br/>- Next Payment Due Date.<br/>- Monthly Payment.<br/>- Last Payment Due Date.<br/>- Last Payment Amount.<br/>- Days Past Due.<br/>- Amount Past Due.<br/>- Late Fees Due.<br/>- Last Updated.<br/>)
updrec-->clsacts(Close accounts not in file.<br/>If zero balance - both NOTE/BAL and LCHG/BAL.<br/>Balance ignored if 'Close with Balance' set to Y.<br/>Accounts re-opened if included in future import file.)
crearec-->updrec
clsacts-->done((Done.))

altp-->getrec2(Read First/Next Record)
getrec2-->taxId2(Alt Tax ID Lookup:<br/>Standard processing occurs for<br/>Tax Owner Except co-borrower<br/>Tax ID used to locate<br/>person/organization in DNA.)
taxId2-->taxidLk2{Exactly 1<br/>Co-borrower<br/>Tax Id Found?}
taxidLk2-- Yes -->addcbwr(Add co-borrower to external account<br/>as a NonTax Owner and NonTax Signator.)
taxId2-.->getact
taxId2-.->updrec
addcbwr-->popflds(CAUTION! Ambiguity/Inference!<br/><br/>IF these fields have values:<br/>-Principal Balance<br/>-Interest Rate<br/>-Maturity Date<br/>-Original Loan Date<br/>-Original Loan Amount<br/><br/>THEN update DNA with:<br/>-Note Balance<br/>-Interest Rate<br/>-Maturity Date<br/>-Contract Date.)
popflds-->popflds2(In addition to the standard layout's<br/>account fields, following account<br/>level user fields are populated:<br/>-Deferred Principal Balance.<br/>-Payment Frequency.<br/>-Suspense Balance <br/>-Escrow Indicator.<br/>-Escrow Balance.<br/>-Original Loan Date.<br/>-Maturity Date.<br/>-Loan Term.<br/>-YTD Interest.<br/>-Property Value.<br/>-Late Pmt Last 12 months.<br/>-Life/Dis Ins Code.)
taxidLk2-- No<br/>Exception Report -->getrec2
popflds2-.->updrec
popflds2-->done
:::

---
# File Formats (Teller Report)
The _Teller Report_ file is available in two formats, standard and alternate. 

## Standard Layout
:warning: This is a convenience list. [PS_DMI_TR.DOCX](https://teams.microsoft.com/l/file/A0F6A914-4466-4B71-9A30-3C31B5CC6D9A?tenantId=19746cbd-4387-4281-b3c5-5714dd76477d&fileType=docx&objectUrl=https%3A%2F%2Fsafecuorg.sharepoint.com%2Fsites%2FProject-DataWarehouseReplacement%2FShared%20Documents%2FGeneral%2FDEM%2FWorkfront%20Tasks%2FWF%2070201%20Gap%20Analysis%2FPS_DMI_TR.DOCX&baseUrl=https%3A%2F%2Fsafecuorg.sharepoint.com%2Fsites%2FProject-DataWarehouseReplacement&serviceName=teams&threadId=19%3Aee17d7691895439d9812514cc7c50c25%40thread.tacv2&groupId=c2b442d9-8049-4961-ba96-9a26450fc3d1) is the document of record.

|#| Field Name |
|:-:|:-|
| 1.| Loan Number  |
| 2.| Mortgager First Name  |
| 3.| Mortgager Last Name  |
| 4.| Old Loan Number (Tax ID)  |
| 5.| Last Payment Due Date  |
| 6.| Next Payment Due Date  |
| 7.| Monthly Payment  |
| 8.| Principal Balance  |
| 9.| Amt Past Due  |
| 10.| Days Past Due  |
| 11.| Last Payment Amount  |
| 12.| Original Amount  |
| 13.| Late Fee Due  |
| 14.| Date of Last Activity  |

## Alternate Layout
:warning: This is a convenience list. [PS_DMI_TR.DOCX](https://teams.microsoft.com/l/file/A0F6A914-4466-4B71-9A30-3C31B5CC6D9A?tenantId=19746cbd-4387-4281-b3c5-5714dd76477d&fileType=docx&objectUrl=https%3A%2F%2Fsafecuorg.sharepoint.com%2Fsites%2FProject-DataWarehouseReplacement%2FShared%20Documents%2FGeneral%2FDEM%2FWorkfront%20Tasks%2FWF%2070201%20Gap%20Analysis%2FPS_DMI_TR.DOCX&baseUrl=https%3A%2F%2Fsafecuorg.sharepoint.com%2Fsites%2FProject-DataWarehouseReplacement&serviceName=teams&threadId=19%3Aee17d7691895439d9812514cc7c50c25%40thread.tacv2&groupId=c2b442d9-8049-4961-ba96-9a26450fc3d1) is the document of record.

|#| Field Name  |
|:-:|:-|
| 1.| Loan Number  |
| 2.| Mortgager First Name  |
| 3.| Mortgager Last Name  |
| 4.| Mortgager Tax ID  |
| 5.| CO Mortgager First Name  |
| 6.| CO Mortgager Last Name  |
| 7.| CO Mortgager Tax ID  |
| 8.| Principal Balance  |
| 9.| Deferred Principal Balance  |
| 10.| Monthly Payment  |
| 11.| Payment Frequency  |
| 12.| APR (Interest Rate)  |
| 13.| Suspense Balance  |
| 14.| Next Payment Due Date  |
| 15.| Days Past Due  |
| 16.| Amt Past Due  |
| 17.| Escrow Indicator  |
| 18.| Escrow Balance  |
| 19.| Late Fee Due  |
| 20.| Original Loan Date  |
| 21.| Original Loan Amount  |
| 22.| Maturity Date  |
| 23.| Loan Term  |
| 24.| YTD Interest  |
| 25.| Property Value  |
| 26.| Late Payment Last 12 months  |
| 27.| Life/Dis Ins Code  |

---
# Batch Application (Teller Report)
The teller report '_batch application_' behavior is controlled via these parameters. 

## Parameters
:warning: This is a convenience list. [PS_DMI_TR.DOCX](https://teams.microsoft.com/l/file/A0F6A914-4466-4B71-9A30-3C31B5CC6D9A?tenantId=19746cbd-4387-4281-b3c5-5714dd76477d&fileType=docx&objectUrl=https%3A%2F%2Fsafecuorg.sharepoint.com%2Fsites%2FProject-DataWarehouseReplacement%2FShared%20Documents%2FGeneral%2FDEM%2FWorkfront%20Tasks%2FWF%2070201%20Gap%20Analysis%2FPS_DMI_TR.DOCX&baseUrl=https%3A%2F%2Fsafecuorg.sharepoint.com%2Fsites%2FProject-DataWarehouseReplacement&serviceName=teams&threadId=19%3Aee17d7691895439d9812514cc7c50c25%40thread.tacv2&groupId=c2b442d9-8049-4961-ba96-9a26450fc3d1) is the document of record.

|#| Parameter | Description (how used) |
|:-:|:-|:-|
| 1.| External File Name | The full path, name and extension of the teller report sent by DMI. |
| 2.| Branch Org Number | The branch new accounts are assigned. |
| 3.| Minor Account Type Code | The minor account type code that is assigned to new accounts. |
| 4.| Close with Balance | Allow external accounts to close if they are not in the file, even if they have a balance. |
| 5.| Mask TIN Information | When set to Y, TIN masked using the following formats:  ***-**-1234 for persons and 12-****123 for organizations.<br/>All application output which includes TIN is masked when the parameter is set to Y.<br/>When set to N or is blank, TIN appears in the clear. |
| 6.| Alternate File Format YN | When set to N or is blank, the Standard File Format in the File Layouts section expected when the file is read.<br/>When set to Y, the Alternate File Format in the File Layouts section expected when the file is read. |

---
# Fiserv DNA (Account)

## Database Fields
:warning: This is a convenience list derived from a close read of the [PS_DMI_TR.DOCX](https://teams.microsoft.com/l/file/A0F6A914-4466-4B71-9A30-3C31B5CC6D9A?tenantId=19746cbd-4387-4281-b3c5-5714dd76477d&fileType=docx&objectUrl=https%3A%2F%2Fsafecuorg.sharepoint.com%2Fsites%2FProject-DataWarehouseReplacement%2FShared%20Documents%2FGeneral%2FDEM%2FWorkfront%20Tasks%2FWF%2070201%20Gap%20Analysis%2FPS_DMI_TR.DOCX&baseUrl=https%3A%2F%2Fsafecuorg.sharepoint.com%2Fsites%2FProject-DataWarehouseReplacement&serviceName=teams&threadId=19%3Aee17d7691895439d9812514cc7c50c25%40thread.tacv2&groupId=c2b442d9-8049-4961-ba96-9a26450fc3d1) document. I've inferred "_Account Fields_" means [DNA](/Tech-Ref/Fiserv/Fiserv-DNA) Database Fields.

|# |Account Field | Description (how used)  |
|:-:|:-|:-|
| 1.| External Account Number |This user field is an account level user field which is used to store the external account number  |
| 2.| Original Amount |This user field is an account level user field which is used to store the original amount.  |
| 3.| Last Activity Date |This user field is an account level user field which is used to store the date when the last activity was performed  |
| 4.| Next Payment Due Date |This user field is an account level user field which is used to store the date when the next payment is due  |
| 5.| Monthly Payment |This user field is an account level user field which is used to store the monthly payment  |
| 6.| Last Payment Due Date |This user field is an account level user field which is used to store the date when the last payment was due  |
| 7.| Last Payment Amount |This user field is an account level user field which is used to store the amount of the last payment  |
| 8.| Days Past Due |This user field is an account level user field which is used to store the past due days  |
| 9.| Amount Past Due |This user field is an account level user field which is used to store the amount of past due  |
| 10.| Late Fees Due |This user field is an account level user field which is used to store the amount of the late fee which is due  |
| 11.| Last Updated |This user field is an account level user field which is used to store when it was last updated  |
| 12.| Deferred Principal Balance |This user field is an account level user field which is used to store the second principal balance  |
| 13.| Payment Frequency |This user field is an account level user field which is used to store the payment frequency  |
| 14.| Suspense Balance |This user field is an account level user field which is used to store the suspense balance  |
| 15.| Escrow Indicator |This user field is an account level user field which is used to store the escrow indicator  |
| 16.| Escrow Balance |This user field is an account level user field which is used to store the escrow balance  |
| 17.| Original Loan Date |This user field is an account level user field which is used to store the note date  |
| 18.| Maturity Date |This user field is an account level user field which is used to store the maturity date  |
| 19.| Loan Term |This user field is an account level user field which is used to store the loan term  |
| 20.| YTD Interest |This user field is an account level user field which is used to store the YTD mortgage interest  |
| 21.| Property Value |This user field is an account level user field which is used to store the property value  |
| 22.| Late Pmt Last 12 months |This user field is an account level user field which is used to store the late payment in last 12 months  |
| 23.| Life/Dis Ins Code |This user field is an account level user field which is used to store the Life/Dis Ins Code  |
