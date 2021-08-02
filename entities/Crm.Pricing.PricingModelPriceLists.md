---
uid: Crm.Pricing.PricingModelPriceLists
---
# Crm.Pricing.PricingModelPriceLists Entity

**Namespace:** [Crm.Pricing](Crm.Pricing.md)  

The price lists, which are updated by the pricing model. Entity: Crm_Pricing_Model_Price_Lists

## Default Visualization
Default Display Text Format:  
_{PricingModel.Name:T}_  
Default Search Member:  
_PricingModel.Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[Crm.Pricing.PricingModels](Crm.Pricing.PricingModels.md)  
Aggregate Root:  
[Crm.Pricing.PricingModels](Crm.Pricing.PricingModels.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Crm.Pricing.PricingModelPriceLists.md#id) | guid |  
| [LineNo](Crm.Pricing.PricingModelPriceLists.md#lineno) | int32 | The consecutive number of this price list within the pricing model. `Required` 
| [MarginPercent](Crm.Pricing.PricingModelPriceLists.md#marginpercent) | decimal (6, 5) __nullable__ | Used, when the price will be automatically calculated as percentage difference from standard price. It is usually a negative value. null, when the price will not be automatically calculated in this way. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [PriceList](Crm.Pricing.PricingModelPriceLists.md#pricelist) | [PriceLists](Crm.PriceLists.md) | The price list, which is included in the pricing model. `Required` `Filter(multi eq)` |
| [PricingModel](Crm.Pricing.PricingModelPriceLists.md#pricingmodel) | [PricingModels](Crm.Pricing.PricingModels.md) | The pricing model, for which the price list is listed. `Required` `Filter(multi eq)` `Owner` |


## Attribute Details

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### LineNo

The consecutive number of this price list within the pricing model. `Required`

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`( obj.PricingModel.PriceLists.Select( c => c.LineNo).DefaultIfEmpty( 0).Max( ) + 10)`

_Front-End Recalc Expressions:_  
`( obj.PricingModel.PriceLists.Select( c => c.LineNo).DefaultIfEmpty( 0).Max( ) + 10)`
### MarginPercent

Used, when the price will be automatically calculated as percentage difference from standard price. It is usually a negative value. null, when the price will not be automatically calculated in this way.

_Type_: **decimal (6, 5) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### PriceList

The price list, which is included in the pricing model. `Required` `Filter(multi eq)`

_Type_: **[PriceLists](Crm.PriceLists.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### PricingModel

The pricing model, for which the price list is listed. `Required` `Filter(multi eq)` `Owner`

_Type_: **[PricingModels](Crm.Pricing.PricingModels.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  



## Business Rules

[!list limit=1000 erp.entity=Crm.Pricing.PricingModelPriceLists erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Crm.Pricing.PricingModelPriceLists erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_Pricing_PricingModelPriceLists?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Crm_Pricing_PricingModelPriceLists?$top=10>

