# Crm.Pricing.PricingModelPriceLists

The price lists, which are updated by the pricing model. Entity: Crm_Pricing_Model_Price_Lists

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Crm.Pricing.PricingModelPriceLists.md#Id) | guid |  
| [LineNo](Crm.Pricing.PricingModelPriceLists.md#LineNo) | int32 | The consecutive number of this price list within the pricing model. [Required] 
| [MarginPercent](Crm.Pricing.PricingModelPriceLists.md#MarginPercent) | decimal (nullable) | Used, when the price will be automatically calculated as percentage difference from standard price. It is usually a negative value. null, when the price will not be automatically calculated in this way. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [PriceList](Crm.Pricing.PricingModelPriceLists.md#PriceList) | [Crm.PriceLists](Crm.PriceLists.md) | The price list, which is included in the pricing model. [Required] [Filter(multi eq)] |
| [PricingModel](Crm.Pricing.PricingModelPriceLists.md#PricingModel) | [Crm.Pricing.PricingModels](Crm.Pricing.PricingModels.md) | The pricing model, for which the price list is listed. [Required] [Filter(multi eq)] [Owner] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### LineNo

> The consecutive number of this price list within the pricing model. [Required]

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`(obj.PricingModel.PriceLists.Select(c => c.LineNo).DefaultIfEmpty(0).Max() + 10)`

_Front-End Recalc Expressions:_  
`(obj.PricingModel.PriceLists.Select(c => c.LineNo).DefaultIfEmpty(0).Max() + 10)`
### MarginPercent

> Used, when the price will be automatically calculated as percentage difference from standard price. It is usually a negative value. null, when the price will not be automatically calculated in this way.

_Type_: **decimal (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### PriceList

> The price list, which is included in the pricing model. [Required] [Filter(multi eq)]

_Type_: **[Crm.PriceLists](Crm.PriceLists.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### PricingModel

> The pricing model, for which the price list is listed. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Crm.Pricing.PricingModels](Crm.Pricing.PricingModels.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Crm.Pricing.PricingModelPriceLists erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Crm.Pricing.PricingModelPriceLists erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Crm.Pricing.PricingModelPriceLists erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_Pricing_PricingModelPriceLists?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Crm_Pricing_PricingModelPriceLists?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_Pricing_Model_Price_Lists?$top=10>

