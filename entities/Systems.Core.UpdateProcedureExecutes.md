---
uid: Systems.Core.UpdateProcedureExecutes
---
# Systems.Core.UpdateProcedureExecutes Entity

**Namespace:** [Systems.Core](Systems.Core.md)  

Contains data about the execution of Upgrade Procedures. Contains status messages and ensures that each procedure is executed only once. Entity: Sys_Update_Procedure_Executes

## Default Visualization
Default Display Text Format:  
_{Id}: {ObjectVersion}_  
Default Search Members:  
__  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Systems.Core.UpdateProcedureExecutes](Systems.Core.UpdateProcedureExecutes.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [ExecuteTime](Systems.Core.UpdateProcedureExecutes.md#executetime) | datetime | The time, when the update procedure was executed. `Required` `Default(Now)` 
| [Id](Systems.Core.UpdateProcedureExecutes.md#id) | guid |  
| [ObjectVersion](Systems.Core.UpdateProcedureExecutes.md#objectversion) | int32 |  
| [ResultMessage](Systems.Core.UpdateProcedureExecutes.md#resultmessage) | string (1024) __nullable__ | Error or success message. 
| [Successful](Systems.Core.UpdateProcedureExecutes.md#successful) | boolean | True when the execution was successfull. `Required` `Default(true)` 
| [UpdateProcedure](Systems.Core.UpdateProcedureExecutes.md#updateprocedure) | string (128) | The system name of the executed update procedure. `Required` 


## Attribute Details

### ExecuteTime

The time, when the update procedure was executed. `Required` `Default(Now)`

_Type_: **datetime**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **CurrentDateTime**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### ObjectVersion

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  

### ResultMessage

Error or success message.

_Type_: **string (1024) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **1024**  

### Successful

True when the execution was successfull. `Required` `Default(true)`

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### UpdateProcedure

The system name of the executed update procedure. `Required`

_Type_: **string (128)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **128**  


## API Methods

Methods that can be invoked in public APIs.

### GetAllowedCustomPropertyValues

Gets the allowed values for the specified custom property for this entity object.              If supported the result is ordered by property value. Some property value sources does not support ordering.  
_Return Type_: **Collection Of [CustomPropertyValue](../data-types.md#general.custompropertyvalue)**  
_Declaring Type_: **EntityObject**  
_Domain API Request_: **GET**  

**Parameters**  
  * **customPropertyCode**  
    The code of the custom property  
    _Type_: string  

  * **search**  
    The search text - searches by value or description  
    _Type_: string  
     _Optional_: True  
    _Default Value_: null  

  * **exactMatch**  
    If true the search text should be equal to the property value  
    _Type_: boolean  
     _Optional_: True  
    _Default Value_: False  

  * **orderByDescription**  
    If true the result is ordered by Description instead of Value. Note that ordering is not always possible.  
    _Type_: boolean  
     _Optional_: True  
    _Default Value_: False  

  * **top**  
    The top clause - default is 10  
    _Type_: int32  
     _Optional_: True  
    _Default Value_: 10  

  * **skip**  
    The skip clause - default is 0  
    _Type_: int32  
     _Optional_: True  
    _Default Value_: 0  



## Business Rules

[!list limit=1000 erp.entity=Systems.Core.UpdateProcedureExecutes erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Systems.Core.UpdateProcedureExecutes erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Systems_Core_UpdateProcedureExecutes?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Systems_Core_UpdateProcedureExecutes?$top=10>

