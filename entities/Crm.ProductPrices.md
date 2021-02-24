---
uid: Crm.ProductPrices
---
# Crm.ProductPrices Entity

Specific prices of products. A price is applied after matching the specified criteria. Entity: Crm_Product_Prices

Default Display Text Format:  
_{Id}_  
Default Search Member:  
_Id_  

## [Aggregate Tree](xref:aggregates)  
* [Crm.ProductPrices](Crm.ProductPrices.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [FromDate](Crm.ProductPrices.md#fromdate) | date (nullable) | Starting date of validity of the price. [Filter(eq;ge;le)] 
| [Id](Crm.ProductPrices.md#id) | guid |  
| [MaxQuantity](Crm.ProductPrices.md#maxquantity) | [Quantity](../data-types.md#quantity) (nullable) | Maximum quantity for which this price is valid in the Price_Quantity_<br />Measurement_Unit. [Unit: PriceQuantityMeasurement<br />Unit] [Filter(eq;ge;le)] 
| [MinQuantity](Crm.ProductPrices.md#minquantity) | [Quantity](../data-types.md#quantity) (nullable) | Minimal quantity required to use this price (in the Price_Quantity_Measurement_Unit). [Unit: PriceQuantityMeasurement<br />Unit] [Filter(eq;ge;le)] 
| [Notes](Crm.ProductPrices.md#notes) | string (nullable) | Notes for this ProductPrice. 
| [Price](Crm.ProductPrices.md#price) | [Amount](../data-types.md#amount) | Price in the specified currency and for the specified quantity. [Currency: Currency] [Required] [Default(0)] [Filter(eq;ge;le)] 
| [PriceQuantity](Crm.ProductPrices.md#pricequantity) | [Quantity](../data-types.md#quantity) | The quantity of the product for which the price is specified. [Unit: PriceQuantityMeasurement<br />Unit] [Required] [Default(1)] [Filter(ge;le)] 
| [Priority](Crm.ProductPrices.md#priority) | [Priority](Crm.ProductPrices.md#priority) | Priority of the price comparative to other prices. Only the highest priority price is applied. [Required] [Default(2)] [Filter(multi eq)] 
| [ThruDate](Crm.ProductPrices.md#thrudate) | date (nullable) | Ending date (inclusive) of the validity of the price. [Filter(eq;ge;le)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Currency](Crm.ProductPrices.md#currency) | [Currencies](General.Currencies.md) | The currency of the price. [Required] [Filter(multi eq)] |
| [Customer](Crm.ProductPrices.md#customer) | [Customers](Crm.Customers.md) (nullable) | When not null, specifies that the customer of the sales document must be the specified customer. [Filter(multi eq)] |
| [DistributionChannel](Crm.ProductPrices.md#distributionchannel) | [DistributionChannels](Crm.Marketing.DistributionChannels.md) (nullable) | Use the price only when selling through the specified channel. [Filter(multi eq)] |
| [EnterpriseCompany](Crm.ProductPrices.md#enterprisecompany) | [EnterpriseCompanies](General.EnterpriseCompanies.md) (nullable) | When not null, specifies that the sales document must be in the specified enterprise company. [Filter(multi eq)] |
| [EnterpriseCompanyLocation](Crm.ProductPrices.md#enterprisecompanylocation) | [CompanyLocations](General.Contacts.CompanyLocations.md) (nullable) | When set, specifies that the sales document must be of the specified enterprise company location. [Filter(multi eq)] |
| [PriceList](Crm.ProductPrices.md#pricelist) | [PriceLists](Crm.PriceLists.md) (nullable) | When not null, specifies that the sales document must have the specified price list. [Filter(multi eq)] |
| [PriceQuantityMeasurement<br />Unit](Crm.ProductPrices.md#pricequantitymeasurementunit) | [MeasurementUnits](General.MeasurementUnits.md) | The measurement unit of Price_Quantity. [Required] [Filter(multi eq)] |
| [PriceType](Crm.ProductPrices.md#pricetype) | [PriceTypes](Crm.PriceTypes.md) (nullable) | Price type of the current product price. The price types are used to set additional priority condition for the prices. [Filter(multi eq)] |
| [Product](Crm.ProductPrices.md#product) | [Products](General.Products.Products.md) | The product for which a price will be defined. [Required] [Filter(multi eq)] |
| [ShipToCustomer](Crm.ProductPrices.md#shiptocustomer) | [Customers](Crm.Customers.md) (nullable) | When not null, specifies that the price will be applied only when the sales document has the specified Ship-To-Customer. [Filter(multi eq)] |
| [TargetGroup](Crm.ProductPrices.md#targetgroup) | [TargetGroups](Crm.Marketing.TargetGroups.md) (nullable) | When not null, specifies a criteria, which is matched only when the customer of the sales document is included in the group. [Filter(multi eq)] |


## Attribute Details

### FromDate

Starting date of validity of the price. [Filter(eq;ge;le)]

_Type_: **date (nullable)**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### MaxQuantity

Maximum quantity for which this price is valid in the Price_Quantity_Measurement_Unit. [Unit: PriceQuantityMeasurementUnit] [Filter(eq;ge;le)]

_Type_: **[Quantity](../data-types.md#quantity) (nullable)**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### MinQuantity

Minimal quantity required to use this price (in the Price_Quantity_Measurement_Unit). [Unit: PriceQuantityMeasurementUnit] [Filter(eq;ge;le)]

_Type_: **[Quantity](../data-types.md#quantity) (nullable)**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### Notes

Notes for this ProductPrice.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Price

Price in the specified currency and for the specified quantity. [Currency: Currency] [Required] [Default(0)] [Filter(eq;ge;le)]

_Type_: **[Amount](../data-types.md#amount)**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### PriceQuantity

The quantity of the product for which the price is specified. [Unit: PriceQuantityMeasurementUnit] [Required] [Default(1)] [Filter(ge;le)]

_Type_: **[Quantity](../data-types.md#quantity)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### Priority

Priority of the price comparative to other prices. Only the highest priority price is applied. [Required] [Default(2)] [Filter(multi eq)]

_Type_: **[Priority](Crm.ProductPrices.md#priority)**  
Generic enum type for Priority properties  
_Allowed Values (General.Priority Enum Members)_  

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

Ending date (inclusive) of the validity of the price. [Filter(eq;ge;le)]

_Type_: **date (nullable)**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  


## Reference Details

### Currency

The currency of the price. [Required] [Filter(multi eq)]

_Type_: **[Currencies](General.Currencies.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### Customer

When not null, specifies that the customer of the sales document must be the specified customer. [Filter(multi eq)]

_Type_: **[Customers](Crm.Customers.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### DistributionChannel

Use the price only when selling through the specified channel. [Filter(multi eq)]

_Type_: **[DistributionChannels](Crm.Marketing.DistributionChannels.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### EnterpriseCompany

When not null, specifies that the sales document must be in the specified enterprise company. [Filter(multi eq)]

_Type_: **[EnterpriseCompanies](General.EnterpriseCompanies.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### EnterpriseCompanyLocation

When set, specifies that the sales document must be of the specified enterprise company location. [Filter(multi eq)]

_Type_: **[CompanyLocations](General.Contacts.CompanyLocations.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

_Front-End Recalc Expressions:_  
`IIF( ( ( obj.EnterpriseCompanyLocation != null) AndAlso ( obj.EnterpriseCompanyLocation.Company != obj.EnterpriseCompany)), null, obj.EnterpriseCompanyLocation.Company)`
### PriceList

When not null, specifies that the sales document must have the specified price list. [Filter(multi eq)]

_Type_: **[PriceLists](Crm.PriceLists.md) (nullable)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  

### PriceQuantityMeasurementUnit

The measurement unit of Price_Quantity. [Required] [Filter(multi eq)]

_Type_: **[MeasurementUnits](General.MeasurementUnits.md)**  
_Supported Filters_: **Equals, EqualsIn**  

_Front-End Recalc Expressions:_  
`IIF( ( obj.Product != null), obj.Product.MeasurementUnit, obj.PriceQuantityMeasurementUnit)`
### PriceType

Price type of the current product price. The price types are used to set additional priority condition for the prices. [Filter(multi eq)]

_Type_: **[PriceTypes](Crm.PriceTypes.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### Product

The product for which a price will be defined. [Required] [Filter(multi eq)]

_Type_: **[Products](General.Products.Products.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  

### ShipToCustomer

When not null, specifies that the price will be applied only when the sales document has the specified Ship-To-Customer. [Filter(multi eq)]

_Type_: **[Customers](Crm.Customers.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

_Front-End Recalc Expressions:_  
`IIF( ( obj.ShipToCustomer.Party.ParentParty != obj.Customer), null, obj.ShipToCustomer)`
### TargetGroup

When not null, specifies a criteria, which is matched only when the customer of the sales document is included in the group. [Filter(multi eq)]

_Type_: **[TargetGroups](Crm.Marketing.TargetGroups.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Crm.ProductPrices erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Crm.ProductPrices erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_ProductPrices?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Crm_ProductPrices?$top=10>

