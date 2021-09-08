---
uid: General.Products.VariantColors
---
# General.Products.VariantColors Entity

**Namespace:** [General.Products](General.Products.md)  

Contains the different colors, which can be assigned to product variants. Entity: Gen_Variant_Colors

## Default Visualization
Default Display Text Format:  
_{Name:T} #{Code}_  
Default Search Member:  
_Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [General.Products.VariantColors](General.Products.VariantColors.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Code](General.Products.VariantColors.md#code) | string (8) | Unique code of the color. Used to generate parts of bar-codes and in other coding schemes. `Required` `Filter(eq;like)` `ORD` 
| [Id](General.Products.VariantColors.md#id) | guid |  
| [Name](General.Products.VariantColors.md#name) | [MultilanguageString](../data-types.md#multilanguagestring) | The name of this VariantColor. `Required` `Filter(eq;like)` `ORD` 


## Attribute Details

### Code

Unique code of the color. Used to generate parts of bar-codes and in other coding schemes. `Required` `Filter(eq;like)` `ORD`

_Type_: **string (8)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  
_Maximum Length_: **8**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

The name of this VariantColor. `Required` `Filter(eq;like)` `ORD`

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  



## Business Rules

[!list limit=1000 erp.entity=General.Products.VariantColors erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=General.Products.VariantColors erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_Products_VariantColors?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_Products_VariantColors?$top=10>

