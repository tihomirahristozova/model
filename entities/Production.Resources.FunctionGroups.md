---
uid: Production.Resources.FunctionGroups
---
# Production.Resources.FunctionGroups Entity

**Namespace:** [Production.Resources](Production.Resources.md)  

Represents the hierarchy of the function groups. They group the multitude of resource functions in logical, user-defined groups. Entity: Prd_Function_Groups

## Default Visualization
Default Display Text Format:  
_{Name:T}_  
Default Search Member:  
_Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Production.Resources.FunctionGroups](Production.Resources.FunctionGroups.md)  
  * [Production.Resources.Functions](Production.Resources.Functions.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [FullPath](Production.Resources.FunctionGroups.md#fullpath) | string | The full path of the item. [Required] [Default("")] [Filter(eq;like)] 
| [Id](Production.Resources.FunctionGroups.md#id) | guid |  
| [Name](Production.Resources.FunctionGroups.md#name) | string | The name of this FunctionGroup. [Required] [Filter(like)] 
| [Parent](Production.Resources.FunctionGroups.md#parent) | string | The path of the parent item. [Required] [Default("/")] [Filter(eq;like)] [ORD] 

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Functions | [Functions](Production.Resources.Functions.md) | List of [Function](Production.Resources.Functions.md) child objects, based on the [Production.Resources.Function.FunctionGroup](Production.Resources.Functions.md#functiongroup) back reference 


## Attribute Details

### FullPath

The full path of the item. [Required] [Default("")] [Filter(eq;like)]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  
_Default Value_: ****  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

The name of this FunctionGroup. [Required] [Filter(like)]

_Type_: **string**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### Parent

The path of the parent item. [Required] [Default("/")] [Filter(eq;like)] [ORD]

_Type_: **string**  
_Indexed_: **True**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  
_Default Value_: **/**  



## Business Rules

[!list erp.entity=Production.Resources.FunctionGroups erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Production.Resources.FunctionGroups erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Production_Resources_FunctionGroups?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Production_Resources_FunctionGroups?$top=10>

