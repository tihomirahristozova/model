---
uid: Finance.Excise.ExciseProductCategories
---
# Finance.Excise.ExciseProductCategories Entity

**Namespace:** [Finance.Excise](Finance.Excise.md)  

Product Category is defined by the taxation and customs authorities. Also specifies the calculation algorithm for the excise. For EU, the product category code is a single character - B,E,I,S,T or W. Entity: Exc_Excise_Product_Categories (Introduced in version 21.1.3.87)

## Default Visualization
Default Display Text Format:  
_{Name:T} : {Code}_  
Default Search Member:  
_Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Finance.Excise.ExciseProductCategories](Finance.Excise.ExciseProductCategories.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [CalculationAlgorithm](Finance.Excise.ExciseProductCategories.md#calculationalgorithm) | [CalculationAlgorithm](Finance.Excise.ExciseProductCategories.md#calculationalgorithm) | The calculation algorithm for Tax Base. NOP=No operation - manually set Tax Base; QTY=Qty; QAS=Qty * Alcoholic strength; QAP=Qty * Alcoholic strength / 100. `Required` 
| [Code](Finance.Excise.ExciseProductCategories.md#code) | string (32) | For EU, the product category code is a single character - B,E,I,S,T or W. `Required` `Filter(multi eq;like)` 
| [Id](Finance.Excise.ExciseProductCategories.md#id) | guid |  
| [Name](Finance.Excise.ExciseProductCategories.md#name) | [MultilanguageString](../data-types.md#multilanguagestring) | Multilanguage String. `Required` `Filter(like)` 


## Attribute Details

### CalculationAlgorithm

The calculation algorithm for Tax Base. NOP=No operation - manually set Tax Base; QTY=Qty; QAS=Qty * Alcoholic strength; QAP=Qty * Alcoholic strength / 100. `Required`

_Type_: **[CalculationAlgorithm](Finance.Excise.ExciseProductCategories.md#calculationalgorithm)**  
Allowed values for the `CalculationAlgorithm`(Finance.Excise.ExciseProductCategories.md#calculationalgorithm) data attribute  
_Allowed Values (Finance.Excise.ExciseProductCategoriesRepository.CalculationAlgorithm Enum Members)_  

| Value | Description |
| ---- | --- |
| NoОperation | No operation - manually set Tax Base. Stored as 'NOP'. <br /> _Database Value:_ 'NOP' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'NoОperation' |
| Qty | Quantity. Stored as 'QTY'. <br /> _Database Value:_ 'QTY' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'Qty' |
| QtyByAlcoholicStrength | Quantity * Alcoholic strength. Stored as 'QAS'. <br /> _Database Value:_ 'QAS' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'QtyByAlcoholicStrength' |
| QtyByAlcoholic<br />StrengthDiv100 | Quantity * Alcoholic strength / 100. Stored as 'QAP'. <br /> _Database Value:_ 'QAP' <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'QtyByAlcoholic<br />StrengthDiv100' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Code

For EU, the product category code is a single character - B,E,I,S,T or W. `Required` `Filter(multi eq;like)`

_Type_: **string (32)**  
_Supported Filters_: **Equals, Like, EqualsIn**  
_Supports Order By_: **False**  
_Maximum Length_: **32**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  
_Default Value_: **NewGuid**  

### Name

Multilanguage String. `Required` `Filter(like)`

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  



## Business Rules

[!list limit=1000 erp.entity=Finance.Excise.ExciseProductCategories erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Finance.Excise.ExciseProductCategories erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Excise_ExciseProductCategories?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Excise_ExciseProductCategories?$top=10>

