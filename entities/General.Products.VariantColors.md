---
uid: General.Products.VariantColors
---
# General.Products.VariantColors Entity

Contains the different colors, which can be assigned to product variants. Entity: Gen_Variant_Colors

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Code](General.Products.VariantColors.md#code) | string | Unique code of the color. Used to generate parts of bar-codes and in other coding schemes. [Required] [Filter(eq;like)] [ORD] 
| [Id](General.Products.VariantColors.md#id) | guid |  
| [Name](General.Products.VariantColors.md#name) | [MultilanguageString](../data-types.md#multilanguagestring) | The name of this VariantColor. [Required] [Filter(eq;like)] [ORD] 


## Attribute Details

### Code

> Unique code of the color. Used to generate parts of bar-codes and in other coding schemes. [Required] [Filter(eq;like)] [ORD]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

> The name of this VariantColor. [Required] [Filter(eq;like)] [ORD]

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  



## Business Rules

[!list erp.entity=General.Products.VariantColors erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.Products.VariantColors erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=General.Products.VariantColors erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_Products_VariantColors?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_Products_VariantColors?$top=10>

