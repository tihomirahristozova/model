---
uid: Crm.Pricing.PricingModels
---
# Crm.Pricing.PricingModels

Pricing models are assigned to product groups and are used to automate creation of standard costs and prices and related price records. Entity: Crm_Pricing_Models

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Crm.Pricing.PricingModels.md#Id) | guid |  
| [DefaultMarginPercent](Crm.Pricing.PricingModels.md#DefaultMarginPercent) | decimal | Default margin between standard cost and standard price. The margin is applied to the products when calculating standard price. [Required] [Default(0)] 
| [Name](Crm.Pricing.PricingModels.md#Name) | string | The name of the pricing model. [Required] [Filter(eq;like)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Currency](Crm.Pricing.PricingModels.md#Currency) | [General.Currencies](General.Currencies.md) | The currency in which the prices will be calculated. [Required] [Filter(multi eq)] |
| [PurchasePriceList](Crm.Pricing.PricingModels.md#PurchasePriceList) | [Logistics.Procurement.PurchasePriceLists](Logistics.Procurement.PurchasePriceLists.md) | Purchase price list Id, which will be used to get the purchase price of the products. [Required] [Filter(multi eq)] |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Costs | [Crm.Pricing.PricingModelCosts](Crm.Pricing.PricingModelCosts.md) | List of [PricingModelCost](Crm.Pricing.PricingModelCosts.md) child objects, based on the [Crm.Pricing.PricingModelCost.PricingModel](Crm.Pricing.PricingModelCosts.md#PricingModel) back reference 
| PriceLists | [Crm.Pricing.PricingModelPriceLists](Crm.Pricing.PricingModelPriceLists.md) | List of [PricingModelPriceList](Crm.Pricing.PricingModelPriceLists.md) child objects, based on the [Crm.Pricing.PricingModelPriceList.PricingModel](Crm.Pricing.PricingModelPriceLists.md#PricingModel) back reference 


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### DefaultMarginPercent

> Default margin between standard cost and standard price. The margin is applied to the products when calculating standard price. [Required] [Default(0)]

_Type_: **decimal**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### Name

> The name of the pricing model. [Required] [Filter(eq;like)]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  


## Reference Details

### Currency

> The currency in which the prices will be calculated. [Required] [Filter(multi eq)]

_Type_: **[General.Currencies](General.Currencies.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### PurchasePriceList

> Purchase price list Id, which will be used to get the purchase price of the products. [Required] [Filter(multi eq)]

_Type_: **[Logistics.Procurement.PurchasePriceLists](Logistics.Procurement.PurchasePriceLists.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Crm.Pricing.PricingModels erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Crm.Pricing.PricingModels erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Crm.Pricing.PricingModels erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_Pricing_PricingModels?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Crm_Pricing_PricingModels?$top=10>

