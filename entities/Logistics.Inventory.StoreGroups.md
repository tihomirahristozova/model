---
uid: Logistics.Inventory.StoreGroups
---
# Logistics.Inventory.StoreGroups Entity

**Namespace:** [Logistics.Inventory](Logistics.Inventory.md)  

Hierarchy of store groups. Entity: Inv_Store_Groups

## Default Visualization
Default Display Text Format:  
_{Name:T} #{Code}_  
Default Search Member:  
_Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Logistics.Inventory.StoreGroups](Logistics.Inventory.StoreGroups.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Code](Logistics.Inventory.StoreGroups.md#code) | string (16) | The unique code of the StoreGroup. `Required` `Filter(eq;like)` 
| [FullPath](Logistics.Inventory.StoreGroups.md#fullpath) | string (25) __nullable__ | The full path to the store group in a dot separated, non-leading dot format. For example: 001.005.008. `Filter(eq;like)` `ORD` `ReadOnly` 
| [Id](Logistics.Inventory.StoreGroups.md#id) | guid |  
| [Name](Logistics.Inventory.StoreGroups.md#name) | [MultilanguageString](../data-types.md#multilanguagestring) | The name of this StoreGroup. `Required` `Filter(like)` 
| [ParentFullPath](Logistics.Inventory.StoreGroups.md#parentfullpath) | string (25) __nullable__ | The full path to the parent store group. It is stored in a dot separated, non-leading dot format. For example: 001.005. `Filter(eq;like)` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [EnterpriseCompany](Logistics.Inventory.StoreGroups.md#enterprisecompany) | [EnterpriseCompanies](General.EnterpriseCompanies.md) (nullable) | The Enterprise Company to which this StoreGroup applies, or null if it is for all enterprise companies. `Filter(multi eq)` |
| [EnterpriseCompanyLocation](Logistics.Inventory.StoreGroups.md#enterprisecompanylocation) | [CompanyLocations](General.Contacts.CompanyLocations.md) (nullable) | The Enterprise Company Location to which this StoreGroup applies, or null if it is for all enterprise company locations. `Filter(multi eq)` |


## Attribute Details

### Code

The unique code of the StoreGroup. `Required` `Filter(eq;like)`

_Type_: **string (16)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  
_Maximum Length_: **16**  

### FullPath

The full path to the store group in a dot separated, non-leading dot format. For example: 001.005.008. `Filter(eq;like)` `ORD` `ReadOnly`

_Type_: **string (25) __nullable__**  
_Indexed_: **True**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  
_Maximum Length_: **25**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

The name of this StoreGroup. `Required` `Filter(like)`

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### ParentFullPath

The full path to the parent store group. It is stored in a dot separated, non-leading dot format. For example: 001.005. `Filter(eq;like)`

_Type_: **string (25) __nullable__**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  
_Maximum Length_: **25**  


## Reference Details

### EnterpriseCompany

The Enterprise Company to which this StoreGroup applies, or null if it is for all enterprise companies. `Filter(multi eq)`

_Type_: **[EnterpriseCompanies](General.EnterpriseCompanies.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### EnterpriseCompanyLocation

The Enterprise Company Location to which this StoreGroup applies, or null if it is for all enterprise company locations. `Filter(multi eq)`

_Type_: **[CompanyLocations](General.Contacts.CompanyLocations.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list limit=1000 erp.entity=Logistics.Inventory.StoreGroups erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Logistics.Inventory.StoreGroups erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_Inventory_StoreGroups?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_Inventory_StoreGroups?$top=10>

