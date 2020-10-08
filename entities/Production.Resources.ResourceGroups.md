---
uid: Production.Resources.ResourceGroups
---
# Production.Resources.ResourceGroups

Groups of resource types. Entity: Prd_Resource_Groups

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Production.Resources.ResourceGroups.md#Id) | guid |  
| [FullPath](Production.Resources.ResourceGroups.md#FullPath) | string | The full path to the operation group. The full path starts with, ends with and is delimited by the "/" (forward slash) character. [Required] [Default("")] [Filter(like)] 
| [Parent](Production.Resources.ResourceGroups.md#Parent) | string | Dot-separated list of parent groups. It also contains leading and trailing dot. [Required] [Default("/")] [Filter(like)] [ORD] 
| [Name](Production.Resources.ResourceGroups.md#Name) | string | Name of resource group. [Required] [Filter(like)] 

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Resources | [Production.Resources.Resources](Production.Resources.Resources.md) | List of [Resource](Production.Resources.Resources.md) child objects, based on the [Production.Resources.Resource.ResourceGroup](Production.Resources.Resources.md#ResourceGroup) back reference 


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

### Parent

> Dot-separated list of parent groups. It also contains leading and trailing dot. [Required] [Default("/")] [Filter(like)] [ORD]

_Type_: **string**  
_Supported Filters_: **Like**  
_Supports Order By_: **True**  
_Default Value_: **/**  

### Name

> Name of resource group. [Required] [Filter(like)]

_Type_: **string**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Production.Resources.ResourceGroups erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Production.Resources.ResourceGroups erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Production.Resources.ResourceGroups erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Production_Resources_ResourceGroups?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Production_Resources_ResourceGroups?$top=10>

