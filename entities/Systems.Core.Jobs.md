---
uid: Systems.Core.Jobs
---
# Systems.Core.Jobs Entity

The jobs, which are configured in the system. Entity: Sys_Jobs (Introduced in version 20.1)

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Systems.Core.Jobs.md#id) | guid |  
| [IsActive](Systems.Core.Jobs.md#isactive) | boolean | Specifies whether the job is active and ready for running. [Required] [Default(true)] [Filter(eq)] 
| [JobType](Systems.Core.Jobs.md#jobtype) | [JobType](Systems.Core.Jobs.md#jobtype) | The system type of the job. DOC=Document Change State, POS=Run Postponed Events, DNT=Delete Old Notifications. [Required] [Filter(multi eq)] 
| [Name](Systems.Core.Jobs.md#name) | string | The name of the job. [Required] [Filter(eq;like)] [ORD] 
| [Notes](Systems.Core.Jobs.md#notes) | string (nullable) | Notes for this Job. 
| [RunOnIdle](Systems.Core.Jobs.md#runonidle) | boolean | Specifies whether to automatically run the job when the server is idle. [Required] [Default(true)] [Filter(eq)] 


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### IsActive

Specifies whether the job is active and ready for running. [Required] [Default(true)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### JobType

The system type of the job. DOC=Document Change State, POS=Run Postponed Events, DNT=Delete Old Notifications. [Required] [Filter(multi eq)]

_Type_: **[JobType](Systems.Core.Jobs.md#jobtype)**  
Allowed values for the [JobType](Systems.Core.Jobs.md#jobtype) data attribute  
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

The name of the job. [Required] [Filter(eq;like)] [ORD]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  

### Notes

Notes for this Job.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### RunOnIdle

Specifies whether to automatically run the job when the server is idle. [Required] [Default(true)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **True**  



## Business Rules

[!list erp.entity=Systems.Core.Jobs erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Systems.Core.Jobs erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Systems_Core_Jobs?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Systems_Core_Jobs?$top=10>

