---
uid: Systems.Core.Jobs
---
# Systems.Core.Jobs

The jobs, which are configured in the system. Entity: Sys_Jobs (Introduced in version 20.1.100.0)

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Systems.Core.Jobs.md#Id) | guid |  
| [IsActive](Systems.Core.Jobs.md#IsActive) | boolean | Specifies whether the job is active and ready for running. [Required] [Default(true)] [Filter(eq)] 
| [Name](Systems.Core.Jobs.md#Name) | string | The name of the job. [Required] [Filter(eq;like)] [ORD] 
| [JobType](Systems.Core.Jobs.md#JobType) | [Systems.Core.JobsRepository.JobType](Systems.Core.Jobs.md#JobType) | The system type of the job. DOC=Document Change State, POS=Run Postponed Events, DNT=Delete Old Notifications. [Required] [Filter(multi eq)] 
| [Notes](Systems.Core.Jobs.md#Notes) | string (nullable) | Notes for this Job. 
| [RunOnIdle](Systems.Core.Jobs.md#RunOnIdle) | boolean | Specifies whether to automatically run the job when the server is idle. [Required] [Default(true)] [Filter(eq)] 


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

_Type_: **[Systems.Core.JobsRepository.JobType](Systems.Core.Jobs.md#JobType)**  
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



## Business Rules

[!list erp.entity=Systems.Core.Jobs erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Systems.Core.Jobs erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Systems.Core.Jobs erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Systems_Core_Jobs?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Systems_Core_Jobs?$top=10>

