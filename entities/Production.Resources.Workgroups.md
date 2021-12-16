---
uid: Production.Resources.Workgroups
---
# Production.Resources.Workgroups Entity

**Namespace:** [Production.Resources](Production.Resources.md)  

Production workgroups. Entity: Prd_Workgroups

## Default Visualization
Default Display Text Format:  
_{Name}_  
Default Search Members:  
_Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Production.Resources.Workgroups](Production.Resources.Workgroups.md)  
  * [Production.Resources.WorkgroupResources](Production.Resources.WorkgroupResources.md)  
    * [Production.Resources.Capacity](Production.Resources.Capacity.md)  
  * [Production.Resources.WorkgroupShifts](Production.Resources.WorkgroupShifts.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [FullPath](Production.Resources.Workgroups.md#fullpath) | string (254) __nullable__ | The full path to the current node, represented with slash ('/') as leading, trailing and separator character. Example: '/rootnode/subnode/'. `Default("")` 
| [Id](Production.Resources.Workgroups.md#id) | guid |  
| [Name](Production.Resources.Workgroups.md#name) | string (64) | Name of the workgroup. `Required` `Filter(like)` 
| [Notes](Production.Resources.Workgroups.md#notes) | string (254) __nullable__ | User notes for the workgroup. 
| [Parent](Production.Resources.Workgroups.md#parent) | string (255) | Path-like parent workgroup name. `Required` `Default("/")` `Filter(like)` `ORD` 
| [RowVersion](Production.Resources.Workgroups.md#rowversion) | byte[] |  

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Resources | [WorkgroupResources](Production.Resources.WorkgroupResources.md) | List of `WorkgroupResource`(Production.Resources.WorkgroupResources.md) child objects, based on the `Production.Resources.WorkgroupResource.Workgroup`(Production.Resources.WorkgroupResources.md#workgroup) back reference 
| Shifts | [WorkgroupShifts](Production.Resources.WorkgroupShifts.md) | List of `WorkgroupShift`(Production.Resources.WorkgroupShifts.md) child objects, based on the `Production.Resources.WorkgroupShift.Workgroup`(Production.Resources.WorkgroupShifts.md#workgroup) back reference 


## Attribute Details

### FullPath

The full path to the current node, represented with slash ('/') as leading, trailing and separator character. Example: '/rootnode/subnode/'. `Default("")`

_Type_: **string (254) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  
_Default Value_: ****  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

Name of the workgroup. `Required` `Filter(like)`

_Type_: **string (64)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  
_Maximum Length_: **64**  

### Notes

User notes for the workgroup.

_Type_: **string (254) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  

### Parent

Path-like parent workgroup name. `Required` `Default("/")` `Filter(like)` `ORD`

_Type_: **string (255)**  
_Indexed_: **True**  
_Supported Filters_: **Like**  
_Supports Order By_: **True**  
_Maximum Length_: **255**  
_Default Value_: **/**  

### RowVersion

_Type_: **byte[]**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  



## Business Rules

[!list limit=1000 erp.entity=Production.Resources.Workgroups erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Production.Resources.Workgroups erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Production_Resources_Workgroups?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Production_Resources_Workgroups?$top=10>

