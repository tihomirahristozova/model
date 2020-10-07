# Production.Resources.OperationGroups

Groups of operations. Entity: Prd_Operation_Groups

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Production.Resources.OperationGroups.md#Id) | guid |  
| [FullPath](Production.Resources.OperationGroups.md#FullPath) | string | The full path to the operation group. The full path starts with, ends with and is delimited by the "/" (forward slash) character. [Required] [Default("")] [Filter(like)] 
| [Name](Production.Resources.OperationGroups.md#Name) | string | The name of this OperationGroup. [Required] [Filter(like)] 
| [Parent](Production.Resources.OperationGroups.md#Parent) | string | Path of parent group. [Required] [Default("/")] [Filter(like)] [ORD] 

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Operations | [Production.Resources.Operations](Production.Resources.Operations.md) | List of [Operation](Production.Resources.Operations.md) child objects, based on the [Production.Resources.Operation.OperationGroup](Production.Resources.Operations.md#OperationGroup) back reference 


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### FullPath

> The full path to the operation group. The full path starts with, ends with and is delimited by the "/" (forward slash) character. [Required] [Default("")] [Filter(like)]

_Type_: **string**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  
_Default Value_: ****  

### Name

> The name of this OperationGroup. [Required] [Filter(like)]

_Type_: **string**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### Parent

> Path of parent group. [Required] [Default("/")] [Filter(like)] [ORD]

_Type_: **string**  
_Supported Filters_: **Like**  
_Supports Order By_: **True**  
_Default Value_: **/**  



## Business Rules

[!list erp.entity=Production.Resources.OperationGroups erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Production.Resources.OperationGroups erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Production.Resources.OperationGroups erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Production_Resources_OperationGroups?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Production_Resources_OperationGroups?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Prd_Operation_Groups?$top=10>

