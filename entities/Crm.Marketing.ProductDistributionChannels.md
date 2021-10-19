---
uid: Crm.Marketing.ProductDistributionChannels
---
# Crm.Marketing.ProductDistributionChannels Entity

**Namespace:** [Crm.Marketing](Crm.Marketing.md)  

Channel assignments (listing) for products. Entity: Crm_Product_Distribution_Channels

## Default Visualization
Default Display Text Format:  
_{Product.Name:T}_  
Default Search Member:  
__  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[General.Products.Products](General.Products.Products.md)  
Aggregate Root:  
[General.Products.Products](General.Products.Products.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [FromDate](Crm.Marketing.ProductDistributionChannels.md#fromdate) | date __nullable__ | When the product was listed. null-the product was not yet listed. The data is for informational purposes only and does not affect the listing status of the product (Is_Active does). `Default(Today)` `Filter(ge;le)` 
| [Id](Crm.Marketing.ProductDistributionChannels.md#id) | guid |  
| [IsActive](Crm.Marketing.ProductDistributionChannels.md#isactive) | boolean | Is this product listing active? true=Yes, false=No. `Required` `Default(true)` `Filter(eq)` 
| [MinimalSalesPricePerLot](Crm.Marketing.ProductDistributionChannels.md#minimalsalespriceperlot) | [Amount (18, 4)](../data-types.md#amount) __nullable__ | Minimal allowed price for sales of this product through this channel. The price is for one standard lot and in the costing currency of the product. The minimum is enforced upon planning and/or releasing a document. null means that there is no minimal sales price enforcement. `Currency: Product.CostingCurrency` 
| [MinimalSalesQuantityBase](Crm.Marketing.ProductDistributionChannels.md#minimalsalesquantitybase) | decimal (18, 3) __nullable__ | Minimal base quantity of the current product that has to be specified in any sale for this distribution channel. 
| [ToDate](Crm.Marketing.ProductDistributionChannels.md#todate) | date __nullable__ | When the product was de-listed. null=unknown or the product was not de-listed. The data is for informational purposes only and does not affect the listing status of the product (Is_Active does). `Filter(ge;le)` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [DistributionChannel](Crm.Marketing.ProductDistributionChannels.md#distributionchannel) | [DistributionChannels](Crm.Marketing.DistributionChannels.md) | The distribution channel in which the product is listed. `Required` `Filter(multi eq)` |
| [Product](Crm.Marketing.ProductDistributionChannels.md#product) | [Products](General.Products.Products.md) | The listed product. `Required` `Filter(multi eq)` `Owner` |


## Attribute Details

### FromDate

When the product was listed. null-the product was not yet listed. The data is for informational purposes only and does not affect the listing status of the product (Is_Active does). `Default(Today)` `Filter(ge;le)`

_Type_: **date __nullable__**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **CurrentDate**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### IsActive

Is this product listing active? true=Yes, false=No. `Required` `Default(true)` `Filter(eq)`

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### MinimalSalesPricePerLot

Minimal allowed price for sales of this product through this channel. The price is for one standard lot and in the costing currency of the product. The minimum is enforced upon planning and/or releasing a document. null means that there is no minimal sales price enforcement. `Currency: Product.CostingCurrency`

_Type_: **[Amount (18, 4)](../data-types.md#amount) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### MinimalSalesQuantityBase

Minimal base quantity of the current product that has to be specified in any sale for this distribution channel.

_Type_: **decimal (18, 3) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ToDate

When the product was de-listed. null=unknown or the product was not de-listed. The data is for informational purposes only and does not affect the listing status of the product (Is_Active does). `Filter(ge;le)`

_Type_: **date __nullable__**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  


## Reference Details

### DistributionChannel

The distribution channel in which the product is listed. `Required` `Filter(multi eq)`

_Type_: **[DistributionChannels](Crm.Marketing.DistributionChannels.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  

### Product

The listed product. `Required` `Filter(multi eq)` `Owner`

_Type_: **[Products](General.Products.Products.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  



## Business Rules

[!list limit=1000 erp.entity=Crm.Marketing.ProductDistributionChannels erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Crm.Marketing.ProductDistributionChannels erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_Marketing_ProductDistributionChannels?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Crm_Marketing_ProductDistributionChannels?$top=10>

