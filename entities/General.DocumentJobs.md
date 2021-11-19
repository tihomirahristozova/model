---
uid: General.DocumentJobs
---
# General.DocumentJobs Entity

**Namespace:** [General](General.md)  
**Inherited From:** [Systems.Core.Jobs](Systems.Core.Jobs.md)  

Represents jobs, which change state of documents. Entity: Gen_Document_Jobs (Introduced in version 20.1)

## Default Visualization
Default Display Text Format:  
_{Name}_  
Default Search Members:  
_Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [General.DocumentJobs](General.DocumentJobs.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [FilterXml](General.DocumentJobs.md#filterxml) | dataaccessfilter | Specifies the documents, whose state will be changed. `Required` 
| [Id](General.DocumentJobs.md#id) | guid |  
| [IsActive](General.DocumentJobs.md#isactive) | boolean | Specifies whether the job is active and ready for running. `Required` `Default(true)` `Filter(eq)` (Inherited from [Jobs](Systems.Core.Jobs.md)) 
| [JobType](General.DocumentJobs.md#jobtype) | [JobType](General.DocumentJobs.md#jobtype) | The system type of the job. DOC=Document Change State, POS=Run Postponed Events, DNT=Delete Old Notifications. `Required` `Filter(multi eq)` (Inherited from [Jobs](Systems.Core.Jobs.md)) 
| [Name](General.DocumentJobs.md#name) | string (254) | The name of the job. `Required` `Filter(eq;like)` `ORD` (Inherited from [Jobs](Systems.Core.Jobs.md)) 
| [NewState](General.DocumentJobs.md#newstate) | [DocumentState](General.DocumentJobs.md#newstate) | Specifies the state, which should be set to the documents, matching the filter. `Required` 
| [Notes](General.DocumentJobs.md#notes) | string (max) __nullable__ | Notes for this Job. (Inherited from [Jobs](Systems.Core.Jobs.md)) 
| [RunOnIdle](General.DocumentJobs.md#runonidle) | boolean | Specifies whether to automatically run the job when the server is idle. `Required` `Default(true)` `Filter(eq)` (Inherited from [Jobs](Systems.Core.Jobs.md)) 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [DocumentType](General.DocumentJobs.md#documenttype) | [DocumentTypes](General.DocumentTypes.md) | The type of the document, whose state will be changed. `Required` `Filter(multi eq)` |
| [NewUserStatus](General.DocumentJobs.md#newuserstatus) | [DocumentTypeUserStatuses](General.DocumentTypeUserStatuses.md) (nullable) | Specifies the user status, which should be set to the documents, matching the filter. The user statuses are defined for the selected document type. `Filter(multi eq)` |


## Attribute Details

### FilterXml

Specifies the documents, whose state will be changed. `Required`

_Type_: **dataaccessfilter**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### IsActive

Specifies whether the job is active and ready for running. `Required` `Default(true)` `Filter(eq)` (Inherited from [Jobs](Systems.Core.Jobs.md))

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### JobType

The system type of the job. DOC=Document Change State, POS=Run Postponed Events, DNT=Delete Old Notifications. `Required` `Filter(multi eq)` (Inherited from [Jobs](Systems.Core.Jobs.md))

_Type_: **[JobType](General.DocumentJobs.md#jobtype)**  
Allowed values for the `JobType`(Systems.Core.Jobs.md#jobtype) data attribute  
_Allowed Values (Systems.Core.JobsRepository.JobType Enum Members)_  

| Value | Description |
| ---- | --- |
| DocumentChangeState | DocumentChangeState value. Stored as 'DOC'. <br /> _Database Value:_ 'DOC' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'DocumentChangeState' |
| RunPostponedEvents | RunPostponedEvents value. Stored as 'POS'. <br /> _Database Value:_ 'POS' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'RunPostponedEvents' |
| DeleteOldNotifications | DeleteOldNotifications value. Stored as 'DNT'. <br /> _Database Value:_ 'DNT' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'DeleteOldNotifications' |
| DeleteOldPrintImages | DeleteOldPrintImages value. Stored as 'DPI'. <br /> _Database Value:_ 'DPI' <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'DeleteOldPrintImages' |

_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Name

The name of the job. `Required` `Filter(eq;like)` `ORD` (Inherited from [Jobs](Systems.Core.Jobs.md))

_Type_: **string (254)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  
_Maximum Length_: **254**  

### NewState

Specifies the state, which should be set to the documents, matching the filter. `Required`

_Type_: **[DocumentState](General.DocumentJobs.md#newstate)**  
Enumeration of document system states  
_Allowed Values (General.DocumentState Enum Members)_  

| Value | Description |
| ---- | --- |
| New | New document, just created. Can be edited. (Stored as 0). <br /> _Database Value:_ 0 <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'New' |
| Adjustment | Document which adjusts other released documents. (Stored as 5). <br /> _Database Value:_ 5 <br /> _Model Value:_ 5 <br /> _Domain API Value:_ 'Adjustment' |
| Planned | Planned by the system for future releasing. (Stored as 10). <br /> _Database Value:_ 10 <br /> _Model Value:_ 10 <br /> _Domain API Value:_ 'Planned' |
| FirmPlanned | Planned by operator for future releasing. (Stored as 20). <br /> _Database Value:_ 20 <br /> _Model Value:_ 20 <br /> _Domain API Value:_ 'FirmPlanned' |
| Released | Released document. Changes can be applied only through adjustment documents. (Stored as 30). <br /> _Database Value:_ 30 <br /> _Model Value:_ 30 <br /> _Domain API Value:_ 'Released' |
| Completed | Work has completed. (Stored as 40). <br /> _Database Value:_ 40 <br /> _Model Value:_ 40 <br /> _Domain API Value:_ 'Completed' |
| Closed | The document is audited and closed. Adjustments are not allowed, but reopening is allowed. (Stored as 50). <br /> _Database Value:_ 50 <br /> _Model Value:_ 50 <br /> _Domain API Value:_ 'Closed' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Notes

Notes for this Job. (Inherited from [Jobs](Systems.Core.Jobs.md))

_Type_: **string (max) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  

### RunOnIdle

Specifies whether to automatically run the job when the server is idle. `Required` `Default(true)` `Filter(eq)` (Inherited from [Jobs](Systems.Core.Jobs.md))

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **True**  


## Reference Details

### DocumentType

The type of the document, whose state will be changed. `Required` `Filter(multi eq)`

_Type_: **[DocumentTypes](General.DocumentTypes.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### NewUserStatus

Specifies the user status, which should be set to the documents, matching the filter. The user statuses are defined for the selected document type. `Filter(multi eq)`

_Type_: **[DocumentTypeUserStatuses](General.DocumentTypeUserStatuses.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list limit=1000 erp.entity=General.DocumentJobs erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=General.DocumentJobs erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_DocumentJobs?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_DocumentJobs?$top=10>

