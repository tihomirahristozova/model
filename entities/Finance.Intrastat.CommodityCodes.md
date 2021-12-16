---
uid: Finance.Intrastat.CommodityCodes
---
# Finance.Intrastat.CommodityCodes Entity

**Namespace:** [Finance.Intrastat](Finance.Intrastat.md)  

Contains the approved Intrastat commodity codes for each period. Entity: Its_Commodity_Codes

## Default Visualization
Default Display Text Format:  
_{ExciseProductCode}_  
Default Search Members:  
_ExciseProductCode_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Finance.Intrastat.CommodityCodes](Finance.Intrastat.CommodityCodes.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [CommodityCodeField](Finance.Intrastat.CommodityCodes.md#commoditycodefield) | string (8) | Product code from the Intrastat Combined nomenclature. `Required` `Filter(eq;like)` `ORD` 
| [Description](Finance.Intrastat.CommodityCodes.md#description) | [MultilanguageString](../data-types.md#multilanguagestring) | Description of the product code from the Intrastat Combined nomenclature. `Required` `Filter(like)` 
| [ExciseAlcoholicStrength](Finance.Intrastat.CommodityCodes.md#excisealcoholicstrength) | decimal (5, 2) __nullable__ | Specifies the alcoholic strength for excise products (if applicable). `Introduced in version 21.1.3.44` 
| [ExciseProductCode](Finance.Intrastat.CommodityCodes.md#exciseproductcode) | string (20) __nullable__ | The code of the product for excise purposes (if applicable). A.k.a. APCode. `Introduced in version 21.1.3.44` 
| [Id](Finance.Intrastat.CommodityCodes.md#id) | guid |  
| [RowVersion](Finance.Intrastat.CommodityCodes.md#rowversion) | byte[] |  
| [SupplementaryUnit](Finance.Intrastat.CommodityCodes.md#supplementaryunit) | string (16) | If not null, the related product should have additional measurement unit with the same code as specified in this field. The additional unit will be used for the purposes of the Intrastat declarations. `Required` 
| [ValidFrom](Finance.Intrastat.CommodityCodes.md#validfrom) | date __nullable__ | The starting date of validity of this code. `Filter(ge;le)` 
| [ValidTo](Finance.Intrastat.CommodityCodes.md#validto) | date __nullable__ | The ending date of validity of this code. `Filter(ge;le)` 


## Attribute Details

### CommodityCodeField

Product code from the Intrastat Combined nomenclature. `Required` `Filter(eq;like)` `ORD`

_Type_: **string (8)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  
_Maximum Length_: **8**  

### Description

Description of the product code from the Intrastat Combined nomenclature. `Required` `Filter(like)`

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### ExciseAlcoholicStrength

Specifies the alcoholic strength for excise products (if applicable). `Introduced in version 21.1.3.44`

_Type_: **decimal (5, 2) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ExciseProductCode

The code of the product for excise purposes (if applicable). A.k.a. APCode. `Introduced in version 21.1.3.44`

_Type_: **string (20) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **20**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### RowVersion

_Type_: **byte[]**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### SupplementaryUnit

If not null, the related product should have additional measurement unit with the same code as specified in this field. The additional unit will be used for the purposes of the Intrastat declarations. `Required`

_Type_: **string (16)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **16**  

### ValidFrom

The starting date of validity of this code. `Filter(ge;le)`

_Type_: **date __nullable__**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### ValidTo

The ending date of validity of this code. `Filter(ge;le)`

_Type_: **date __nullable__**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  



## Business Rules

[!list limit=1000 erp.entity=Finance.Intrastat.CommodityCodes erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Finance.Intrastat.CommodityCodes erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Intrastat_CommodityCodes?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Intrastat_CommodityCodes?$top=10>

