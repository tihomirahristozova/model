# Logistics.Inventory.StoreGroups

Hierarchy of store groups. Entity: Inv_Store_Groups

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Logistics.Inventory.StoreGroups.md#Id) | guid |  
| [FullPath](Logistics.Inventory.StoreGroups.md#FullPath) | string (nullable) | The full path to the store group in a dot separated, non-leading dot format. For example: 001.005.008. [Filter(eq;like)] [ORD] [ReadOnly] 
| [ParentFullPath](Logistics.Inventory.StoreGroups.md#ParentFullPath) | string (nullable) | The full path to the parent store group. It is stored in a dot separated, non-leading dot format. For example: 001.005. [Filter(eq;like)] 
| [Code](Logistics.Inventory.StoreGroups.md#Code) | string | The unique code of the StoreGroup. [Required] [Filter(eq;like)] 
| [Name](Logistics.Inventory.StoreGroups.md#Name) | [MultilanguageString](../data-types/MultilanguageString.md) | The name of this StoreGroup. [Required] [Filter(like)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [EnterpriseCompany](Logistics.Inventory.StoreGroups.md#EnterpriseCompany) | [General.EnterpriseCompanies](General.EnterpriseCompanies.md) (nullable) | The Enterprise Company to which this StoreGroup applies, or null if it is for all enterprise companies. [Filter(multi eq)] |
| [EnterpriseCompanyLocation](Logistics.Inventory.StoreGroups.md#EnterpriseCompanyLocation) | [General.Contacts.CompanyLocations](General.Contacts.CompanyLocations.md) (nullable) | The Enterprise Company Location to which this StoreGroup applies, or null if it is for all enterprise company locations. [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### FullPath

> The full path to the store group in a dot separated, non-leading dot format. For example: 001.005.008. [Filter(eq;like)] [ORD] [ReadOnly]

_Type_: **string (nullable)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  

### ParentFullPath

> The full path to the parent store group. It is stored in a dot separated, non-leading dot format. For example: 001.005. [Filter(eq;like)]

_Type_: **string (nullable)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### Code

> The unique code of the StoreGroup. [Required] [Filter(eq;like)]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### Name

> The name of this StoreGroup. [Required] [Filter(like)]

_Type_: **[MultilanguageString](../data-types/MultilanguageString.md)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  


## Reference Details

### EnterpriseCompany

> The Enterprise Company to which this StoreGroup applies, or null if it is for all enterprise companies. [Filter(multi eq)]

_Type_: **[General.EnterpriseCompanies](General.EnterpriseCompanies.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### EnterpriseCompanyLocation

> The Enterprise Company Location to which this StoreGroup applies, or null if it is for all enterprise company locations. [Filter(multi eq)]

_Type_: **[General.Contacts.CompanyLocations](General.Contacts.CompanyLocations.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Logistics.Inventory.StoreGroups erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Logistics.Inventory.StoreGroups erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Logistics.Inventory.StoreGroups erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_Inventory_StoreGroups?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_Inventory_StoreGroups?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Inv_Store_Groups?$top=10>

