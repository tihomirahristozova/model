---
uid: General.Products.ProductCodes
---
# General.Products.ProductCodes Entity

**Namespace:** [General.Products](General.Products.md)  

Additional product codes, categorized by coding systems. Entity: Gen_Product_Codes

## Default Visualization
Default Display Text Format:  
_{Product.Name:T}_  
Default Search Members:  
_Product.Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[General.Products.Products](General.Products.Products.md)  
Aggregate Root:  
[General.Products.Products](General.Products.Products.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Active](General.Products.ProductCodes.md#active) | boolean | True when the code is active and can be selected in new documents. `Required` `Default(true)` `Filter(eq)` 
| [Id](General.Products.ProductCodes.md#id) | guid |  
| [ProductCodeField](General.Products.ProductCodes.md#productcodefield) | string (32) | The code of the product in the specified coding system. `Required` `Filter(eq;like)` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [CodingSystem](General.Products.ProductCodes.md#codingsystem) | [CodingSystems](General.Products.CodingSystems.md) | The coding system in which the product code is specified. `Required` `Filter(multi eq)` |
| [Product](General.Products.ProductCodes.md#product) | [Products](General.Products.Products.md) | The product for which the code is specified. `Required` `Filter(multi eq)` `Owner` |


## Attribute Details

### Active

True when the code is active and can be selected in new documents. `Required` `Default(true)` `Filter(eq)`

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### ProductCodeField

The code of the product in the specified coding system. `Required` `Filter(eq;like)`

_Type_: **string (32)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  
_Maximum Length_: **32**  


## Reference Details

### CodingSystem

The coding system in which the product code is specified. `Required` `Filter(multi eq)`

_Type_: **[CodingSystems](General.Products.CodingSystems.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  

### Product

The product for which the code is specified. `Required` `Filter(multi eq)` `Owner`

_Type_: **[Products](General.Products.Products.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  



## Business Rules

[!list limit=1000 erp.entity=General.Products.ProductCodes erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=General.Products.ProductCodes erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_Products_ProductCodes?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_Products_ProductCodes?$top=10>

