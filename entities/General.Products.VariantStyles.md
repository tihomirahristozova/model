# General.Products.VariantStyles

Contains the different styles, which can be assigned to product variants. Entity: Gen_Variant_Styles

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](General.Products.VariantStyles.md#Id) | guid |  
| [Code](General.Products.VariantStyles.md#Code) | string | Unique code of the style. Used to generate parts of bar-codes and in other coding schemes. [Required] [Filter(eq;like)] [ORD] 
| [Name](General.Products.VariantStyles.md#Name) | [MultilanguageString](../data-types/MultilanguageString.md) | The name of this VariantStyle. [Required] [Filter(eq;like)] [ORD] 


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### Code

> Unique code of the style. Used to generate parts of bar-codes and in other coding schemes. [Required] [Filter(eq;like)] [ORD]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  

### Name

> The name of this VariantStyle. [Required] [Filter(eq;like)] [ORD]

_Type_: **[MultilanguageString](../data-types/MultilanguageString.md)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  



## Business Rules

[!list erp.entity=General.Products.VariantStyles erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.Products.VariantStyles erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=General.Products.VariantStyles erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_Products_VariantStyles?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_Products_VariantStyles?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Gen_Variant_Styles?$top=10>

