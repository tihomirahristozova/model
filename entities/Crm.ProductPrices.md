# Crm.ProductPrices

Specific prices of products. A price is applied after matching the specified criteria. Entity: Crm_Product_Prices

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Crm.ProductPrices.md#Id) | guid |  
| [FromDate](Crm.ProductPrices.md#FromDate) | date (nullable) | Starting date of validity of the price. [Filter(eq;ge;le)] 
| [MaxQuantity](Crm.ProductPrices.md#MaxQuantity) | [Quantity](../data-types/Quantity.md) (nullable) | Maximum quantity for which this price is valid in the Price_Quantity_Measurement_Unit. [Unit: PriceQuantityMeasurementUnit] [Filter(eq;ge;le)] 
| [MinQuantity](Crm.ProductPrices.md#MinQuantity) | [Quantity](../data-types/Quantity.md) (nullable) | Minimal quantity required to use this price (in the Price_Quantity_Measurement_Unit). [Unit: PriceQuantityMeasurementUnit] [Filter(eq;ge;le)] 
| [Notes](Crm.ProductPrices.md#Notes) | string (nullable) | Notes for this ProductPrice. 
| [Price](Crm.ProductPrices.md#Price) | [Amount](../data-types/Amount.md) | Price in the specified currency and for the specified quantity. [Currency: Currency] [Required] [Default(0)] [Filter(eq;ge;le)] 
| [PriceQuantity](Crm.ProductPrices.md#PriceQuantity) | [Quantity](../data-types/Quantity.md) | The quantity of the product for which the price is specified. [Unit: PriceQuantityMeasurementUnit] [Required] [Default(1)] [Filter(ge;le)] 
| [Priority](Crm.ProductPrices.md#Priority) | [General.Priority](Crm.ProductPrices.md#Priority) | Priority of the price comparative to other prices. Only the highest priority price is applied. [Required] [Default(2)] [Filter(multi eq)] 
| [ThruDate](Crm.ProductPrices.md#ThruDate) | date (nullable) | Ending date (inclusive) of the validity of the price. [Filter(eq;ge;le)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Currency](Crm.ProductPrices.md#Currency) | [General.Currencies](General.Currencies.md) | The currency of the price. [Required] [Filter(multi eq)] |
| [Customer](Crm.ProductPrices.md#Customer) | [Crm.Customers](Crm.Customers.md) (nullable) | When not null, specifies that the customer of the sales document must be the specified customer. [Filter(multi eq)] |
| [DistributionChannel](Crm.ProductPrices.md#DistributionChannel) | [Crm.Marketing.DistributionChannels](Crm.Marketing.DistributionChannels.md) (nullable) | Use the price only when selling through the specified channel. [Filter(multi eq)] |
| [EnterpriseCompany](Crm.ProductPrices.md#EnterpriseCompany) | [General.EnterpriseCompanies](General.EnterpriseCompanies.md) (nullable) | When not null, specifies that the sales document must be in the specified enterprise company. [Filter(multi eq)] |
| [EnterpriseCompanyLocation](Crm.ProductPrices.md#EnterpriseCompanyLocation) | [General.Contacts.CompanyLocations](General.Contacts.CompanyLocations.md) (nullable) | When set, specifies that the sales document must be of the specified enterprise company location. [Filter(multi eq)] |
| [PriceList](Crm.ProductPrices.md#PriceList) | [Crm.PriceLists](Crm.PriceLists.md) (nullable) | When not null, specifies that the sales document must have the specified price list. [Filter(multi eq)] |
| [PriceQuantityMeasurementUnit](Crm.ProductPrices.md#PriceQuantityMeasurementUnit) | [General.MeasurementUnits](General.MeasurementUnits.md) | The measurement unit of Price_Quantity. [Required] [Filter(multi eq)] |
| [PriceType](Crm.ProductPrices.md#PriceType) | [Crm.PriceTypes](Crm.PriceTypes.md) (nullable) | Price type of the current product price. The price types are used to set additional priority condition for the prices. [Filter(multi eq)] |
| [Product](Crm.ProductPrices.md#Product) | [General.Products.Products](General.Products.Products.md) | The product for which a price will be defined. [Required] [Filter(multi eq)] |
| [ShipToCustomer](Crm.ProductPrices.md#ShipToCustomer) | [Crm.Customers](Crm.Customers.md) (nullable) | When not null, specifies that the price will be applied only when the sales document has the specified Ship-To-Customer. [Filter(multi eq)] |
| [TargetGroup](Crm.ProductPrices.md#TargetGroup) | [Crm.Marketing.TargetGroups](Crm.Marketing.TargetGroups.md) (nullable) | When not null, specifies a criteria, which is matched only when the customer of the sales document is included in the group. [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### FromDate

> Starting date of validity of the price. [Filter(eq;ge;le)]

_Type_: **date (nullable)**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### MaxQuantity

> Maximum quantity for which this price is valid in the Price_Quantity_Measurement_Unit. [Unit: PriceQuantityMeasurementUnit] [Filter(eq;ge;le)]

_Type_: **[Quantity](../data-types/Quantity.md) (nullable)**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### MinQuantity

> Minimal quantity required to use this price (in the Price_Quantity_Measurement_Unit). [Unit: PriceQuantityMeasurementUnit] [Filter(eq;ge;le)]

_Type_: **[Quantity](../data-types/Quantity.md) (nullable)**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### Notes

> Notes for this ProductPrice.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Price

> Price in the specified currency and for the specified quantity. [Currency: Currency] [Required] [Default(0)] [Filter(eq;ge;le)]

_Type_: **[Amount](../data-types/Amount.md)**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### PriceQuantity

> The quantity of the product for which the price is specified. [Unit: PriceQuantityMeasurementUnit] [Required] [Default(1)] [Filter(ge;le)]

_Type_: **[Quantity](../data-types/Quantity.md)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### Priority

> Priority of the price comparative to other prices. Only the highest priority price is applied. [Required] [Default(2)] [Filter(multi eq)]

_Type_: **[General.Priority](Crm.ProductPrices.md#Priority)**  
Generic enum type for Priority properties  
_Allowed Values (Enum Members)_  

| Value | Description |
| ---- | --- |
| Lowest | Lowest value. Stored as 1. <br /> _Database Value:_ 1 <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'Lowest' |
| Low | Low value. Stored as 2. <br /> _Database Value:_ 2 <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'Low' |
| Medium | Medium value. Stored as 3. <br /> _Database Value:_ 3 <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'Medium' |
| High | High value. Stored as 4. <br /> _Database Value:_ 4 <br /> _Model Value:_ 4 <br /> _Domain API Value:_ 'High' |
| Highest | Highest value. Stored as 5. <br /> _Database Value:_ 5 <br /> _Model Value:_ 5 <br /> _Domain API Value:_ 'Highest' |

_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **2**  

### ThruDate

> Ending date (inclusive) of the validity of the price. [Filter(eq;ge;le)]

_Type_: **date (nullable)**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  


## Reference Details

### Currency

> The currency of the price. [Required] [Filter(multi eq)]

_Type_: **[General.Currencies](General.Currencies.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Customer

> When not null, specifies that the customer of the sales document must be the specified customer. [Filter(multi eq)]

_Type_: **[Crm.Customers](Crm.Customers.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### DistributionChannel

> Use the price only when selling through the specified channel. [Filter(multi eq)]

_Type_: **[Crm.Marketing.DistributionChannels](Crm.Marketing.DistributionChannels.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### EnterpriseCompany

> When not null, specifies that the sales document must be in the specified enterprise company. [Filter(multi eq)]

_Type_: **[General.EnterpriseCompanies](General.EnterpriseCompanies.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### EnterpriseCompanyLocation

> When set, specifies that the sales document must be of the specified enterprise company location. [Filter(multi eq)]

_Type_: **[General.Contacts.CompanyLocations](General.Contacts.CompanyLocations.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`IIF(((obj.EnterpriseCompanyLocation != null) AndAlso (obj.EnterpriseCompanyLocation.Company != obj.EnterpriseCompany)), null, obj.EnterpriseCompanyLocation.Company)`
### PriceList

> When not null, specifies that the sales document must have the specified price list. [Filter(multi eq)]

_Type_: **[Crm.PriceLists](Crm.PriceLists.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### PriceQuantityMeasurementUnit

> The measurement unit of Price_Quantity. [Required] [Filter(multi eq)]

_Type_: **[General.MeasurementUnits](General.MeasurementUnits.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`IIF((obj.Product != null), obj.Product.MeasurementUnit, obj.PriceQuantityMeasurementUnit)`
### PriceType

> Price type of the current product price. The price types are used to set additional priority condition for the prices. [Filter(multi eq)]

_Type_: **[Crm.PriceTypes](Crm.PriceTypes.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Product

> The product for which a price will be defined. [Required] [Filter(multi eq)]

_Type_: **[General.Products.Products](General.Products.Products.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### ShipToCustomer

> When not null, specifies that the price will be applied only when the sales document has the specified Ship-To-Customer. [Filter(multi eq)]

_Type_: **[Crm.Customers](Crm.Customers.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`IIF((obj.ShipToCustomer.Party.ParentParty != obj.Customer), null, obj.ShipToCustomer)`
### TargetGroup

> When not null, specifies a criteria, which is matched only when the customer of the sales document is included in the group. [Filter(multi eq)]

_Type_: **[Crm.Marketing.TargetGroups](Crm.Marketing.TargetGroups.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Crm.ProductPrices erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Crm.ProductPrices erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Crm.ProductPrices erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_ProductPrices?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Crm_ProductPrices?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_Product_Prices?$top=10>

