---
uid: Systems.Core.UpdateProcedureExecutes
---
# Systems.Core.UpdateProcedureExecutes Entity

**Namespace:** [Systems.Core](Systems.Core.md)  

Contains data about the execution of Upgrade Procedures. Contains status messages and ensures that each procedure is executed only once. Entity: Sys_Update_Procedure_Executes

## Default Visualization
Default Display Text Format:  
_{Id}_  
Default Search Member:  
_Id_  

## Aggregate
  @aggregates  
Aggregate Tree  
* [Systems.Core.UpdateProcedureExecutes](Systems.Core.UpdateProcedureExecutes.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [ExecuteTime](Systems.Core.UpdateProcedureExecutes.md#executetime) | datetime | The time, when the update procedure was executed. [Required] [Default(Now)] 
| [Id](Systems.Core.UpdateProcedureExecutes.md#id) | guid |  
| [ResultMessage](Systems.Core.UpdateProcedureExecutes.md#resultmessage) | string (nullable) | Error or success message. 
| [Successful](Systems.Core.UpdateProcedureExecutes.md#successful) | boolean | True when the execution was successfull. [Required] [Default(true)] 
| [UpdateProcedure](Systems.Core.UpdateProcedureExecutes.md#updateprocedure) | string | The system name of the executed update procedure. [Required] 


## Attribute Details

### ExecuteTime

The time, when the update procedure was executed. [Required] [Default(Now)]

_Type_: **datetime**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **CurrentDateTime**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### ResultMessage

Error or success message.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Successful

True when the execution was successfull. [Required] [Default(true)]

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### UpdateProcedure

The system name of the executed update procedure. [Required]

_Type_: **string**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Systems.Core.UpdateProcedureExecutes erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Systems.Core.UpdateProcedureExecutes erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Systems_Core_UpdateProcedureExecutes?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Systems_Core_UpdateProcedureExecutes?$top=10>

