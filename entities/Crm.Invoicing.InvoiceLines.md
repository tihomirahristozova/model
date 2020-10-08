---
uid: Crm.Invoicing.InvoiceLines
---
# Crm.Invoicing.InvoiceLines

Detail records (lines) of the invoices. Entity: Crm_Invoice_Lines

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Crm.Invoicing.InvoiceLines.md#Id) | guid |  
| [BusinessReason](Crm.Invoicing.InvoiceLines.md#BusinessReason) | [Crm.Invoicing.InvoicingBusinessReason](Crm.Invoicing.InvoiceLines.md#BusinessReason) | Business reason for invoicing of this product or service. S=Shipment, P=Payment. [Required] [Default("S")] 
| [DeliveryTermsCode](Crm.Invoicing.InvoiceLines.md#DeliveryTermsCode) | [Finance.Intrastat.DeliveryTerms](Crm.Invoicing.InvoiceLines.md#DeliveryTermsCode) (nullable) | Mode of delivery, like CIF, FOB, etc. Used also in Intrastat reporting. 
| [IntrastatTransactionNatureCode](Crm.Invoicing.InvoiceLines.md#IntrastatTransactionNatureCode) | [Finance.Intrastat.TransactionNature](Crm.Invoicing.InvoiceLines.md#IntrastatTransactionNatureCode) (nullable) | Transaction nature; used for Intrastat reporting. 
| [IntrastatTransportModeCode](Crm.Invoicing.InvoiceLines.md#IntrastatTransportModeCode) | [Finance.Intrastat.TransportMode](Crm.Invoicing.InvoiceLines.md#IntrastatTransportModeCode) (nullable) | Transport mode; used for Intrastat reporting. 
| [LineAmount](Crm.Invoicing.InvoiceLines.md#LineAmount) | [Amount](../data-types.md#Amount) | Amount for the line in the currency of the parent document. Usually equals Quantity * Unit_Price. When Quantity = 0, Unit Price is undefined and this contains the total line amount. [Currency: Invoice.DocumentCurrency] [Required] [Default(0)] 
| [LineCustomDiscountPercent](Crm.Invoicing.InvoiceLines.md#LineCustomDiscountPercent) | decimal | User-defined discount for the line. [Required] [Default(0)] [Filter(ge;le)] 
| [LineNo](Crm.Invoicing.InvoiceLines.md#LineNo) | int32 | Consecutive line number, unique within the invoice. Usually is increasing in steps of 10, like in 10, 20, 30, etc. [Required] [Filter(eq)] 
| [LineStandardDiscountPercent](Crm.Invoicing.InvoiceLines.md#LineStandardDiscountPercent) | decimal | Standard discount for the line. This is automatically computed according to discount conditions. [Required] [Default(0)] 
| [Notes](Crm.Invoicing.InvoiceLines.md#Notes) | string (nullable) | Notes for this InvoiceLine. 
| [ParentLineNo](Crm.Invoicing.InvoiceLines.md#ParentLineNo) | int32 (nullable) | The number of the line within the parent document, which the current line executes. null when the current line does not execute line. (Introduced in version 18.2.100.0) 
| [ProductDescription](Crm.Invoicing.InvoiceLines.md#ProductDescription) | [MultilanguageString](../data-types.md#MultilanguageString) | The description of the invoiced product. Initially copied from the name of the invoiced Product or from the generating document. [Required] 
| [Quantity](Crm.Invoicing.InvoiceLines.md#Quantity) | [Quantity](../data-types.md#Quantity) | The quantity of the invoiced product. [Unit: QuantityUnit] [Required] [Default(1)] [Filter(ge;le)] 
| [QuantityBase](Crm.Invoicing.InvoiceLines.md#QuantityBase) | [Quantity](../data-types.md#Quantity) | The equivalent of Quantity in the base measurement unit of the Product. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] 
| [SalesOrderAmount](Crm.Invoicing.InvoiceLines.md#SalesOrderAmount) | decimal (nullable) | Specifies what portion of the amount of the sales order is invoiced with this line. The amount is calculated with respect to the trade conditions (prices, discounts, etc.) from the sales order. Can be different from the total amount of the line when the trade conditions from the sales order have changed before invoicing. 
| [StandardQuantityBase](Crm.Invoicing.InvoiceLines.md#StandardQuantityBase) | [Quantity](../data-types.md#Quantity) | The theoretical quantity in base measurement unit according to the current measurement dimensions for the product. Used to measure the execution. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] [ReadOnly] (Introduced in version 18.2.100.0) 
| [UnitPrice](Crm.Invoicing.InvoiceLines.md#UnitPrice) | [Amount](../data-types.md#Amount) | The unit selling price of Quantity. [Currency: Invoice.DocumentCurrency] [Required] [Default(0)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [IntrastatTransportCountry](Crm.Invoicing.InvoiceLines.md#IntrastatTransportCountry) | [General.Geography.Countries](General.Geography.Countries.md) (nullable) | Country of origin of the transport company; used for Intrastat reporting. [Filter(multi eq)] |
| [Invoice](Crm.Invoicing.InvoiceLines.md#Invoice) | [Crm.Invoicing.Invoices](Crm.Invoicing.Invoices.md) | The [Invoice](Crm.Invoicing.InvoiceLines.md#Invoice) to which this InvoiceLine belongs. [Required] [Filter(multi eq)] [Owner] |
| [InvoiceOrderLine](Crm.Invoicing.InvoiceLines.md#InvoiceOrderLine) | [Crm.Invoicing.InvoiceOrderLines](Crm.Invoicing.InvoiceOrderLines.md) (nullable) | Invoice order line which is invoiced by this line. [Filter(multi eq)] |
| [LineDealType](Crm.Invoicing.InvoiceLines.md#LineDealType) | [Finance.Vat.DealTypes](Finance.Vat.DealTypes.md) (nullable) | Deal type for this line. If deal type in the line is different from deal type in the header another VAT entry is created. [Filter(multi eq)] |
| [LineDiscount](Crm.Invoicing.InvoiceLines.md#LineDiscount) | [Crm.LineDiscounts](Crm.LineDiscounts.md) (nullable) | The line discount type used to form the Line_Standard_Discount_Percent. [Filter(multi eq)] |
| [ParentDocument](Crm.Invoicing.InvoiceLines.md#ParentDocument) | [General.Documents](General.Documents.md) (nullable) | The document, which the current line executes. null when the current line does not execute another line. [Filter(multi eq)] (Introduced in version 18.2.100.0) |
| [ParentSalesOrderLine](Crm.Invoicing.InvoiceLines.md#ParentSalesOrderLine) | [Crm.Sales.SalesOrderLines](Crm.Sales.SalesOrderLines.md) (nullable) | When not null specifies the Sales Order line that is invoiced by this invoice line. [Filter(multi eq)] |
| [PaymentTransaction](Crm.Invoicing.InvoiceLines.md#PaymentTransaction) | [Finance.Payments.PaymentTransactions](Finance.Payments.PaymentTransactions.md) (nullable) | The payment transaction, which is invoiced by this line, when Business Reason = P. Used to reconcile the invoice with the payments in the case of advance payment. [Filter(multi eq)] |
| [Product](Crm.Invoicing.InvoiceLines.md#Product) | [General.Products.Products](General.Products.Products.md) (nullable) | The invoiced product. When null, although rarely used, the invoice line is still valid and the Product Description contains the invoiced item. [Filter(multi eq)] |
| [QuantityUnit](Crm.Invoicing.InvoiceLines.md#QuantityUnit) | [General.MeasurementUnits](General.MeasurementUnits.md) | The measurement unit of Quantity. [Required] [Filter(multi eq)] |
| [SalesOrder](Crm.Invoicing.InvoiceLines.md#SalesOrder) | [Crm.Sales.SalesOrders](Crm.Sales.SalesOrders.md) (nullable) | When not null specifies the Sales Order that is invoiced by this line. [Filter(multi eq;like)] |
| [SerialNumber](Crm.Invoicing.InvoiceLines.md#SerialNumber) | [Logistics.Inventory.SerialNumbers](Logistics.Inventory.SerialNumbers.md) (nullable) | Which serial number to receive/issue. null means that serial number is unknown or not applicable. [Filter(multi eq)] |
| [TransactionLine](Crm.Invoicing.InvoiceLines.md#TransactionLine) | [Logistics.Inventory.StoreTransactionLines](Logistics.Inventory.StoreTransactionLines.md) (nullable) | The store transaction line that is invoiced by this line, for Business Reason = S. [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### BusinessReason

> Business reason for invoicing of this product or service. S=Shipment, P=Payment. [Required] [Default("S")]

_Type_: **[Crm.Invoicing.InvoicingBusinessReason](Crm.Invoicing.InvoiceLines.md#BusinessReason)**  
Generic enum type for InvoicingBusinessReason properties  
_Allowed Values (Enum Members)_  

| Value | Description |
| ---- | --- |
| Payment | Payment value. Stored as 'P'. <br /> _Database Value:_ 'P' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Payment' |
| Shipment | Shipment value. Stored as 'S'. <br /> _Database Value:_ 'S' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'Shipment' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Shipment**  

### DeliveryTermsCode

> Mode of delivery, like CIF, FOB, etc. Used also in Intrastat reporting.

_Type_: **[Finance.Intrastat.DeliveryTerms](Crm.Invoicing.InvoiceLines.md#DeliveryTermsCode) (nullable)**  
Generic enum type for DeliveryTerms properties  
_Allowed Values (Enum Members)_  

| Value | Description |
| ---- | --- |
| ExWorks | ExWorks value. Stored as 'EXW'. <br /> _Database Value:_ 'EXW' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'ExWorks' |
| FrancoCarrier | FrancoCarrier value. Stored as 'FCA'. <br /> _Database Value:_ 'FCA' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'FrancoCarrier' |
| FreeAlongsideShip | FreeAlongsideShip value. Stored as 'FAS'. <br /> _Database Value:_ 'FAS' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'FreeAlongsideShip' |
| FreeOnBoard | FreeOnBoard value. Stored as 'FOB'. <br /> _Database Value:_ 'FOB' <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'FreeOnBoard' |
| CostAndFreightCF | CostAndFreightCF value. Stored as 'CFR'. <br /> _Database Value:_ 'CFR' <br /> _Model Value:_ 4 <br /> _Domain API Value:_ 'CostAndFreightCF' |
| CostInsuranceAndFreight | CostInsuranceAndFreight value. Stored as 'CIF'. <br /> _Database Value:_ 'CIF' <br /> _Model Value:_ 5 <br /> _Domain API Value:_ 'CostInsuranceAndFreight' |
| CarriagePaidTo | CarriagePaidTo value. Stored as 'CPT'. <br /> _Database Value:_ 'CPT' <br /> _Model Value:_ 6 <br /> _Domain API Value:_ 'CarriagePaidTo' |
| CarriageAndInsurancePaidTo | CarriageAndInsurancePaidTo value. Stored as 'CIP'. <br /> _Database Value:_ 'CIP' <br /> _Model Value:_ 7 <br /> _Domain API Value:_ 'CarriageAndInsurancePaidTo' |
| DeliveredAtPlace | DeliveredAtPlace value. Stored as 'DAP'. <br /> _Database Value:_ 'DAP' <br /> _Model Value:_ 8 <br /> _Domain API Value:_ 'DeliveredAtPlace' |
| DeliveredAtTerminal | DeliveredAtTerminal value. Stored as 'DAT'. <br /> _Database Value:_ 'DAT' <br /> _Model Value:_ 9 <br /> _Domain API Value:_ 'DeliveredAtTerminal' |
| DeliveredDutyPaid | DeliveredDutyPaid value. Stored as 'DDP'. <br /> _Database Value:_ 'DDP' <br /> _Model Value:_ 10 <br /> _Domain API Value:_ 'DeliveredDutyPaid' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`obj.Invoice.DeliveryTermsCode`

_Front-End Recalc Expressions:_  
`obj.Invoice.DeliveryTermsCode`
### IntrastatTransactionNatureCode

> Transaction nature; used for Intrastat reporting.

_Type_: **[Finance.Intrastat.TransactionNature](Crm.Invoicing.InvoiceLines.md#IntrastatTransactionNatureCode) (nullable)**  
Generic enum type for TransactionNature properties  
_Allowed Values (Enum Members)_  

| Value | Description |
| ---- | --- |
| OutrightPurchaseOrSale | OutrightPurchaseOrSale value. Stored as '11'. <br /> _Database Value:_ '11' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'OutrightPurchaseOrSale' |
| SupplyForSale | SupplyForSale value. Stored as '12'. <br /> _Database Value:_ '12' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'SupplyForSale' |
| BarterTrade | BarterTrade value. Stored as '13'. <br /> _Database Value:_ '13' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'BarterTrade' |
| FinancialLeasing | FinancialLeasing value. Stored as '14'. <br /> _Database Value:_ '14' <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'FinancialLeasing' |
| OtherTransactions | OtherTransactions value. Stored as '19'. <br /> _Database Value:_ '19' <br /> _Model Value:_ 4 <br /> _Domain API Value:_ 'OtherTransactions' |
| ReturnStokilizing | ReturnStokilizing value. Stored as '21'. <br /> _Database Value:_ '21' <br /> _Model Value:_ 5 <br /> _Domain API Value:_ 'ReturnStokilizing' |
| ReplacementForReturnedGoods | ReplacementForReturnedGoods value. Stored as '22'. <br /> _Database Value:_ '22' <br /> _Model Value:_ 6 <br /> _Domain API Value:_ 'ReplacementForReturnedGoods' |
| ReplacementOfGoodsNotBeingReturned | ReplacementOfGoodsNotBeingReturned value. Stored as '23'. <br /> _Database Value:_ '23' <br /> _Model Value:_ 7 <br /> _Domain API Value:_ 'ReplacementOfGoodsNotBeingReturned' |
| ReturnOrExchangeOfOtherGoods | ReturnOrExchangeOfOtherGoods value. Stored as '29'. <br /> _Database Value:_ '29' <br /> _Model Value:_ 8 <br /> _Domain API Value:_ 'ReturnOrExchangeOfOtherGoods' |
| SpecificTransactions | SpecificTransactions value. Stored as '60'. <br /> _Database Value:_ '60' <br /> _Model Value:_ 9 <br /> _Domain API Value:_ 'SpecificTransactions' |
| OperationsOnJointProjects | OperationsOnJointProjects value. Stored as '70'. <br /> _Database Value:_ '70' <br /> _Model Value:_ 10 <br /> _Domain API Value:_ 'OperationsOnJointProjects' |
| TransactionsOfConstructionMaterialsAndEquipment | TransactionsOfConstructionMaterialsAndEquipment value. Stored as '80'. <br /> _Database Value:_ '80' <br /> _Model Value:_ 11 <br /> _Domain API Value:_ 'TransactionsOfConstructionMaterialsAndEquipment' |
| OtherTransactionsLeasing | OtherTransactionsLeasing value. Stored as '91'. <br /> _Database Value:_ '91' <br /> _Model Value:_ 12 <br /> _Domain API Value:_ 'OtherTransactionsLeasing' |
| OtherTransactionsOther | OtherTransactionsOther value. Stored as '99'. <br /> _Database Value:_ '99' <br /> _Model Value:_ 13 <br /> _Domain API Value:_ 'OtherTransactionsOther' |
| DealsThatIncludePropertyTransfersWithoutFinancialCompensationOrCompensationInKind | DealsThatIncludePropertyTransfersWithoutFinancialCompensationOrCompensationInKind value. Stored as '30'. <br /> _Database Value:_ '30' <br /> _Model Value:_ 14 <br /> _Domain API Value:_ 'DealsThatIncludePropertyTransfersWithoutFinancialCompensationOrCompensationInKind' |
| GoodsThatAreExpectedToBeReturnedToSender | GoodsThatAreExpectedToBeReturnedToSender value. Stored as '41'. <br /> _Database Value:_ '41' <br /> _Model Value:_ 15 <br /> _Domain API Value:_ 'GoodsThatAreExpectedToBeReturnedToSender' |
| GoodsThatAreNotExpectedToBeReturnedToSender | GoodsThatAreNotExpectedToBeReturnedToSender value. Stored as '42'. <br /> _Database Value:_ '42' <br /> _Model Value:_ 16 <br /> _Domain API Value:_ 'GoodsThatAreNotExpectedToBeReturnedToSender' |
| GoodsThatAreReturnedToSender | GoodsThatAreReturnedToSender value. Stored as '51'. <br /> _Database Value:_ '51' <br /> _Model Value:_ 17 <br /> _Domain API Value:_ 'GoodsThatAreReturnedToSender' |
| GoodsThatAreNotReturnedToSender | GoodsThatAreNotReturnedToSender value. Stored as '52'. <br /> _Database Value:_ '52' <br /> _Model Value:_ 18 <br /> _Domain API Value:_ 'GoodsThatAreNotReturnedToSender' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`obj.Invoice.IntrastatTransactionNatureCode`

_Front-End Recalc Expressions:_  
`obj.Invoice.IntrastatTransactionNatureCode`
### IntrastatTransportModeCode

> Transport mode; used for Intrastat reporting.

_Type_: **[Finance.Intrastat.TransportMode](Crm.Invoicing.InvoiceLines.md#IntrastatTransportModeCode) (nullable)**  
Generic enum type for TransportMode properties  
_Allowed Values (Enum Members)_  

| Value | Description |
| ---- | --- |
| Shipping | Shipping value. Stored as '1'. <br /> _Database Value:_ '1' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Shipping' |
| RailwayTransport | RailwayTransport value. Stored as '2'. <br /> _Database Value:_ '2' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'RailwayTransport' |
| RoadTransport | RoadTransport value. Stored as '3'. <br /> _Database Value:_ '3' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'RoadTransport' |
| AirTransport | AirTransport value. Stored as '4'. <br /> _Database Value:_ '4' <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'AirTransport' |
| Mail | Mail value. Stored as '5'. <br /> _Database Value:_ '5' <br /> _Model Value:_ 4 <br /> _Domain API Value:_ 'Mail' |
| FixedTransportInstallations | FixedTransportInstallations value. Stored as '6'. <br /> _Database Value:_ '6' <br /> _Model Value:_ 5 <br /> _Domain API Value:_ 'FixedTransportInstallations' |
| RiverTransport | RiverTransport value. Stored as '7'. <br /> _Database Value:_ '7' <br /> _Model Value:_ 6 <br /> _Domain API Value:_ 'RiverTransport' |
| SelfPropelled | SelfPropelled value. Stored as '8'. <br /> _Database Value:_ '8' <br /> _Model Value:_ 7 <br /> _Domain API Value:_ 'SelfPropelled' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`obj.Invoice.IntrastatTransportModeCode`

_Front-End Recalc Expressions:_  
`obj.Invoice.IntrastatTransportModeCode`
### LineAmount

> Amount for the line in the currency of the parent document. Usually equals Quantity * Unit_Price. When Quantity = 0, Unit Price is undefined and this contains the total line amount. [Currency: Invoice.DocumentCurrency] [Required] [Default(0)]

_Type_: **[Amount](../data-types.md#Amount)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

_Front-End Recalc Expressions:_  
`obj.CalculateLineAmount(obj.Quantity, obj.UnitPrice, Convert(obj.LineStandardDiscountPercent, Nullable`1), Convert(obj.LineCustomDiscountPercent, Nullable`1), obj.Invoice.DocumentCurrency)`
### LineCustomDiscountPercent

> User-defined discount for the line. [Required] [Default(0)] [Filter(ge;le)]

_Type_: **decimal**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### LineNo

> Consecutive line number, unique within the invoice. Usually is increasing in steps of 10, like in 10, 20, 30, etc. [Required] [Filter(eq)]

_Type_: **int32**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`(obj.Invoice.Lines.Select(c => c.LineNo).DefaultIfEmpty(0).Max() + 10)`

_Front-End Recalc Expressions:_  
`(obj.Invoice.Lines.Select(c => c.LineNo).DefaultIfEmpty(0).Max() + 10)`
### LineStandardDiscountPercent

> Standard discount for the line. This is automatically computed according to discount conditions. [Required] [Default(0)]

_Type_: **decimal**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  

_Front-End Recalc Expressions:_  
`IIF((obj.LineDiscount != null), obj.LineDiscount.DiscountPercent, 0)`
### Notes

> Notes for this InvoiceLine.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ParentLineNo

> The number of the line within the parent document, which the current line executes. null when the current line does not execute line. (Introduced in version 18.2.100.0)

_Type_: **int32 (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ProductDescription

> The description of the invoiced product. Initially copied from the name of the invoiced Product or from the generating document. [Required]

_Type_: **[MultilanguageString](../data-types.md#MultilanguageString)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`obj.Product.Name`
### Quantity

> The quantity of the invoiced product. [Unit: QuantityUnit] [Required] [Default(1)] [Filter(ge;le)]

_Type_: **[Quantity](../data-types.md#Quantity)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### QuantityBase

> The equivalent of Quantity in the base measurement unit of the Product. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required]

_Type_: **[Quantity](../data-types.md#Quantity)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`IIF((((obj.Quantity == null) OrElse (obj.QuantityUnit == null)) OrElse (obj.Product == null)), obj.QuantityBase, obj.Quantity.ConvertTo(obj.Product.BaseUnit, obj.Product))`

_Front-End Recalc Expressions:_  
`IIF((((obj.Quantity == null) OrElse (obj.QuantityUnit == null)) OrElse (obj.Product == null)), obj.QuantityBase, obj.Quantity.ConvertTo(obj.Product.BaseUnit, obj.Product))`
### SalesOrderAmount

> Specifies what portion of the amount of the sales order is invoiced with this line. The amount is calculated with respect to the trade conditions (prices, discounts, etc.) from the sales order. Can be different from the total amount of the line when the trade conditions from the sales order have changed before invoicing.

_Type_: **decimal (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

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

> The unit selling price of Quantity. [Currency: Invoice.DocumentCurrency] [Required] [Default(0)]

_Type_: **[Amount](../data-types.md#Amount)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  


## Reference Details

### IntrastatTransportCountry

> Country of origin of the transport company; used for Intrastat reporting. [Filter(multi eq)]

_Type_: **[General.Geography.Countries](General.Geography.Countries.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`obj.Invoice.IntrastatTransportCountry`

_Front-End Recalc Expressions:_  
`obj.Invoice.IntrastatTransportCountry`
### Invoice

> The [Invoice](Crm.Invoicing.InvoiceLines.md#Invoice) to which this InvoiceLine belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Crm.Invoicing.Invoices](Crm.Invoicing.Invoices.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### InvoiceOrderLine

> Invoice order line which is invoiced by this line. [Filter(multi eq)]

_Type_: **[Crm.Invoicing.InvoiceOrderLines](Crm.Invoicing.InvoiceOrderLines.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### LineDealType

> Deal type for this line. If deal type in the line is different from deal type in the header another VAT entry is created. [Filter(multi eq)]

_Type_: **[Finance.Vat.DealTypes](Finance.Vat.DealTypes.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`obj.Invoice.DealType`

_Front-End Recalc Expressions:_  
`obj.Invoice.DealType`
### LineDiscount

> The line discount type used to form the Line_Standard_Discount_Percent. [Filter(multi eq)]

_Type_: **[Crm.LineDiscounts](Crm.LineDiscounts.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`obj.DetermineLineDiscount(Convert((obj.Invoice.DeliveryDate ?? obj.Invoice.DocumentDate), Nullable`1), obj.Invoice.Customer, obj.Product, obj.Quantity, obj.Invoice.EnterpriseCompany, obj.Invoice.EnterpriseCompanyLocation, IIF((obj.SalesOrder == null), null, obj.SalesOrder.DistributionChannel), IIF((obj.SalesOrder == null), null, obj.SalesOrder.PriceList))`
### ParentDocument

> The document, which the current line executes. null when the current line does not execute another line. [Filter(multi eq)] (Introduced in version 18.2.100.0)

_Type_: **[General.Documents](General.Documents.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### ParentSalesOrderLine

> When not null specifies the Sales Order line that is invoiced by this invoice line. [Filter(multi eq)]

_Type_: **[Crm.Sales.SalesOrderLines](Crm.Sales.SalesOrderLines.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### PaymentTransaction

> The payment transaction, which is invoiced by this line, when Business Reason = P. Used to reconcile the invoice with the payments in the case of advance payment. [Filter(multi eq)]

_Type_: **[Finance.Payments.PaymentTransactions](Finance.Payments.PaymentTransactions.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Product

> The invoiced product. When null, although rarely used, the invoice line is still valid and the Product Description contains the invoiced item. [Filter(multi eq)]

_Type_: **[General.Products.Products](General.Products.Products.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### QuantityUnit

> The measurement unit of Quantity. [Required] [Filter(multi eq)]

_Type_: **[General.MeasurementUnits](General.MeasurementUnits.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`obj.Product.MeasurementUnit`
### SalesOrder

> When not null specifies the Sales Order that is invoiced by this line. [Filter(multi eq;like)]

_Type_: **[Crm.Sales.SalesOrders](Crm.Sales.SalesOrders.md) (nullable)**  
_Supported Filters_: **Equals, Like, EqualsIn**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`IIF((obj.ParentSalesOrderLine != null), obj.ParentSalesOrderLine.SalesOrder, null)`
### SerialNumber

> Which serial number to receive/issue. null means that serial number is unknown or not applicable. [Filter(multi eq)]

_Type_: **[Logistics.Inventory.SerialNumbers](Logistics.Inventory.SerialNumbers.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### TransactionLine

> The store transaction line that is invoiced by this line, for Business Reason = S. [Filter(multi eq)]

_Type_: **[Logistics.Inventory.StoreTransactionLines](Logistics.Inventory.StoreTransactionLines.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Crm.Invoicing.InvoiceLines erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Crm.Invoicing.InvoiceLines erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Crm.Invoicing.InvoiceLines erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_Invoicing_InvoiceLines?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Crm_Invoicing_InvoiceLines?$top=10>

