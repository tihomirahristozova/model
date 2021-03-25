---
uid: Production.Resources.OperationGroups
---
# Production.Resources.OperationGroups Entity

**Namespace:** [Production.Resources](Production.Resources.md)  

Groups of operations. Entity: Prd_Operation_Groups

## Default Visualization
Default Display Text Format:  
_{Name:T}_  
Default Search Member:  
_Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Production.Resources.OperationGroups](Production.Resources.OperationGroups.md)  
  * [Production.Resources.Operations](Production.Resources.Operations.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [FullPath](Production.Resources.OperationGroups.md#fullpath) | string(254) | The full path to the operation group. The full path starts with, ends with and is delimited by the "/" (forward slash) character. `Required` `Default("")` `Filter(like)` 
| [Id](Production.Resources.OperationGroups.md#id) | guid |  
| [Name](Production.Resources.OperationGroups.md#name) | string(64) | The name of this OperationGroup. `Required` `Filter(like)` 
| [Parent](Production.Resources.OperationGroups.md#parent) | string(254) | Path of parent group. `Required` `Default("/")` `Filter(like)` `ORD` 

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Operations | [Operations](Production.Resources.Operations.md) | List of `Operation`(Production.Resources.Operations.md) child objects, based on the `Production.Resources.Operation.OperationGroup`(Production.Resources.Operations.md#operationgroup) back reference 


## Attribute Details

### FullPath

The full path to the operation group. The full path starts with, ends with and is delimited by the "/" (forward slash) character. `Required` `Default("")` `Filter(like)`

_Type_: **string(254)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  
_Default Value_: ****  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

The name of this OperationGroup. `Required` `Filter(like)`

_Type_: **string(64)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  
_Maximum Length_: **64**  

### Parent

Path of parent group. `Required` `Default("/")` `Filter(like)` `ORD`

_Type_: **string(254)**  
_Indexed_: **True**  
_Supported Filters_: **Like**  
_Supports Order By_: **True**  
_Maximum Length_: **254**  
_Default Value_: **/**  



## Business Rules

[!list erp.entity=Production.Resources.OperationGroups erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Production.Resources.OperationGroups erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Production_Resources_OperationGroups?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Production_Resources_OperationGroups?$top=10>

