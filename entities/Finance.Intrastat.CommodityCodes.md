---
uid: Finance.Intrastat.CommodityCodes
---
# Finance.Intrastat.CommodityCodes

Contains the approved Intrastat commodity codes for each period. Entity: Its_Commodity_Codes

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Finance.Intrastat.CommodityCodes.md#Id) | guid |  
| [CommodityCodeField](Finance.Intrastat.CommodityCodes.md#CommodityCodeField) | string | Product code from the Intrastat Combined nomenclature. [Required] [Filter(eq;like)] [ORD] 
| [Description](Finance.Intrastat.CommodityCodes.md#Description) | [MultilanguageString](../data-types.md#MultilanguageString) | Description of the product code from the Intrastat Combined nomenclature. [Required] [Filter(like)] 
| [SupplementaryUnit](Finance.Intrastat.CommodityCodes.md#SupplementaryUnit) | string | If not null, the related product should have additional measurement unit with the same code as specified in this field. The additional unit will be used for the purposes of the Intrastat declarations. [Required] 
| [ValidFrom](Finance.Intrastat.CommodityCodes.md#ValidFrom) | date (nullable) | The starting date of validity of this code. [Filter(ge;le)] 
| [ValidTo](Finance.Intrastat.CommodityCodes.md#ValidTo) | date (nullable) | The ending date of validity of this code. [Filter(ge;le)] 


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### CommodityCodeField

> Product code from the Intrastat Combined nomenclature. [Required] [Filter(eq;like)] [ORD]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  

### Description

> Description of the product code from the Intrastat Combined nomenclature. [Required] [Filter(like)]

_Type_: **[MultilanguageString](../data-types.md#MultilanguageString)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### SupplementaryUnit

> If not null, the related product should have additional measurement unit with the same code as specified in this field. The additional unit will be used for the purposes of the Intrastat declarations. [Required]

_Type_: **string**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ValidFrom

> The starting date of validity of this code. [Filter(ge;le)]

_Type_: **date (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### ValidTo

> The ending date of validity of this code. [Filter(ge;le)]

_Type_: **date (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Finance.Intrastat.CommodityCodes erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Finance.Intrastat.CommodityCodes erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Finance.Intrastat.CommodityCodes erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Intrastat_CommodityCodes?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Intrastat_CommodityCodes?$top=10>

