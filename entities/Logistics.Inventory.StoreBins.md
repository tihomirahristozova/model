---
uid: Logistics.Inventory.StoreBins
---
# Logistics.Inventory.StoreBins Entity

The storage locations within a store. If there are no differentiated storage locations, create only one, called “(Default)” or similar. Entity: Inv_Store_Bins

Default Display Text Format:  
_{Name:T}_  
Default Search Member:  
_Name_  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Logistics.Inventory.StoreBins.md#id) | guid |  
| [IsDefault](Logistics.Inventory.StoreBins.md#isdefault) | boolean | True, when this is the default storage bin for the specified store. [Required] [Default(false)] 
| [Name](Logistics.Inventory.StoreBins.md#name) | string | Name of the store bin. [Required] [Filter(like)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [BlockedForParty](Logistics.Inventory.StoreBins.md#blockedforparty) | [Parties](General.Contacts.Parties.md) (nullable) | If not null, the goods can only be used by the specified party. [Filter(multi eq)] |
| [Store](Logistics.Inventory.StoreBins.md#store) | [Stores](Logistics.Inventory.Stores.md) | The id of the containing store. [Required] [Filter(multi eq)] [Owner] |


## Attribute Details

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### IsDefault

True, when this is the default storage bin for the specified store. [Required] [Default(false)]

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### Name

Name of the store bin. [Required] [Filter(like)]

_Type_: **string**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  


## Reference Details

### BlockedForParty

If not null, the goods can only be used by the specified party. [Filter(multi eq)]

_Type_: **[Parties](General.Contacts.Parties.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### Store

The id of the containing store. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Stores](Logistics.Inventory.Stores.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Logistics.Inventory.StoreBins erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Logistics.Inventory.StoreBins erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_Inventory_StoreBins?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_Inventory_StoreBins?$top=10>

