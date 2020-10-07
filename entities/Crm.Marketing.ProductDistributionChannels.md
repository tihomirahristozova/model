# Crm.Marketing.ProductDistributionChannels

Channel assignments (listing) for products. Entity: Crm_Product_Distribution_Channels

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Crm.Marketing.ProductDistributionChannels.md#Id) | guid |  
| [FromDate](Crm.Marketing.ProductDistributionChannels.md#FromDate) | date (nullable) | When the product was listed. null-the product was not yet listed. The data is for informational purposes only and does not affect the listing status of the product (Is_Active does). [Default(Today)] [Filter(ge;le)] 
| [IsActive](Crm.Marketing.ProductDistributionChannels.md#IsActive) | boolean | Is this product listing active? true=Yes, false=No. [Required] [Default(true)] [Filter(eq)] 
| [MinimalSalesPricePerLot](Crm.Marketing.ProductDistributionChannels.md#MinimalSalesPricePerLot) | [Amount](../data-types/Amount.md) (nullable) | Minimal allowed price for sales of this product through this channel. The price is for one standard lot and in the costing currency of the product. The minimum is enforced upon planning and/or releasing a document. null means that there is no minimal sales price enforcement. [Currency: Product.CostingCurrency] 
| [MinimalSalesQuantityBase](Crm.Marketing.ProductDistributionChannels.md#MinimalSalesQuantityBase) | decimal (nullable) | Minimal base quantity of the current product that has to be specified in any sale for this distribution channel. 
| [ToDate](Crm.Marketing.ProductDistributionChannels.md#ToDate) | date (nullable) | When the product was de-listed. null=unknown or the product was not de-listed. The data is for informational purposes only and does not affect the listing status of the product (Is_Active does). [Filter(ge;le)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [DistributionChannel](Crm.Marketing.ProductDistributionChannels.md#DistributionChannel) | [Crm.Marketing.DistributionChannels](Crm.Marketing.DistributionChannels.md) | The distribution channel in which the product is listed. [Required] [Filter(multi eq)] |
| [Product](Crm.Marketing.ProductDistributionChannels.md#Product) | [General.Products.Products](General.Products.Products.md) | The listed product. [Required] [Filter(multi eq)] [Owner] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### FromDate

> When the product was listed. null-the product was not yet listed. The data is for informational purposes only and does not affect the listing status of the product (Is_Active does). [Default(Today)] [Filter(ge;le)]

_Type_: **date (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **CurrentDate**  

### IsActive

> Is this product listing active? true=Yes, false=No. [Required] [Default(true)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### MinimalSalesPricePerLot

> Minimal allowed price for sales of this product through this channel. The price is for one standard lot and in the costing currency of the product. The minimum is enforced upon planning and/or releasing a document. null means that there is no minimal sales price enforcement. [Currency: Product.CostingCurrency]

_Type_: **[Amount](../data-types/Amount.md) (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### MinimalSalesQuantityBase

> Minimal base quantity of the current product that has to be specified in any sale for this distribution channel.

_Type_: **decimal (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ToDate

> When the product was de-listed. null=unknown or the product was not de-listed. The data is for informational purposes only and does not affect the listing status of the product (Is_Active does). [Filter(ge;le)]

_Type_: **date (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  


## Reference Details

### DistributionChannel

> The distribution channel in which the product is listed. [Required] [Filter(multi eq)]

_Type_: **[Crm.Marketing.DistributionChannels](Crm.Marketing.DistributionChannels.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Product

> The listed product. [Required] [Filter(multi eq)] [Owner]

_Type_: **[General.Products.Products](General.Products.Products.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Crm.Marketing.ProductDistributionChannels erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Crm.Marketing.ProductDistributionChannels erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Crm.Marketing.ProductDistributionChannels erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_Marketing_ProductDistributionChannels?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Crm_Marketing_ProductDistributionChannels?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_Product_Distribution_Channels?$top=10>

