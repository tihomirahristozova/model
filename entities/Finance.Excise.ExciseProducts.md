---
uid: Finance.Excise.ExciseProducts
---
# Finance.Excise.ExciseProducts Entity

**Namespace:** [Finance.Excise](Finance.Excise.md)  

Excise product codes are defined by the taxation and customs authorities. For EU, these are 4-letter codes, similar to T200, S200, B000, etc. . Entity: Exc_Excise_Products (Introduced in version 21.1.3.87)

## Default Visualization
Default Display Text Format:  
_{Name:T} : {Code}_  
Default Search Member:  
__  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Finance.Excise.ExciseProducts](Finance.Excise.ExciseProducts.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Code](Finance.Excise.ExciseProducts.md#code) | string (32) | The unique code of the ExciseProduct. `Required` `Filter(multi eq;like)` `ORD` 
| [Id](Finance.Excise.ExciseProducts.md#id) | guid |  
| [Name](Finance.Excise.ExciseProducts.md#name) | [MultilanguageString](../data-types.md#multilanguagestring) | Multilanguage string. `Required` `Filter(like)` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [ExciseProductCategory](Finance.Excise.ExciseProducts.md#exciseproductcategory) | [ExciseProductCategories](Finance.Excise.ExciseProductCategories.md) | The category of the excise product. `Required` `Filter(multi eq)` |


## Attribute Details

### Code

The unique code of the ExciseProduct. `Required` `Filter(multi eq;like)` `ORD`

_Type_: **string (32)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, Like, EqualsIn**  
_Supports Order By_: **True**  
_Maximum Length_: **32**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

Multilanguage string. `Required` `Filter(like)`

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  


## Reference Details

### ExciseProductCategory

The category of the excise product. `Required` `Filter(multi eq)`

_Type_: **[ExciseProductCategories](Finance.Excise.ExciseProductCategories.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list limit=1000 erp.entity=Finance.Excise.ExciseProducts erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Finance.Excise.ExciseProducts erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Excise_ExciseProducts?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Excise_ExciseProducts?$top=10>

