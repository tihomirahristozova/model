---
uid: Crm.Presales.OfferLines
---
# Crm.Presales.OfferLines

Detail records (lines) of Offers. Entity: Crm_Offer_Lines

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Crm.Presales.OfferLines.md#Id) | guid |  
| [ChoiceGroupName](Crm.Presales.OfferLines.md#ChoiceGroupName) | string (nullable) | Name of a group of alternative lines, only one of which can be selected for ordering. Lines are grouped based on the exact name of the Choice Group. 
| [DeliveryTermDays](Crm.Presales.OfferLines.md#DeliveryTermDays) | int32 | Delivery term in days. When Required Delivery Date is specified (not null), it takes precedence and this is ignored. [Required] [Default(0)] 
| [GuaranteePeriodDays](Crm.Presales.OfferLines.md#GuaranteePeriodDays) | int32 (nullable) | Guarantee period in days for the offered product. null for non-serviced products. 
| [IsSelected](Crm.Presales.OfferLines.md#IsSelected) | boolean | True when the line is selected for further processing (ordering), false otherwise. [Required] [Default(true)] 
| [LineAmount](Crm.Presales.OfferLines.md#LineAmount) | [Amount](../data-types.md#Amount) | Amount for the line in the currency of the parent document. Usually equals Quantity * Unit_Price. When Quantity = 0, Unit Price is undefined and this contains the total line amount. [Currency: Offer.DocumentCurrency] [Required] [Default(0)] 
| [LineCustomDiscountPercent](Crm.Presales.OfferLines.md#LineCustomDiscountPercent) | decimal | Operator defined discount percentage, specified for this line. [Required] [Default(0)] 
| [LineNo](Crm.Presales.OfferLines.md#LineNo) | int32 | Line number, unique within the Offer. Usually is increasing number like 10, 20, 30, ... when initially entering the Offer (in order to allow insertions with adjustment documents). [Required] 
| [LineStandardDiscountPercent](Crm.Presales.OfferLines.md#LineStandardDiscountPercent) | decimal | The discount percentage, applied through the standard discount policy. [Required] [Default(0)] 
| [Notes](Crm.Presales.OfferLines.md#Notes) | string (nullable) | Notes for this OfferLine. 
| [ProductDescription](Crm.Presales.OfferLines.md#ProductDescription) | [MultilanguageString](../data-types.md#MultilanguageString) | The description of the offered product. Initially copied from the name of the offered product. [Required] [Filter(like)] 
| [Quantity](Crm.Presales.OfferLines.md#Quantity) | [Quantity](../data-types.md#Quantity) | Quantity offered. [Unit: QuantityUnit] [Required] [Default(1)] 
| [QuantityBase](Crm.Presales.OfferLines.md#QuantityBase) | [Quantity](../data-types.md#Quantity) | The equivalent of Quantity in the base measurement unit of the Product. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] [ReadOnly] 
| [RequiredDeliveryDate](Crm.Presales.OfferLines.md#RequiredDeliveryDate) | date (nullable) | Date, when the delivery is required. Alternative to Delivery Term Days. When null, Delivery Term Days is used. 
| [StandardQuantityBase](Crm.Presales.OfferLines.md#StandardQuantityBase) | [Quantity](../data-types.md#Quantity) | The theoretical quantity in base measurement unit according to the current measurement dimensions for the product. Used to measure the execution. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] [ReadOnly] (Introduced in version 18.2.100.0) 
| [UnitPrice](Crm.Presales.OfferLines.md#UnitPrice) | [Amount](../data-types.md#Amount) | The unit price of the offered product. It is specified in the measurement unit of Quantity. [Currency: Offer.DocumentCurrency] [Required] [Default(0)] 
| [Variant](Crm.Presales.OfferLines.md#Variant) | string (nullable) | Name or number of variant of the whole offer. When multiple lines have the same variant, they are selected for ordering together. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [LineDiscount](Crm.Presales.OfferLines.md#LineDiscount) | [Crm.LineDiscounts](Crm.LineDiscounts.md) (nullable) | When not null, contains the discount policy selected for this line. [Filter(multi eq)] |
| [Offer](Crm.Presales.OfferLines.md#Offer) | [Crm.Presales.Offers](Crm.Presales.Offers.md) | The [Offer](Crm.Presales.OfferLines.md#Offer) to which this OfferLine belongs. [Required] [Filter(multi eq)] [Owner] |
| [ProductCode](Crm.Presales.OfferLines.md#ProductCode) | [General.Products.ProductCodes](General.Products.ProductCodes.md) (nullable) | Not null, when the product is selected using a coding system code. [Filter(multi eq)] |
| [Product](Crm.Presales.OfferLines.md#Product) | [General.Products.Products](General.Products.Products.md) | The offered product. [Required] [Filter(multi eq)] |
| [ProductPrice](Crm.Presales.OfferLines.md#ProductPrice) | [Crm.ProductPrices](Crm.ProductPrices.md) (nullable) | Not null when the price has been selected from the list of valid standard prices. [Filter(multi eq)] |
| [QuantityUnit](Crm.Presales.OfferLines.md#QuantityUnit) | [General.MeasurementUnits](General.MeasurementUnits.md) | The measurement unit of Quantity. [Required] [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### ChoiceGroupName

> Name of a group of alternative lines, only one of which can be selected for ordering. Lines are grouped based on the exact name of the Choice Group.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### DeliveryTermDays

> Delivery term in days. When Required Delivery Date is specified (not null), it takes precedence and this is ignored. [Required] [Default(0)]

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### GuaranteePeriodDays

> Guarantee period in days for the offered product. null for non-serviced products.

_Type_: **int32 (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`obj.Product.GuaranteePeriodDays`
### IsSelected

> True when the line is selected for further processing (ordering), false otherwise. [Required] [Default(true)]

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### LineAmount

> Amount for the line in the currency of the parent document. Usually equals Quantity * Unit_Price. When Quantity = 0, Unit Price is undefined and this contains the total line amount. [Currency: Offer.DocumentCurrency] [Required] [Default(0)]

_Type_: **[Amount](../data-types.md#Amount)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

_Back-End Default Expression:_  
`IIF((((obj.Quantity == null) OrElse (obj.UnitPrice == null)) OrElse ((obj.Quantity.Value == 0) AndAlso (obj.UnitPrice.Value == 0))), obj.LineAmount, (((obj.Quantity.Value * obj.UnitPrice) * (1 - obj.LineStandardDiscountPercent)) * (1 - obj.LineCustomDiscountPercent)).Round())`

_Front-End Recalc Expressions:_  
`IIF((((obj.Quantity == null) OrElse (obj.UnitPrice == null)) OrElse ((obj.Quantity.Value == 0) AndAlso (obj.UnitPrice.Value == 0))), obj.LineAmount, (((obj.Quantity.Value * obj.UnitPrice) * (1 - obj.LineStandardDiscountPercent)) * (1 - obj.LineCustomDiscountPercent)).Round())`
### LineCustomDiscountPercent

> Operator defined discount percentage, specified for this line. [Required] [Default(0)]

_Type_: **decimal**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### LineNo

> Line number, unique within the Offer. Usually is increasing number like 10, 20, 30, ... when initially entering the Offer (in order to allow insertions with adjustment documents). [Required]

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`(obj.Offer.Lines.Select(c => c.LineNo).DefaultIfEmpty(0).Max() + 10)`

_Front-End Recalc Expressions:_  
`(obj.Offer.Lines.Select(c => c.LineNo).DefaultIfEmpty(0).Max() + 10)`
### LineStandardDiscountPercent

> The discount percentage, applied through the standard discount policy. [Required] [Default(0)]

_Type_: **decimal**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  

_Back-End Default Expression:_  
`obj.LineDiscount.DiscountPercent`

_Front-End Recalc Expressions:_  
`IIF((obj.LineDiscount == null), 0, obj.LineDiscount.DiscountPercent)`
### Notes

> Notes for this OfferLine.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ProductDescription

> The description of the offered product. Initially copied from the name of the offered product. [Required] [Filter(like)]

_Type_: **[MultilanguageString](../data-types.md#MultilanguageString)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`obj.Product.Name`

_Front-End Recalc Expressions:_  
`obj.Product.Name`
### Quantity

> Quantity offered. [Unit: QuantityUnit] [Required] [Default(1)]

_Type_: **[Quantity](../data-types.md#Quantity)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### QuantityBase

> The equivalent of Quantity in the base measurement unit of the Product. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] [ReadOnly]

_Type_: **[Quantity](../data-types.md#Quantity)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`IIF((((obj.Quantity == null) OrElse (obj.QuantityUnit == null)) OrElse (obj.Product == null)), obj.QuantityBase, obj.Quantity.ConvertTo(obj.Product.BaseUnit, obj.Product))`

_Front-End Recalc Expressions:_  
`IIF((((obj.Quantity == null) OrElse (obj.QuantityUnit == null)) OrElse (obj.Product == null)), obj.QuantityBase, obj.Quantity.ConvertTo(obj.Product.BaseUnit, obj.Product))`
### RequiredDeliveryDate

> Date, when the delivery is required. Alternative to Delivery Term Days. When null, Delivery Term Days is used.

_Type_: **date (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`obj.Offer.RequiredDeliveryDate`

_Front-End Recalc Expressions:_  
`IIF((obj.DeliveryTermDays == 0), obj.RequiredDeliveryDate, null)`
`obj.Offer.RequiredDeliveryDate`
### StandardQuantityBase

> The theoretical quantity in base measurement unit according to the current measurement dimensions for the product. Used to measure the execution. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] [ReadOnly] (Introduced in version 18.2.100.0)

_Type_: **[Quantity](../data-types.md#Quantity)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`IIF((((obj.Quantity == null) OrElse (obj.QuantityUnit == null)) OrElse (obj.Product == null)), obj.StandardQuantityBase, obj.Quantity.ConvertTo(obj.Product.BaseUnit, obj.Product))`

_Front-End Recalc Expressions:_  
`IIF((((obj.Quantity == null) OrElse (obj.QuantityUnit == null)) OrElse (obj.Product == null)), obj.StandardQuantityBase, obj.Quantity.ConvertTo(obj.Product.BaseUnit, obj.Product))`
### UnitPrice

> The unit price of the offered product. It is specified in the measurement unit of Quantity. [Currency: Offer.DocumentCurrency] [Required] [Default(0)]

_Type_: **[Amount](../data-types.md#Amount)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

_Back-End Default Expression:_  
`(CalculateUnitPriceFromLineAmount(obj.LineAmount, obj.Quantity, obj.LineStandardDiscountPercent, obj.LineCustomDiscountPercent) ?? obj.UnitPrice)`

_Front-End Recalc Expressions:_  
`obj.CalculateUnitPrice(obj.Product, obj.ProductPrice, obj.QuantityUnit, obj.Offer)`
### Variant

> Name or number of variant of the whole offer. When multiple lines have the same variant, they are selected for ordering together.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### LineDiscount

> When not null, contains the discount policy selected for this line. [Filter(multi eq)]

_Type_: **[Crm.LineDiscounts](Crm.LineDiscounts.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`obj.DetermineLineDiscount(obj.RequiredDeliveryDate, obj.Offer.Customer, obj.Offer.ShipToCustomer, obj.Product, obj.Quantity, obj.QuantityUnit, obj.Offer.EnterpriseCompany, obj.Offer.EnterpriseCompanyLocation, obj.Offer.PriceList, obj.LineDiscount)`
### Offer

> The [Offer](Crm.Presales.OfferLines.md#Offer) to which this OfferLine belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Crm.Presales.Offers](Crm.Presales.Offers.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### ProductCode

> Not null, when the product is selected using a coding system code. [Filter(multi eq)]

_Type_: **[General.Products.ProductCodes](General.Products.ProductCodes.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Product

> The offered product. [Required] [Filter(multi eq)]

_Type_: **[General.Products.Products](General.Products.Products.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`IIF((obj.ProductCode.Product == null), obj.Product, obj.ProductCode.Product)`

_Front-End Recalc Expressions:_  
`IIF((obj.ProductCode.Product == null), obj.Product, obj.ProductCode.Product)`
### ProductPrice

> Not null when the price has been selected from the list of valid standard prices. [Filter(multi eq)]

_Type_: **[Crm.ProductPrices](Crm.ProductPrices.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`DetermineProductPrice(obj.Product, obj.Quantity, obj.QuantityUnit, obj.RequiredDeliveryDate, obj.Offer.Customer, obj.Offer.ShipToCustomer, obj.Offer.EnterpriseCompany, obj.Offer.EnterpriseCompanyLocation, null, obj.Offer.PriceList, obj.ProductPrice)`
### QuantityUnit

> The measurement unit of Quantity. [Required] [Filter(multi eq)]

_Type_: **[General.MeasurementUnits](General.MeasurementUnits.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`obj.Product.MeasurementUnit.IfNullThen(obj.QuantityUnit)`

_Front-End Recalc Expressions:_  
`obj.Product.MeasurementUnit.IfNullThen(obj.QuantityUnit)`


## Business Rules

[!list erp.entity=Crm.Presales.OfferLines erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Crm.Presales.OfferLines erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Crm.Presales.OfferLines erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_Presales_OfferLines?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Crm_Presales_OfferLines?$top=10>

