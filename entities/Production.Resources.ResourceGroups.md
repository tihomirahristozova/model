---
uid: Production.Resources.ResourceGroups
---
# Production.Resources.ResourceGroups Entity

Groups of resource types. Entity: Prd_Resource_Groups

Default Display Text Format:  
_{Name:T}_  
Default Search Member:  
_Name_  

Aggregate Tree:  
* [Production.Resources.ResourceGroups](Production.Resources.ResourceGroups.md)  
  * [Production.Resources.Resources](Production.Resources.Resources.md)  
    * [Production.Resources.ResourceFunctions](Production.Resources.ResourceFunctions.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [FullPath](Production.Resources.ResourceGroups.md#fullpath) | string | The full path to the operation group. The full path starts with, ends with and is delimited by the "/" (forward slash) character. [Required] [Default("")] [Filter(like)] 
| [Id](Production.Resources.ResourceGroups.md#id) | guid |  
| [Name](Production.Resources.ResourceGroups.md#name) | string | Name of resource group. [Required] [Filter(like)] 
| [Parent](Production.Resources.ResourceGroups.md#parent) | string | Dot-separated list of parent groups. It also contains leading and trailing dot. [Required] [Default("/")] [Filter(like)] [ORD] 

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Resources | [Resources](Production.Resources.Resources.md) | List of [Resource](Production.Resources.Resources.md) child objects, based on the [Production.Resources.Resource.ResourceGroup](Production.Resources.Resources.md#resourcegroup) back reference 


## Attribute Details

### FullPath

The full path to the operation group. The full path starts with, ends with and is delimited by the "/" (forward slash) character. [Required] [Default("")] [Filter(like)]

_Type_: **string**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  
_Default Value_: ****  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

Name of resource group. [Required] [Filter(like)]

_Type_: **string**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### Parent

Dot-separated list of parent groups. It also contains leading and trailing dot. [Required] [Default("/")] [Filter(like)] [ORD]

_Type_: **string**  
_Indexed_: **True**  
_Supported Filters_: **Like**  
_Supports Order By_: **True**  
_Default Value_: **/**  



## Business Rules

[!list erp.entity=Production.Resources.ResourceGroups erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Production.Resources.ResourceGroups erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Production_Resources_ResourceGroups?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Production_Resources_ResourceGroups?$top=10>

