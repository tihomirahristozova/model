---
uid: General.Folders
---
# General.Folders Entity

**Namespace:** [General](General.md)  

Folders are the base for the file storage within the system. Each folder is a data object, with the primary idea of containing files. Entity: Gen_Folders (Introduced in version 21.1.1.8)

## Default Visualization
Default Display Text Format:  
_{Name:T}_  
Default Search Member:  
_Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [General.Folders](General.Folders.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](General.Folders.md#id) | guid |  
| [Name](General.Folders.md#name) | string | Name of the folder. Unique within its parent folder. `Required` `Filter(multi eq;like)` 
| [Notes](General.Folders.md#notes) | string (nullable) | Notes for this Folder. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [AccessKey](General.Folders.md#accesskey) | [AccessKeys](Systems.Security.AccessKeys.md) (nullable) | The access key, required to unlock the folder contents. null means the folder is unprotected and accessible to all internal users. `Filter(multi eq)` |
| [Parent](General.Folders.md#parent) | [Folders](General.Folders.md) (nullable) | Parent folder. null if this is root folder. `Filter(multi eq)` |


## Attribute Details

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

Name of the folder. Unique within its parent folder. `Required` `Filter(multi eq;like)`

_Type_: **string**  
_Supported Filters_: **Equals, Like, EqualsIn**  
_Supports Order By_: **False**  

### Notes

Notes for this Folder.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### AccessKey

The access key, required to unlock the folder contents. null means the folder is unprotected and accessible to all internal users. `Filter(multi eq)`

_Type_: **[AccessKeys](Systems.Security.AccessKeys.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### Parent

Parent folder. null if this is root folder. `Filter(multi eq)`

_Type_: **[Folders](General.Folders.md) (nullable)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=General.Folders erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.Folders erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_Folders?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_Folders?$top=10>

