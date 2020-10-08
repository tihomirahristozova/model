---
uid: General.DocumentJobs
---
# General.DocumentJobs

Represents jobs, which change state of documents. Entity: Gen_Document_Jobs (Introduced in version 20.1.100.0)

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](General.DocumentJobs.md#Id) | guid |  
| [IsActive](General.DocumentJobs.md#IsActive) | boolean | Specifies whether the job is active and ready for running. [Required] [Default(true)] [Filter(eq)] 
| [Name](General.DocumentJobs.md#Name) | string | The name of the job. [Required] [Filter(eq;like)] [ORD] 
| [JobType](General.DocumentJobs.md#JobType) | [Systems.Core.JobsRepository.JobType](General.DocumentJobs.md#JobType) | The system type of the job. DOC=Document Change State, POS=Run Postponed Events, DNT=Delete Old Notifications. [Required] [Filter(multi eq)] 
| [Notes](General.DocumentJobs.md#Notes) | string (nullable) | Notes for this Job. 
| [RunOnIdle](General.DocumentJobs.md#RunOnIdle) | boolean | Specifies whether to automatically run the job when the server is idle. [Required] [Default(true)] [Filter(eq)] 
| [FilterXml](General.DocumentJobs.md#FilterXml) | dataaccessfilter | Specifies the documents, whose state will be changed. [Required] 
| [NewState](General.DocumentJobs.md#NewState) | [General.DocumentState](General.DocumentJobs.md#NewState) | Specifies the state, which should be set to the documents, matching the filter. [Required] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [DocumentType](General.DocumentJobs.md#DocumentType) | [General.DocumentTypes](General.DocumentTypes.md) | The type of the document, whose state will be changed. [Required] [Filter(multi eq)] |
| [NewUserStatus](General.DocumentJobs.md#NewUserStatus) | [General.DocumentTypeUserStatuses](General.DocumentTypeUserStatuses.md) (nullable) | Specifies the user status, which should be set to the documents, matching the filter. The user statuses are defined for the selected document type. [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### IsActive

> Specifies whether the job is active and ready for running. [Required] [Default(true)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### Name

> The name of the job. [Required] [Filter(eq;like)] [ORD]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  

### JobType

> The system type of the job. DOC=Document Change State, POS=Run Postponed Events, DNT=Delete Old Notifications. [Required] [Filter(multi eq)]

_Type_: **[Systems.Core.JobsRepository.JobType](General.DocumentJobs.md#JobType)**  
Allowed values for the [JobType](Systems.Core.Jobs.md#JobType) data attribute  
_Allowed Values (Enum Members)_  

| Value | Description |
| ---- | --- |
| DocumentChangeState | DocumentChangeState value. Stored as 'DOC'. <br /> _Database Value:_ 'DOC' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'DocumentChangeState' |
| RunPostponedEvents | RunPostponedEvents value. Stored as 'POS'. <br /> _Database Value:_ 'POS' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'RunPostponedEvents' |
| DeleteOldNotifications | DeleteOldNotifications value. Stored as 'DNT'. <br /> _Database Value:_ 'DNT' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'DeleteOldNotifications' |
| DeleteOldPrintImages | DeleteOldPrintImages value. Stored as 'DPI'. <br /> _Database Value:_ 'DPI' <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'DeleteOldPrintImages' |

_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Notes

> Notes for this Job.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### RunOnIdle

> Specifies whether to automatically run the job when the server is idle. [Required] [Default(true)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### FilterXml

> Specifies the documents, whose state will be changed. [Required]

_Type_: **dataaccessfilter**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### NewState

> Specifies the state, which should be set to the documents, matching the filter. [Required]

_Type_: **[General.DocumentState](General.DocumentJobs.md#NewState)**  
Enumeration of document system states  
_Allowed Values (Enum Members)_  

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


## Reference Details

### DocumentType

> The type of the document, whose state will be changed. [Required] [Filter(multi eq)]

_Type_: **[General.DocumentTypes](General.DocumentTypes.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### NewUserStatus

> Specifies the user status, which should be set to the documents, matching the filter. The user statuses are defined for the selected document type. [Filter(multi eq)]

_Type_: **[General.DocumentTypeUserStatuses](General.DocumentTypeUserStatuses.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=General.DocumentJobs erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.DocumentJobs erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=General.DocumentJobs erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_DocumentJobs?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_DocumentJobs?$top=10>

