---
uid: Systems.Bpm.ProcessInstances
---
# Systems.Bpm.ProcessInstances

Contains the running instances of the processes. Entity: Bpm_Process_Instances

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Systems.Bpm.ProcessInstances.md#Id) | guid |  
| [CreationTime](Systems.Bpm.ProcessInstances.md#CreationTime) | datetime | The date and time, when the process instance was created. [Required] [Default(Now)] [Filter(eq)] [ReadOnly] 
| [FinishTime](Systems.Bpm.ProcessInstances.md#FinishTime) | datetime (nullable) | The date and time, when the process instance has finished its execution. null when the instance has not yet finished execution. [Filter(eq)] [ReadOnly] 
| [StartTime](Systems.Bpm.ProcessInstances.md#StartTime) | datetime | The date and time, when the process instance was started. [Required] [Default(Now)] [Filter(eq)] [ReadOnly] 
| [State](Systems.Bpm.ProcessInstances.md#State) | [Systems.Bpm.ProcessInstancesRepository.State](Systems.Bpm.ProcessInstances.md#State) | Instance state. 0=Created; 60=Completed. [Required] [Default(0)] [Filter(eq)] [ReadOnly] 
| [Subject](Systems.Bpm.ProcessInstances.md#Subject) | string | The multilanguage subject (or title) of this process instance. [Required] [Filter(eq;like)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Process](Systems.Bpm.ProcessInstances.md#Process) | [Systems.Bpm.Processes](Systems.Bpm.Processes.md) | The process on which this instance is based. [Required] [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### CreationTime

> The date and time, when the process instance was created. [Required] [Default(Now)] [Filter(eq)] [ReadOnly]

_Type_: **datetime**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **CurrentDateTime**  

### FinishTime

> The date and time, when the process instance has finished its execution. null when the instance has not yet finished execution. [Filter(eq)] [ReadOnly]

_Type_: **datetime (nullable)**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

### StartTime

> The date and time, when the process instance was started. [Required] [Default(Now)] [Filter(eq)] [ReadOnly]

_Type_: **datetime**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **CurrentDateTime**  

### State

> Instance state. 0=Created; 60=Completed. [Required] [Default(0)] [Filter(eq)] [ReadOnly]

_Type_: **[Systems.Bpm.ProcessInstancesRepository.State](Systems.Bpm.ProcessInstances.md#State)**  
Allowed values for the [State](Systems.Bpm.ProcessInstances.md#State) data attribute  
_Allowed Values (Enum Members)_  

| Value | Description |
| ---- | --- |
| Created | Created value. Stored as 0. <br /> _Database Value:_ 0 <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Created' |
| Start | Start value. Stored as 10. <br /> _Database Value:_ 10 <br /> _Model Value:_ 10 <br /> _Domain API Value:_ 'Start' |
| Finish | Finish value. Stored as 20. <br /> _Database Value:_ 20 <br /> _Model Value:_ 20 <br /> _Domain API Value:_ 'Finish' |
| Complated | Complated value. Stored as 60. <br /> _Database Value:_ 60 <br /> _Model Value:_ 60 <br /> _Domain API Value:_ 'Complated' |

_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### Subject

> The multilanguage subject (or title) of this process instance. [Required] [Filter(eq;like)]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  


## Reference Details

### Process

> The process on which this instance is based. [Required] [Filter(multi eq)]

_Type_: **[Systems.Bpm.Processes](Systems.Bpm.Processes.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Systems.Bpm.ProcessInstances erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Systems.Bpm.ProcessInstances erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Systems.Bpm.ProcessInstances erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Systems_Bpm_ProcessInstances?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Systems_Bpm_ProcessInstances?$top=10>

