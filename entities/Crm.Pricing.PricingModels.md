---
uid: Crm.Pricing.PricingModels
---
# Crm.Pricing.PricingModels Entity

**Namespace:** [Crm.Pricing](Crm.Pricing.md)  

Pricing models are assigned to product groups and are used to automate creation of standard costs and prices and related price records. Entity: Crm_Pricing_Models

## Default Visualization
Default Display Text Format:  
_{Name}_  
Default Search Members:  
_Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Crm.Pricing.PricingModels](Crm.Pricing.PricingModels.md)  
  * [Crm.Pricing.PricingModelCosts](Crm.Pricing.PricingModelCosts.md)  
  * [Crm.Pricing.PricingModelPriceLists](Crm.Pricing.PricingModelPriceLists.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [DefaultMarginPercent](Crm.Pricing.PricingModels.md#defaultmarginpercent) | decimal (6, 5) | Default margin between standard cost and standard price. The margin is applied to the products when calculating standard price. `Required` `Default(0)` 
| [Id](Crm.Pricing.PricingModels.md#id) | guid |  
| [Name](Crm.Pricing.PricingModels.md#name) | string (254) | The name of the pricing model. `Required` `Filter(eq;like)` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Currency](Crm.Pricing.PricingModels.md#currency) | [Currencies](General.Currencies.md) | The currency in which the prices will be calculated. `Required` `Filter(multi eq)` |
| [PurchasePriceList](Crm.Pricing.PricingModels.md#purchasepricelist) | [PurchasePriceLists](Logistics.Procurement.PurchasePriceLists.md) | Purchase price list Id, which will be used to get the purchase price of the products. `Required` `Filter(multi eq)` |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Costs | [PricingModelCosts](Crm.Pricing.PricingModelCosts.md) | List of `PricingModelCost`(Crm.Pricing.PricingModelCosts.md) child objects, based on the `Crm.Pricing.PricingModelCost.PricingModel`(Crm.Pricing.PricingModelCosts.md#pricingmodel) back reference 
| PriceLists | [PricingModelPriceLists](Crm.Pricing.PricingModelPriceLists.md) | List of `PricingModelPriceList`(Crm.Pricing.PricingModelPriceLists.md) child objects, based on the `Crm.Pricing.PricingModelPriceList.PricingModel`(Crm.Pricing.PricingModelPriceLists.md#pricingmodel) back reference 


## Attribute Details

### DefaultMarginPercent

Default margin between standard cost and standard price. The margin is applied to the products when calculating standard price. `Required` `Default(0)`

_Type_: **decimal (6, 5)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

The name of the pricing model. `Required` `Filter(eq;like)`

_Type_: **string (254)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  


## Reference Details

### Currency

The currency in which the prices will be calculated. `Required` `Filter(multi eq)`

_Type_: **[Currencies](General.Currencies.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### PurchasePriceList

Purchase price list Id, which will be used to get the purchase price of the products. `Required` `Filter(multi eq)`

_Type_: **[PurchasePriceLists](Logistics.Procurement.PurchasePriceLists.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list limit=1000 erp.entity=Crm.Pricing.PricingModels erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Crm.Pricing.PricingModels erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_Pricing_PricingModels?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Crm_Pricing_PricingModels?$top=10>

