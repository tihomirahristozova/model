---
uid: Logistics.Inventory.ProductValuationGroups
---
# Logistics.Inventory.ProductValuationGroups Entity

Contains the available valuation groups for products. They are used in reconciliations, where all pluses and minuses within a valuation group are allowed to balance each other without fiscal effects. Without valuation groups, each product is balanced for itself and taxes are calculated for each surplus. Entity: Inv_Product_Valuation_Groups

Default Display Text Format:  
_{ValuationGroupCode}: {ValuationGroupName:T}_  
Default Search Member:  
_ValuationGroupCode_  

Aggregate Tree:  
* [Logistics.Inventory.ProductValuationGroups](Logistics.Inventory.ProductValuationGroups.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Description](Logistics.Inventory.ProductValuationGroups.md#description) | string (nullable) | The description of this ProductValuationGroup. [Filter(like)] 
| [Id](Logistics.Inventory.ProductValuationGroups.md#id) | guid |  
| [ValuationGroupCode](Logistics.Inventory.ProductValuationGroups.md#valuationgroupcode) | string | The unique code of the product valuation group. [Required] [Filter(eq;like)] [ORD] 
| [ValuationGroupName](Logistics.Inventory.ProductValuationGroups.md#valuationgroupname) | [MultilanguageString](../data-types.md#multilanguagestring) | The name of the product valuation group. [Required] [Filter(eq;like)] 


## Attribute Details

### Description

The description of this ProductValuationGroup. [Filter(like)]

_Type_: **string (nullable)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### ValuationGroupCode

The unique code of the product valuation group. [Required] [Filter(eq;like)] [ORD]

_Type_: **string**  
_Indexed_: **True**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  

### ValuationGroupName

The name of the product valuation group. [Required] [Filter(eq;like)]

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Logistics.Inventory.ProductValuationGroups erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Logistics.Inventory.ProductValuationGroups erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_Inventory_ProductValuationGroups?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_Inventory_ProductValuationGroups?$top=10>

