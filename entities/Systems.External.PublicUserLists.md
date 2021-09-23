---
uid: Systems.External.PublicUserLists
---
# Systems.External.PublicUserLists Entity

**Namespace:** [Systems.External](Systems.External.md)  

Each list represents a unique collection of public users. Entity: Ext_Public_User_Lists

## Default Visualization
Default Display Text Format:  
_{Name:T}_  
Default Search Member:  
__  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Systems.External.PublicUserLists](Systems.External.PublicUserLists.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Systems.External.PublicUserLists.md#id) | guid |  
| [Name](Systems.External.PublicUserLists.md#name) | string (64) | The name of this PublicUserList. `Required` `Filter(like)` 
| [Notes](Systems.External.PublicUserLists.md#notes) | string (max) __nullable__ | Notes for this PublicUserList. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [EnterpriseCompany](Systems.External.PublicUserLists.md#enterprisecompany) | [EnterpriseCompanies](General.EnterpriseCompanies.md) (nullable) | The enterprise company to which this list belongs. Null means that the list is available to services offered by all enterprise companies. `Filter(multi eq)` |


## Attribute Details

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

The name of this PublicUserList. `Required` `Filter(like)`

_Type_: **string (64)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  
_Maximum Length_: **64**  

### Notes

Notes for this PublicUserList.

_Type_: **string (max) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  


## Reference Details

### EnterpriseCompany

The enterprise company to which this list belongs. Null means that the list is available to services offered by all enterprise companies. `Filter(multi eq)`

_Type_: **[EnterpriseCompanies](General.EnterpriseCompanies.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list limit=1000 erp.entity=Systems.External.PublicUserLists erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Systems.External.PublicUserLists erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Systems_External_PublicUserLists?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Systems_External_PublicUserLists?$top=10>

