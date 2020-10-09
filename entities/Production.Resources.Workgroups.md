---
uid: Production.Resources.Workgroups
---
# Production.Resources.Workgroups Entity

Production workgroups. Entity: Prd_Workgroups

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [FullPath](Production.Resources.Workgroups.md#fullpath) | string (nullable) | The full path to the current node, represented with slash ('/') as leading, trailing and separator character. Example: '/rootnode/subnode/'. [Default("")] 
| [Id](Production.Resources.Workgroups.md#id) | guid |  
| [Name](Production.Resources.Workgroups.md#name) | string | Name of the workgroup. [Required] [Filter(like)] 
| [Notes](Production.Resources.Workgroups.md#notes) | string (nullable) | User notes for the workgroup. 
| [Parent](Production.Resources.Workgroups.md#parent) | string | Path-like parent workgroup name. [Required] [Default("/")] [Filter(like)] [ORD] 

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Resources | [WorkgroupResources](Production.Resources.WorkgroupResources.md) | List of [WorkgroupResource](Production.Resources.WorkgroupResources.md) child objects, based on the [Production.Resources.WorkgroupResource.Workgroup](Production.Resources.WorkgroupResources.md#workgroup) back reference 
| Shifts | [WorkgroupShifts](Production.Resources.WorkgroupShifts.md) | List of [WorkgroupShift](Production.Resources.WorkgroupShifts.md) child objects, based on the [Production.Resources.WorkgroupShift.Workgroup](Production.Resources.WorkgroupShifts.md#workgroup) back reference 


## Attribute Details

### FullPath

The full path to the current node, represented with slash ('/') as leading, trailing and separator character. Example: '/rootnode/subnode/'. [Default("")]

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: ****  

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

Name of the workgroup. [Required] [Filter(like)]

_Type_: **string**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### Notes

User notes for the workgroup.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Parent

Path-like parent workgroup name. [Required] [Default("/")] [Filter(like)] [ORD]

_Type_: **string**  
_Supported Filters_: **Like**  
_Supports Order By_: **True**  
_Default Value_: **/**  



## Business Rules

[!list erp.entity=Production.Resources.Workgroups erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Production.Resources.Workgroups erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Production.Resources.Workgroups erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Production_Resources_Workgroups?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Production_Resources_Workgroups?$top=10>

