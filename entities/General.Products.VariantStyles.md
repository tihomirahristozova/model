---
uid: General.Products.VariantStyles
---
# General.Products.VariantStyles Entity

Contains the different styles, which can be assigned to product variants. Entity: Gen_Variant_Styles

Default Display Text Format:  
_{Code}: {Name:T}_  
Default Search Member:  
_Code_  

## [Aggregate Tree](xref:aggregates)  
* [General.Products.VariantStyles](General.Products.VariantStyles.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Code](General.Products.VariantStyles.md#code) | string | Unique code of the style. Used to generate parts of bar-codes and in other coding schemes. [Required] [Filter(eq;like)] [ORD] 
| [Id](General.Products.VariantStyles.md#id) | guid |  
| [Name](General.Products.VariantStyles.md#name) | [MultilanguageString](../data-types.md#multilanguagestring) | The name of this VariantStyle. [Required] [Filter(eq;like)] [ORD] 


## Attribute Details

### Code

Unique code of the style. Used to generate parts of bar-codes and in other coding schemes. [Required] [Filter(eq;like)] [ORD]

_Type_: **string**  
_Indexed_: **True**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

The name of this VariantStyle. [Required] [Filter(eq;like)] [ORD]

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  



## Business Rules

[!list erp.entity=General.Products.VariantStyles erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.Products.VariantStyles erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_Products_VariantStyles?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_Products_VariantStyles?$top=10>

