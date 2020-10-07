# Production.Resources.FunctionGroups

Represents the hierarchy of the function groups. They group the multitude of resource functions in logical, user-defined groups. Entity: Prd_Function_Groups

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Production.Resources.FunctionGroups.md#Id) | guid |  
| [FullPath](Production.Resources.FunctionGroups.md#FullPath) | string | The full path of the item. [Required] [Default("")] [Filter(eq;like)] 
| [Name](Production.Resources.FunctionGroups.md#Name) | string | The name of this FunctionGroup. [Required] [Filter(like)] 
| [Parent](Production.Resources.FunctionGroups.md#Parent) | string | The path of the parent item. [Required] [Default("/")] [Filter(eq;like)] [ORD] 

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Functions | [Production.Resources.Functions](Production.Resources.Functions.md) | List of [Function](Production.Resources.Functions.md) child objects, based on the [Production.Resources.Function.FunctionGroup](Production.Resources.Functions.md#FunctionGroup) back reference 


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### FullPath

> The full path of the item. [Required] [Default("")] [Filter(eq;like)]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  
_Default Value_: ****  

### Name

> The name of this FunctionGroup. [Required] [Filter(like)]

_Type_: **string**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### Parent

> The path of the parent item. [Required] [Default("/")] [Filter(eq;like)] [ORD]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  
_Default Value_: **/**  



## Business Rules

[!list erp.entity=Production.Resources.FunctionGroups erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Production.Resources.FunctionGroups erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Production.Resources.FunctionGroups erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Production_Resources_FunctionGroups?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Production_Resources_FunctionGroups?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Prd_Function_Groups?$top=10>

