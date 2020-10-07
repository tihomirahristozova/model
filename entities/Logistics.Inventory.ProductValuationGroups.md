# Logistics.Inventory.ProductValuationGroups

Contains the available valuation groups for products. They are used in reconciliations, where all pluses and minuses within a valuation group are allowed to balance each other without fiscal effects. Without valuation groups, each product is balanced for itself and taxes are calculated for each surplus. Entity: Inv_Product_Valuation_Groups

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Logistics.Inventory.ProductValuationGroups.md#Id) | guid |  
| [Description](Logistics.Inventory.ProductValuationGroups.md#Description) | string (nullable) | The description of this ProductValuationGroup. [Filter(like)] 
| [ValuationGroupCode](Logistics.Inventory.ProductValuationGroups.md#ValuationGroupCode) | string | The unique code of the product valuation group. [Required] [Filter(eq;like)] [ORD] 
| [ValuationGroupName](Logistics.Inventory.ProductValuationGroups.md#ValuationGroupName) | [MultilanguageString](../data-types/MultilanguageString.md) | The name of the product valuation group. [Required] [Filter(eq;like)] 


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### Description

> The description of this ProductValuationGroup. [Filter(like)]

_Type_: **string (nullable)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### ValuationGroupCode

> The unique code of the product valuation group. [Required] [Filter(eq;like)] [ORD]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  

### ValuationGroupName

> The name of the product valuation group. [Required] [Filter(eq;like)]

_Type_: **[MultilanguageString](../data-types/MultilanguageString.md)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Logistics.Inventory.ProductValuationGroups erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Logistics.Inventory.ProductValuationGroups erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Logistics.Inventory.ProductValuationGroups erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_Inventory_ProductValuationGroups?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_Inventory_ProductValuationGroups?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Inv_Product_Valuation_Groups?$top=10>

