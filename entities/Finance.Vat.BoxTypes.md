---
uid: Finance.Vat.BoxTypes
---
# Finance.Vat.BoxTypes Entity

**Namespace:** [Finance.Vat](Finance.Vat.md)  

The types of boxes in a VAT declaration. . Entity: VAT_Box_Types (Introduced in version 22.1.4.18)

## Default Visualization
Default Display Text Format:  
_{Name:T}_  
Default Search Members:  
_Code; Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Finance.Vat.BoxTypes](Finance.Vat.BoxTypes.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Code](Finance.Vat.BoxTypes.md#code) | string (32) | The unique code of the BoxType. `Required` `Filter(multi eq)` 
| [Id](Finance.Vat.BoxTypes.md#id) | guid |  
| [Name](Finance.Vat.BoxTypes.md#name) | [MultilanguageString](../data-types.md#multilanguagestring) | The name for this box type. (Miltilanguage string). `Required` `Filter(like)` 
| [Notes](Finance.Vat.BoxTypes.md#notes) | string (max) __nullable__ | Notes for this BoxType. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Country](Finance.Vat.BoxTypes.md#country) | [Countries](General.Geography.Countries.md) | The Country for which this type of box is declared. `Required` `Filter(multi eq)` |


## Attribute Details

### Code

The unique code of the BoxType. `Required` `Filter(multi eq)`

_Type_: **string (32)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Maximum Length_: **32**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

The name for this box type. (Miltilanguage string). `Required` `Filter(like)`

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### Notes

Notes for this BoxType.

_Type_: **string (max) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  


## Reference Details

### Country

The Country for which this type of box is declared. `Required` `Filter(multi eq)`

_Type_: **[Countries](General.Geography.Countries.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list limit=1000 erp.entity=Finance.Vat.BoxTypes erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Finance.Vat.BoxTypes erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Vat_BoxTypes?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Vat_BoxTypes?$top=10>

