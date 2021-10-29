---
uid: General.DocumentPartyRoles
---
# General.DocumentPartyRoles Entity

**Namespace:** [General](General.md)  

Represents the different roles of parties which are associated to the documents. Entity: Gen_Document_Party_Roles (Introduced in version 22.1.4.45)

## Default Visualization
Default Display Text Format:  
_{Name}_  
Default Search Member:  
__  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [General.DocumentPartyRoles](General.DocumentPartyRoles.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Code](General.DocumentPartyRoles.md#code) | string (32) | The code of the role. `Required` `ORD` 
| [Id](General.DocumentPartyRoles.md#id) | guid |  
| [Name](General.DocumentPartyRoles.md#name) | string (254) | Party role name. `Required` 
| [Notes](General.DocumentPartyRoles.md#notes) | string (512) __nullable__ | Notes for this DocumentPartyRole. 


## Attribute Details

### Code

The code of the role. `Required` `ORD`

_Type_: **string (32)**  
_Indexed_: **True**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **True**  
_Maximum Length_: **32**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

Party role name. `Required`

_Type_: **string (254)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  

### Notes

Notes for this DocumentPartyRole.

_Type_: **string (512) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **512**  



## Business Rules

[!list limit=1000 erp.entity=General.DocumentPartyRoles erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=General.DocumentPartyRoles erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_DocumentPartyRoles?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_DocumentPartyRoles?$top=10>

