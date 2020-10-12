---
uid: Crm.Distribution.SalesPersonGroups
---
# Crm.Distribution.SalesPersonGroups Entity

Hierarchical sales person grouping. Entity: Crm_Sales_Person_Groups

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Code](Crm.Distribution.SalesPersonGroups.md#code) | string | The unique code of the SalesPersonGroup. [Required] [Filter(eq;like)] [ORD] 
| [FullPath](Crm.Distribution.SalesPersonGroups.md#fullpath) | string (nullable) | Full path to this item in the form /root/child1/../leaf/. [Filter(eq;like)] [ReadOnly] 
| [Id](Crm.Distribution.SalesPersonGroups.md#id) | guid |  
| [Name](Crm.Distribution.SalesPersonGroups.md#name) | string | The name of this SalesPersonGroup. [Required] [Filter(eq;like)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [ManagerPerson](Crm.Distribution.SalesPersonGroups.md#managerperson) | [Persons](General.Contacts.Persons.md) (nullable) | The manager of the group. null when there is no manager. [Filter(multi eq)] |
| [Parent](Crm.Distribution.SalesPersonGroups.md#parent) | [SalesPersonGroups](Crm.Distribution.SalesPersonGroups.md) (nullable) | The parent sales person group in the hierarchy. [Filter(multi eq)] |


## Attribute Details

### Code

The unique code of the SalesPersonGroup. [Required] [Filter(eq;like)] [ORD]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  

### FullPath

Full path to this item in the form /root/child1/../leaf/. [Filter(eq;like)] [ReadOnly]

_Type_: **string (nullable)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

The name of this SalesPersonGroup. [Required] [Filter(eq;like)]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  


## Reference Details

### ManagerPerson

The manager of the group. null when there is no manager. [Filter(multi eq)]

_Type_: **[Persons](General.Contacts.Persons.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### Parent

The parent sales person group in the hierarchy. [Filter(multi eq)]

_Type_: **[SalesPersonGroups](Crm.Distribution.SalesPersonGroups.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Crm.Distribution.SalesPersonGroups erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Crm.Distribution.SalesPersonGroups erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_Distribution_SalesPersonGroups?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Crm_Distribution_SalesPersonGroups?$top=10>

