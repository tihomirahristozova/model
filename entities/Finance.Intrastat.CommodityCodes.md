---
uid: Finance.Intrastat.CommodityCodes
---
# Finance.Intrastat.CommodityCodes Entity

Contains the approved Intrastat commodity codes for each period. Entity: Its_Commodity_Codes

Default Display Text Format:  
_{Id}_  
Default Search Member:  
_Id_  

Aggregate Tree:  
* [Finance.Intrastat.CommodityCodes](Finance.Intrastat.CommodityCodes.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [CommodityCodeField](Finance.Intrastat.CommodityCodes.md#commoditycodefield) | string | Product code from the Intrastat Combined nomenclature. [Required] [Filter(eq;like)] [ORD] 
| [Description](Finance.Intrastat.CommodityCodes.md#description) | [MultilanguageString](../data-types.md#multilanguagestring) | Description of the product code from the Intrastat Combined nomenclature. [Required] [Filter(like)] 
| [Id](Finance.Intrastat.CommodityCodes.md#id) | guid |  
| [SupplementaryUnit](Finance.Intrastat.CommodityCodes.md#supplementaryunit) | string | If not null, the related product should have additional measurement unit with the same code as specified in this field. The additional unit will be used for the purposes of the Intrastat declarations. [Required] 
| [ValidFrom](Finance.Intrastat.CommodityCodes.md#validfrom) | date (nullable) | The starting date of validity of this code. [Filter(ge;le)] 
| [ValidTo](Finance.Intrastat.CommodityCodes.md#validto) | date (nullable) | The ending date of validity of this code. [Filter(ge;le)] 


## Attribute Details

### CommodityCodeField

Product code from the Intrastat Combined nomenclature. [Required] [Filter(eq;like)] [ORD]

_Type_: **string**  
_Indexed_: **True**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  

### Description

Description of the product code from the Intrastat Combined nomenclature. [Required] [Filter(like)]

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### SupplementaryUnit

If not null, the related product should have additional measurement unit with the same code as specified in this field. The additional unit will be used for the purposes of the Intrastat declarations. [Required]

_Type_: **string**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ValidFrom

The starting date of validity of this code. [Filter(ge;le)]

_Type_: **date (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### ValidTo

The ending date of validity of this code. [Filter(ge;le)]

_Type_: **date (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Finance.Intrastat.CommodityCodes erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Finance.Intrastat.CommodityCodes erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Intrastat_CommodityCodes?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Intrastat_CommodityCodes?$top=10>

