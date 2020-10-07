# Crm.Distribution.SalesPersonGroups

Hierarchical sales person grouping. Entity: Crm_Sales_Person_Groups

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Crm.Distribution.SalesPersonGroups.md#Id) | guid |  
| [FullPath](Crm.Distribution.SalesPersonGroups.md#FullPath) | string (nullable) | Full path to this item in the form /root/child1/../leaf/. [Filter(eq;like)] [ReadOnly] 
| [Code](Crm.Distribution.SalesPersonGroups.md#Code) | string | The unique code of the SalesPersonGroup. [Required] [Filter(eq;like)] [ORD] 
| [Name](Crm.Distribution.SalesPersonGroups.md#Name) | string | The name of this SalesPersonGroup. [Required] [Filter(eq;like)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [ManagerPerson](Crm.Distribution.SalesPersonGroups.md#ManagerPerson) | [General.Contacts.Persons](General.Contacts.Persons.md) (nullable) | The manager of the group. null when there is no manager. [Filter(multi eq)] |
| [Parent](Crm.Distribution.SalesPersonGroups.md#Parent) | [Crm.Distribution.SalesPersonGroups](Crm.Distribution.SalesPersonGroups.md) (nullable) | The parent sales person group in the hierarchy. [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### FullPath

> Full path to this item in the form /root/child1/../leaf/. [Filter(eq;like)] [ReadOnly]

_Type_: **string (nullable)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### Code

> The unique code of the SalesPersonGroup. [Required] [Filter(eq;like)] [ORD]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  

### Name

> The name of this SalesPersonGroup. [Required] [Filter(eq;like)]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  


## Reference Details

### ManagerPerson

> The manager of the group. null when there is no manager. [Filter(multi eq)]

_Type_: **[General.Contacts.Persons](General.Contacts.Persons.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Parent

> The parent sales person group in the hierarchy. [Filter(multi eq)]

_Type_: **[Crm.Distribution.SalesPersonGroups](Crm.Distribution.SalesPersonGroups.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Crm.Distribution.SalesPersonGroups erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Crm.Distribution.SalesPersonGroups erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Crm.Distribution.SalesPersonGroups erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_Distribution_SalesPersonGroups?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Crm_Distribution_SalesPersonGroups?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_Sales_Person_Groups?$top=10>

