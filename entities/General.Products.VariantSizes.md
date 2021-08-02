---
uid: General.Products.VariantSizes
---
# General.Products.VariantSizes Entity

**Namespace:** [General.Products](General.Products.md)  

Contains the different sizes, which can be assigned to product variants. Entity: Gen_Variant_Sizes

## Default Visualization
Default Display Text Format:  
_{Code}: {Name:T}_  
Default Search Member:  
_Code_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [General.Products.VariantSizes](General.Products.VariantSizes.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Code](General.Products.VariantSizes.md#code) | string (8) | Unique code of the size. Used to generate parts of bar-codes and in other coding schemes. `Required` `Filter(eq;like)` `ORD` 
| [Id](General.Products.VariantSizes.md#id) | guid |  
| [Name](General.Products.VariantSizes.md#name) | [MultilanguageString](../data-types.md#multilanguagestring) | The name of the variant size. `Required` `Filter(eq;like)` `ORD` 


## Attribute Details

### Code

Unique code of the size. Used to generate parts of bar-codes and in other coding schemes. `Required` `Filter(eq;like)` `ORD`

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

The name of the variant size. `Required` `Filter(eq;like)` `ORD`

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  



## Business Rules

[!list limit=1000 erp.entity=General.Products.VariantSizes erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=General.Products.VariantSizes erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_Products_VariantSizes?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_Products_VariantSizes?$top=10>

