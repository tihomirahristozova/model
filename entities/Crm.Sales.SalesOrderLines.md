---
uid: Crm.Sales.SalesOrderLines
---
# Crm.Sales.SalesOrderLines

Sales Orders detail records. Entity: Crm_Sales_Order_Lines

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Crm.Sales.SalesOrderLines.md#Id) | guid |  
| [DeliveryTermsCode](Crm.Sales.SalesOrderLines.md#DeliveryTermsCode) | [Finance.Intrastat.DeliveryTerms](Crm.Sales.SalesOrderLines.md#DeliveryTermsCode) (nullable) | Mode of delivery, like CIF, FOB, etc. Used also in Intrastat reporting. 
| [GuaranteePeriodDays](Crm.Sales.SalesOrderLines.md#GuaranteePeriodDays) | int32 (nullable) | Guarantee period in days for the offered product. null for non-serviced products. 
| [HistoricalDataJson](Crm.Sales.SalesOrderLines.md#HistoricalDataJson) | string (nullable) | Used only for lines, which are returns. It is a JSON-formatted string, containing data from the original sale. (Introduced in version 19.1.100.0) 
| [HistoricalUnitCost](Crm.Sales.SalesOrderLines.md#HistoricalUnitCost) | [Amount](../data-types.md#Amount) (nullable) | Used for returning of goods that are sold before the exploitation of the system. [Currency: SalesOrder.DocumentCurrency] [Filter(eq;ge;le)] 
| [IntrastatTransactionNatureCode](Crm.Sales.SalesOrderLines.md#IntrastatTransactionNatureCode) | [Finance.Intrastat.TransactionNature](Crm.Sales.SalesOrderLines.md#IntrastatTransactionNatureCode) (nullable) | Transaction nature; used for Intrastat reporting. 
| [IntrastatTransportModeCode](Crm.Sales.SalesOrderLines.md#IntrastatTransportModeCode) | [Finance.Intrastat.TransportMode](Crm.Sales.SalesOrderLines.md#IntrastatTransportModeCode) (nullable) | Transport mode; used for Intrastat reporting. 
| [LineAmount](Crm.Sales.SalesOrderLines.md#LineAmount) | [Amount](../data-types.md#Amount) | The total amount for the line. Equals to Quantity * Unit_Price, less the discounts. [Currency: SalesOrder.DocumentCurrency] [Required] [Default(0)] 
| [LineCustomDiscountPercent](Crm.Sales.SalesOrderLines.md#LineCustomDiscountPercent) | decimal | User-defined discount for the line. [Required] [Default(0)] [Filter(ge;le)] 
| [LineFromDate](Crm.Sales.SalesOrderLines.md#LineFromDate) | date (nullable) | When selling a service valid only for a period, denotes the beginning of the period. null means that it is unknown or N/A. (Introduced in version 20.1.100.0) 
| [LineNo](Crm.Sales.SalesOrderLines.md#LineNo) | int32 | Consecutive number of the line within the sales order. [Required] [Filter(eq)] [ORD] 
| [LineStandardDiscountPercent](Crm.Sales.SalesOrderLines.md#LineStandardDiscountPercent) | decimal | Standard discount for the line. This is automatically computed according to discount conditions. [Required] [Default(0)] [ReadOnly] 
| [LineToDate](Crm.Sales.SalesOrderLines.md#LineToDate) | date (nullable) | When selling a service valid only for a period, denotes the end of the period. null means that it is unknown or N/A. (Introduced in version 20.1.100.0) 
| [Notes](Crm.Sales.SalesOrderLines.md#Notes) | string (nullable) | Notes for this SalesOrderLine. 
| [ParentLineNo](Crm.Sales.SalesOrderLines.md#ParentLineNo) | int32 (nullable) | The number of the line within the parent document, which the current line executes. null when the current line does not execute parent line. [Filter(eq)] 
| [PersistLot](Crm.Sales.SalesOrderLines.md#PersistLot) | boolean | If checked specifies that the lot in the line cannot be changed in the sub-documents created by the current document. [Required] [Default(false)] [Filter(eq)] 
| [ProductDescription](Crm.Sales.SalesOrderLines.md#ProductDescription) | [MultilanguageString](../data-types.md#MultilanguageString) | The name of the sold product at the time the sale was made. [Required] [Filter(like)] 
| [Quantity](Crm.Sales.SalesOrderLines.md#Quantity) | [Quantity](../data-types.md#Quantity) | The quantity sold. [Unit: QuantityUnit] [Required] [Default(1)] [Filter(ge;le)] 
| [QuantityBase](Crm.Sales.SalesOrderLines.md#QuantityBase) | [Quantity](../data-types.md#Quantity) | The equivalent of Quantity in the base measurement category of the product. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] 
| [RequestedQuantity](Crm.Sales.SalesOrderLines.md#RequestedQuantity) | [Quantity](../data-types.md#Quantity) (nullable) | Quantity requested by customer. [Unit: QuantityUnit] 
| [RequiredDeliveryDate](Crm.Sales.SalesOrderLines.md#RequiredDeliveryDate) | date (nullable) | The required (contracted) delivery date for the line. [Filter(ge;le)] 
| [StandardQuantityBase](Crm.Sales.SalesOrderLines.md#StandardQuantityBase) | [Quantity](../data-types.md#Quantity) | The theoretical quantity in base measurement unit according to the current measurement dimensions for the product. Used to measure the execution. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] [ReadOnly] (Introduced in version 18.2.100.0) 
| [StandardUnitPrice](Crm.Sales.SalesOrderLines.md#StandardUnitPrice) | [Amount](../data-types.md#Amount) (nullable) | Standard unit price of the product during the creation of the sales order line. [Currency: SalesOrder.DocumentCurrency] [ReadOnly] 
| [UnitPrice](Crm.Sales.SalesOrderLines.md#UnitPrice) | [Amount](../data-types.md#Amount) | Unit price of the product in the currency of the sales order and in the unit of measure, as specified by QuantityUnitId. [Currency: SalesOrder.DocumentCurrency] [Required] [Default(0)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [BonusProgram](Crm.Sales.SalesOrderLines.md#BonusProgram) | [Crm.Marketing.BonusPrograms](Crm.Marketing.BonusPrograms.md) (nullable) | The bonus program, based on which the line was automatically added. null when the line was not added for bonus program. [Filter(multi eq)] |
| [IntrastatTransportCountry](Crm.Sales.SalesOrderLines.md#IntrastatTransportCountry) | [General.Geography.Countries](General.Geography.Countries.md) (nullable) | Country of origin of the transport company; used for Intrastat reporting. [Filter(multi eq)] |
| [LineDealType](Crm.Sales.SalesOrderLines.md#LineDealType) | [Finance.Vat.DealTypes](Finance.Vat.DealTypes.md) (nullable) | Deal type to be passed to the invoice line. If deal type in entered then the invoice creates VAT entry for this deal type. [Filter(multi eq)] |
| [LineDiscount](Crm.Sales.SalesOrderLines.md#LineDiscount) | [Crm.LineDiscounts](Crm.LineDiscounts.md) (nullable) | The line discount type used to form the Line_Standard_Discount_Percent. [Filter(multi eq)] |
| [LineEndCustomerParty](Crm.Sales.SalesOrderLines.md#LineEndCustomerParty) | [General.Contacts.Parties](General.Contacts.Parties.md) (nullable) | The end customer is the customer of the dealer. It is stored for information purposes only. The end customer may not have customer definition, just party. [Filter(multi eq)] (Introduced in version 20.1.100.0) |
| [LineStore](Crm.Sales.SalesOrderLines.md#LineStore) | [Logistics.Inventory.Stores](Logistics.Inventory.Stores.md) (nullable) | The store which should be used to issue the goods for the line. null means to use the store from the header. [Filter(multi eq;like)] |
| [Lot](Crm.Sales.SalesOrderLines.md#Lot) | [Logistics.Inventory.Lots](Logistics.Inventory.Lots.md) (nullable) | Specifies the lot from which the goods should be issued. null means that the lot will be specified at a later stage (store order, etc.). [Filter(multi eq)] |
| [ParentDocument](Crm.Sales.SalesOrderLines.md#ParentDocument) | [General.Documents](General.Documents.md) (nullable) | The document, which the current line executes. null when the current line does not execute another line. [Filter(multi eq)] |
| [ProductCode](Crm.Sales.SalesOrderLines.md#ProductCode) | [General.Products.ProductCodes](General.Products.ProductCodes.md) (nullable) | Used to set the Product_Id thru the coding systems. [Filter(multi eq)] |
| [Product](Crm.Sales.SalesOrderLines.md#Product) | [General.Products.Products](General.Products.Products.md) | The product sold. [Required] [Filter(multi eq)] |
| [ProductPrice](Crm.Sales.SalesOrderLines.md#ProductPrice) | [Crm.ProductPrices](Crm.ProductPrices.md) (nullable) | Not null when the price has been selected from the list of valid standard prices. [Filter(multi eq)] |
| [ProductVariant](Crm.Sales.SalesOrderLines.md#ProductVariant) | [General.ProductVariants](General.ProductVariants.md) (nullable) | If specified determines which product variant of the current product in this line is used. [Filter(multi eq)] |
| [PromotionalPackage](Crm.Sales.SalesOrderLines.md#PromotionalPackage) | [Crm.PromotionalPackages](Crm.PromotionalPackages.md) (nullable) | The promotional package, based on which the line was added. null when the line was not added as part of a promotional package. [Filter(multi eq)] [ReadOnly] |
| [QuantityUnit](Crm.Sales.SalesOrderLines.md#QuantityUnit) | [General.MeasurementUnits](General.MeasurementUnits.md) | The measurement unit of Quantity. [Required] [Filter(multi eq)] |
| [ReturnForInvoiceLine](Crm.Sales.SalesOrderLines.md#ReturnForInvoiceLine) | [Crm.Invoicing.InvoiceLines](Crm.Invoicing.InvoiceLines.md) (nullable) | When specified, indicates that the current line is a return for products, invoiced with the specified invoice line. [Filter(multi eq)] |
| [ReturnForSalesOrderLine](Crm.Sales.SalesOrderLines.md#ReturnForSalesOrderLine) | [Crm.Sales.SalesOrderLines](Crm.Sales.SalesOrderLines.md) (nullable) | When specified indicates that the goods sold in Return_For_Sales_Order_Line_Id are returned with the current line. [Filter(multi eq)] |
| [SalesOrder](Crm.Sales.SalesOrderLines.md#SalesOrder) | [Crm.Sales.SalesOrders](Crm.Sales.SalesOrders.md) | The [SalesOrder](Crm.Sales.SalesOrderLines.md#SalesOrder) to which this SalesOrderLine belongs. [Required] [Filter(multi eq)] [Owner] |
| [SerialNumber](Crm.Sales.SalesOrderLines.md#SerialNumber) | [Logistics.Inventory.SerialNumbers](Logistics.Inventory.SerialNumbers.md) (nullable) | Which serial number to receive/issue. null means that serial number is unknown or not applicable. [Filter(multi eq)] |
| [StoreBin](Crm.Sales.SalesOrderLines.md#StoreBin) | [Logistics.Inventory.StoreBins](Logistics.Inventory.StoreBins.md) (nullable) | The bin from which the goods should be withdrawn. null means that the bin will be specified at a later stage (store order, etc.). [Filter(multi eq)] |
| [Document](Crm.Sales.SalesOrderLines.md#Document) | [Crm.Sales.SalesOrders](Crm.Sales.SalesOrders.md) | The [SalesOrder](Crm.Sales.SalesOrderLines.md#SalesOrder) to which this SalesOrderLine belongs. [Required] [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### DeliveryTermsCode

> Mode of delivery, like CIF, FOB, etc. Used also in Intrastat reporting.

_Type_: **[Finance.Intrastat.DeliveryTerms](Crm.Sales.SalesOrderLines.md#DeliveryTermsCode) (nullable)**  
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
`obj.SalesOrder.DeliveryTermsCode`

_Front-End Recalc Expressions:_  
`obj.SalesOrder.DeliveryTermsCode`
### GuaranteePeriodDays

> Guarantee period in days for the offered product. null for non-serviced products.

_Type_: **int32 (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`IIF((obj.Product != null), obj.Product.GuaranteePeriodDays, obj.GuaranteePeriodDays)`
### HistoricalDataJson

> Used only for lines, which are returns. It is a JSON-formatted string, containing data from the original sale. (Introduced in version 19.1.100.0)

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### HistoricalUnitCost

> Used for returning of goods that are sold before the exploitation of the system. [Currency: SalesOrder.DocumentCurrency] [Filter(eq;ge;le)]

_Type_: **[Amount](../data-types.md#Amount) (nullable)**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### IntrastatTransactionNatureCode

> Transaction nature; used for Intrastat reporting.

_Type_: **[Finance.Intrastat.TransactionNature](Crm.Sales.SalesOrderLines.md#IntrastatTransactionNatureCode) (nullable)**  
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
`obj.SalesOrder.IntrastatTransactionNatureCode`

_Front-End Recalc Expressions:_  
`obj.SalesOrder.IntrastatTransactionNatureCode`
### IntrastatTransportModeCode

> Transport mode; used for Intrastat reporting.

_Type_: **[Finance.Intrastat.TransportMode](Crm.Sales.SalesOrderLines.md#IntrastatTransportModeCode) (nullable)**  
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
`obj.SalesOrder.IntrastatTransportModeCode`

_Front-End Recalc Expressions:_  
`obj.SalesOrder.IntrastatTransportModeCode`
### LineAmount

> The total amount for the line. Equals to Quantity * Unit_Price, less the discounts. [Currency: SalesOrder.DocumentCurrency] [Required] [Default(0)]

_Type_: **[Amount](../data-types.md#Amount)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

_Back-End Default Expression:_  
`IIF((((obj.Quantity == null) OrElse (obj.UnitPrice == null)) OrElse ((obj.Quantity.Value == 0) AndAlso (obj.UnitPrice.Value == 0))), obj.LineAmount, (((obj.Quantity.Value * obj.UnitPrice) * (1 - obj.LineStandardDiscountPercent)) * (1 - obj.LineCustomDiscountPercent)).Round())`

_Front-End Recalc Expressions:_  
`IIF((((obj.Quantity == null) OrElse (obj.UnitPrice == null)) OrElse ((obj.Quantity.Value == 0) AndAlso (obj.UnitPrice.Value == 0))), obj.LineAmount, (((obj.Quantity.Value * obj.UnitPrice) * (1 - obj.LineStandardDiscountPercent)) * (1 - obj.LineCustomDiscountPercent)).Round())`
### LineCustomDiscountPercent

> User-defined discount for the line. [Required] [Default(0)] [Filter(ge;le)]

_Type_: **decimal**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### LineFromDate

> When selling a service valid only for a period, denotes the beginning of the period. null means that it is unknown or N/A. (Introduced in version 20.1.100.0)

_Type_: **date (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`obj.SalesOrder.FromDate`

_Front-End Recalc Expressions:_  
`obj.SalesOrder.FromDate`
### LineNo

> Consecutive number of the line within the sales order. [Required] [Filter(eq)] [ORD]

_Type_: **int32**  
_Supported Filters_: **Equals**  
_Supports Order By_: **True**  

_Back-End Default Expression:_  
`(obj.SalesOrder.Lines.Select(c => c.LineNo).DefaultIfEmpty(0).Max() + 10)`

_Front-End Recalc Expressions:_  
`(obj.SalesOrder.Lines.Select(c => c.LineNo).DefaultIfEmpty(0).Max() + 10)`
### LineStandardDiscountPercent

> Standard discount for the line. This is automatically computed according to discount conditions. [Required] [Default(0)] [ReadOnly]

_Type_: **decimal**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  

_Back-End Default Expression:_  
`obj.DetermineLineStandardDiscountPercent(obj.Product, obj.LineDiscount, obj.BonusProgram, obj.PromotionalPackage, obj.ReturnForSalesOrderLine)`

_Front-End Recalc Expressions:_  
`obj.DetermineLineStandardDiscountPercent(obj.Product, obj.LineDiscount, obj.BonusProgram, obj.PromotionalPackage, obj.ReturnForSalesOrderLine)`
### LineToDate

> When selling a service valid only for a period, denotes the end of the period. null means that it is unknown or N/A. (Introduced in version 20.1.100.0)

_Type_: **date (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`obj.SalesOrder.ToDate`

_Front-End Recalc Expressions:_  
`obj.SalesOrder.ToDate`
### Notes

> Notes for this SalesOrderLine.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ParentLineNo

> The number of the line within the parent document, which the current line executes. null when the current line does not execute parent line. [Filter(eq)]

_Type_: **int32 (nullable)**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

### PersistLot

> If checked specifies that the lot in the line cannot be changed in the sub-documents created by the current document. [Required] [Default(false)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

_Back-End Default Expression:_  
`((obj.Lot != null) AndAlso obj.SalesOrder.Customer.PersistSalesOrdersLots)`

_Front-End Recalc Expressions:_  
`((obj.Lot != null) AndAlso obj.SalesOrder.Customer.PersistSalesOrdersLots)`
### ProductDescription

> The name of the sold product at the time the sale was made. [Required] [Filter(like)]

_Type_: **[MultilanguageString](../data-types.md#MultilanguageString)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`obj.Product.Name`

_Front-End Recalc Expressions:_  
`obj.Product.Name`
### Quantity

> The quantity sold. [Unit: QuantityUnit] [Required] [Default(1)] [Filter(ge;le)]

_Type_: **[Quantity](../data-types.md#Quantity)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### QuantityBase

> The equivalent of Quantity in the base measurement category of the product. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required]

_Type_: **[Quantity](../data-types.md#Quantity)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`IIF((((obj.Quantity == null) OrElse (obj.QuantityUnit == null)) OrElse (obj.Product == null)), obj.QuantityBase, obj.Quantity.ConvertTo(obj.Product.BaseUnit, obj.Product))`

_Front-End Recalc Expressions:_  
`IIF((((obj.Quantity == null) OrElse (obj.QuantityUnit == null)) OrElse (obj.Product == null)), obj.QuantityBase, obj.Quantity.ConvertTo(obj.Product.BaseUnit, obj.Product))`
### RequestedQuantity

> Quantity requested by customer. [Unit: QuantityUnit]

_Type_: **[Quantity](../data-types.md#Quantity) (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### RequiredDeliveryDate

> The required (contracted) delivery date for the line. [Filter(ge;le)]

_Type_: **date (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`obj.SalesOrder.RequiredDeliveryDate`

_Front-End Recalc Expressions:_  
`obj.SalesOrder.RequiredDeliveryDate`
### StandardQuantityBase

> The theoretical quantity in base measurement unit according to the current measurement dimensions for the product. Used to measure the execution. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] [ReadOnly] (Introduced in version 18.2.100.0)

_Type_: **[Quantity](../data-types.md#Quantity)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`IIF((((obj.Quantity == null) OrElse (obj.QuantityUnit == null)) OrElse (obj.Product == null)), obj.StandardQuantityBase, obj.Quantity.ConvertTo(obj.Product.BaseUnit, obj.Product))`

_Front-End Recalc Expressions:_  
`IIF((((obj.Quantity == null) OrElse (obj.QuantityUnit == null)) OrElse (obj.Product == null)), obj.StandardQuantityBase, obj.Quantity.ConvertTo(obj.Product.BaseUnit, obj.Product))`
### StandardUnitPrice

> Standard unit price of the product during the creation of the sales order line. [Currency: SalesOrder.DocumentCurrency] [ReadOnly]

_Type_: **[Amount](../data-types.md#Amount) (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`obj.Product.GetStandardUnitPrice(obj.QuantityUnit, obj.SalesOrder.DocumentCurrency, obj.SalesOrder.CurrencyDirectory)`

_Front-End Recalc Expressions:_  
`obj.Product.GetStandardUnitPrice(obj.QuantityUnit, obj.SalesOrder.DocumentCurrency, obj.SalesOrder.CurrencyDirectory)`
### UnitPrice

> Unit price of the product in the currency of the sales order and in the unit of measure, as specified by QuantityUnitId. [Currency: SalesOrder.DocumentCurrency] [Required] [Default(0)]

_Type_: **[Amount](../data-types.md#Amount)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

_Back-End Default Expression:_  
`(CalculateUnitPriceFromLineAmount(obj.LineAmount, obj.Quantity, obj.LineStandardDiscountPercent, obj.LineCustomDiscountPercent) ?? obj.UnitPrice)`

_Front-End Recalc Expressions:_  
`obj.CalculateUnitPrice(obj.SalesOrder, obj.QuantityUnit, obj.Product, obj.ProductPrice)`

## Reference Details

### BonusProgram

> The bonus program, based on which the line was automatically added. null when the line was not added for bonus program. [Filter(multi eq)]

_Type_: **[Crm.Marketing.BonusPrograms](Crm.Marketing.BonusPrograms.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`IIF((obj.ReturnForSalesOrderLine != null), null, obj.BonusProgram)`
### IntrastatTransportCountry

> Country of origin of the transport company; used for Intrastat reporting. [Filter(multi eq)]

_Type_: **[General.Geography.Countries](General.Geography.Countries.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`obj.SalesOrder.IntrastatTransportCountry`

_Front-End Recalc Expressions:_  
`obj.SalesOrder.IntrastatTransportCountry`
### LineDealType

> Deal type to be passed to the invoice line. If deal type in entered then the invoice creates VAT entry for this deal type. [Filter(multi eq)]

_Type_: **[Finance.Vat.DealTypes](Finance.Vat.DealTypes.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`obj.SalesOrder.DealType`

_Front-End Recalc Expressions:_  
`obj.SalesOrder.DealType`
### LineDiscount

> The line discount type used to form the Line_Standard_Discount_Percent. [Filter(multi eq)]

_Type_: **[Crm.LineDiscounts](Crm.LineDiscounts.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`obj.DetermineLineDiscount(obj.SalesOrder.EnterpriseCompany, obj.SalesOrder.EnterpriseCompanyLocation, obj.RequiredDeliveryDate, obj.SalesOrder.Customer, obj.SalesOrder.ShipToCustomer, obj.SalesOrder.DistributionChannel, obj.SalesOrder.PriceList, obj.Product, obj.Quantity, obj.QuantityUnit, obj.ReturnForSalesOrderLine, obj.BonusProgram, obj.PromotionalPackage, obj.LineDiscount)`
### LineEndCustomerParty

> The end customer is the customer of the dealer. It is stored for information purposes only. The end customer may not have customer definition, just party. [Filter(multi eq)] (Introduced in version 20.1.100.0)

_Type_: **[General.Contacts.Parties](General.Contacts.Parties.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`obj.SalesOrder.EndCustomerParty`

_Front-End Recalc Expressions:_  
`obj.SalesOrder.EndCustomerParty`
### LineStore

> The store which should be used to issue the goods for the line. null means to use the store from the header. [Filter(multi eq;like)]

_Type_: **[Logistics.Inventory.Stores](Logistics.Inventory.Stores.md) (nullable)**  
_Supported Filters_: **Equals, Like, EqualsIn**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`obj.SalesOrder.Store`

_Front-End Recalc Expressions:_  
`obj.SalesOrder.Store`
### Lot

> Specifies the lot from which the goods should be issued. null means that the lot will be specified at a later stage (store order, etc.). [Filter(multi eq)]

_Type_: **[Logistics.Inventory.Lots](Logistics.Inventory.Lots.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### ParentDocument

> The document, which the current line executes. null when the current line does not execute another line. [Filter(multi eq)]

_Type_: **[General.Documents](General.Documents.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### ProductCode

> Used to set the Product_Id thru the coding systems. [Filter(multi eq)]

_Type_: **[General.Products.ProductCodes](General.Products.ProductCodes.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Product

> The product sold. [Required] [Filter(multi eq)]

_Type_: **[General.Products.Products](General.Products.Products.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`IIF(((obj.BonusProgram != null) AndAlso (Convert(obj.BonusProgram.BonusAction, Int32) == 0)), obj.BonusProgram.BonusProduct, obj.ProductCode.Product.IfNullThen(obj.Product))`

_Front-End Recalc Expressions:_  
`IIF(((obj.BonusProgram != null) AndAlso (Convert(obj.BonusProgram.BonusAction, Int32) == 0)), obj.BonusProgram.BonusProduct, obj.ProductCode.Product.IfNullThen(obj.Product))`
### ProductPrice

> Not null when the price has been selected from the list of valid standard prices. [Filter(multi eq)]

_Type_: **[Crm.ProductPrices](Crm.ProductPrices.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`IIF((((obj.BonusProgram != null) AndAlso (Convert(obj.BonusProgram.BonusAction, Int32) == 0)) OrElse (obj.ReturnForSalesOrderLine != null)), null, DetermineProductPrice(obj.Product, obj.Quantity, obj.QuantityUnit, obj.RequiredDeliveryDate, obj.SalesOrder.Customer, obj.SalesOrder.ShipToCustomer, obj.SalesOrder.EnterpriseCompany, obj.SalesOrder.EnterpriseCompanyLocation, obj.SalesOrder.DistributionChannel, obj.SalesOrder.PriceList, obj.ProductPrice))`
### ProductVariant

> If specified determines which product variant of the current product in this line is used. [Filter(multi eq)]

_Type_: **[General.ProductVariants](General.ProductVariants.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### PromotionalPackage

> The promotional package, based on which the line was added. null when the line was not added as part of a promotional package. [Filter(multi eq)] [ReadOnly]

_Type_: **[Crm.PromotionalPackages](Crm.PromotionalPackages.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`IIF((obj.ReturnForSalesOrderLine != null), null, obj.PromotionalPackage)`
### QuantityUnit

> The measurement unit of Quantity. [Required] [Filter(multi eq)]

_Type_: **[General.MeasurementUnits](General.MeasurementUnits.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`obj.ProductCode.CodingSystem.DefaultMeasurementUnit.IfNullThen(obj.Product.MeasurementUnit.IfNullThen(obj.QuantityUnit))`

_Front-End Recalc Expressions:_  
`obj.ProductCode.CodingSystem.DefaultMeasurementUnit.IfNullThen(obj.Product.MeasurementUnit.IfNullThen(obj.QuantityUnit))`
### ReturnForInvoiceLine

> When specified, indicates that the current line is a return for products, invoiced with the specified invoice line. [Filter(multi eq)]

_Type_: **[Crm.Invoicing.InvoiceLines](Crm.Invoicing.InvoiceLines.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### ReturnForSalesOrderLine

> When specified indicates that the goods sold in Return_For_Sales_Order_Line_Id are returned with the current line. [Filter(multi eq)]

_Type_: **[Crm.Sales.SalesOrderLines](Crm.Sales.SalesOrderLines.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### SalesOrder

> The [SalesOrder](Crm.Sales.SalesOrderLines.md#SalesOrder) to which this SalesOrderLine belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Crm.Sales.SalesOrders](Crm.Sales.SalesOrders.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### SerialNumber

> Which serial number to receive/issue. null means that serial number is unknown or not applicable. [Filter(multi eq)]

_Type_: **[Logistics.Inventory.SerialNumbers](Logistics.Inventory.SerialNumbers.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### StoreBin

> The bin from which the goods should be withdrawn. null means that the bin will be specified at a later stage (store order, etc.). [Filter(multi eq)]

_Type_: **[Logistics.Inventory.StoreBins](Logistics.Inventory.StoreBins.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Document

> The [SalesOrder](Crm.Sales.SalesOrderLines.md#SalesOrder) to which this SalesOrderLine belongs. [Required] [Filter(multi eq)]

_Type_: **[Crm.Sales.SalesOrders](Crm.Sales.SalesOrders.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Crm.Sales.SalesOrderLines erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Crm.Sales.SalesOrderLines erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Crm.Sales.SalesOrderLines erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_Sales_SalesOrderLines?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Crm_Sales_SalesOrderLines?$top=10>

