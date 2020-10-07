# Logistics.Procurement.PurchaseInvoiceLines

Contains detail lines for purchase invoice documents. Entity: Scm_Purchase_Invoice_Lines

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Logistics.Procurement.PurchaseInvoiceLines.md#Id) | guid |  
| [DeliveryTermsCode](Logistics.Procurement.PurchaseInvoiceLines.md#DeliveryTermsCode) | [Finance.Intrastat.DeliveryTerms](Logistics.Procurement.PurchaseInvoiceLines.md#DeliveryTermsCode) (nullable) | Mode of delivery, like CIF, FOB, etc. Used also in Intrastat reporting. 
| [IntrastatApplyDate](Logistics.Procurement.PurchaseInvoiceLines.md#IntrastatApplyDate) | datetime (nullable) | Specifies in which period for Intrastat declaration must be included the current operation. Used only when the invoice is issued in different period than the one, that the operation must be included. If not set the document date is used. 
| [IntrastatTransactionNatureCode](Logistics.Procurement.PurchaseInvoiceLines.md#IntrastatTransactionNatureCode) | [Finance.Intrastat.TransactionNature](Logistics.Procurement.PurchaseInvoiceLines.md#IntrastatTransactionNatureCode) (nullable) | Transaction nature; used for Intrastat reporting. 
| [IntrastatTransportModeCode](Logistics.Procurement.PurchaseInvoiceLines.md#IntrastatTransportModeCode) | [Finance.Intrastat.TransportMode](Logistics.Procurement.PurchaseInvoiceLines.md#IntrastatTransportModeCode) (nullable) | Transport mode; used for Intrastat reporting. 
| [LineAmount](Logistics.Procurement.PurchaseInvoiceLines.md#LineAmount) | [Amount](../data-types/Amount.md) | The total invoiced amount for this line in the document currency of the invoice. [Currency: PurchaseInvoice.DocumentCurrency] [Required] [Default(0)] 
| [LineNo](Logistics.Procurement.PurchaseInvoiceLines.md#LineNo) | int32 | Consecutive line number within the invoice. [Required] 
| [Notes](Logistics.Procurement.PurchaseInvoiceLines.md#Notes) | string (nullable) | Notes for this PurchaseInvoiceLine. 
| [ProductName](Logistics.Procurement.PurchaseInvoiceLines.md#ProductName) | [MultilanguageString](../data-types/MultilanguageString.md) | The name of the invoiced product, initially copied from the name in the product definition. The field can be edited by the user. [Required] 
| [Quantity](Logistics.Procurement.PurchaseInvoiceLines.md#Quantity) | [Quantity](../data-types/Quantity.md) | The invoiced quantity. [Unit: QuantityUnit] [Required] [Default(1)] 
| [QuantityBase](Logistics.Procurement.PurchaseInvoiceLines.md#QuantityBase) | [Quantity](../data-types/Quantity.md) | The equivalence of Quantity in the base measurement category of the product. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] 
| [StandardQuantityBase](Logistics.Procurement.PurchaseInvoiceLines.md#StandardQuantityBase) | [Quantity](../data-types/Quantity.md) | The theoretical quantity in base measurement unit according to the current measurement dimensions for the product. Used to measure the execution. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] [ReadOnly] (Introduced in version 18.2.100.0) 
| [UnitPrice](Logistics.Procurement.PurchaseInvoiceLines.md#UnitPrice) | [Amount](../data-types/Amount.md) | The unit price of the invoiced item in the document currency of the invoice. [Currency: PurchaseInvoice.DocumentCurrency] [Required] [Default(0)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [IntrastatDestinationRegion](Logistics.Procurement.PurchaseInvoiceLines.md#IntrastatDestinationRegion) | [General.Geography.AdministrativeRegions](General.Geography.AdministrativeRegions.md) (nullable) | Region, which is the final destination of the goods. Used for Intrastat reporting. [Filter(multi eq)] |
| [IntrastatTransportCountry](Logistics.Procurement.PurchaseInvoiceLines.md#IntrastatTransportCountry) | [General.Geography.Countries](General.Geography.Countries.md) (nullable) | Country of origin of the transport company; used for Intrastat reporting. [Filter(multi eq)] |
| [LineCostCenter](Logistics.Procurement.PurchaseInvoiceLines.md#LineCostCenter) | [Finance.Accounting.CostCenters](Finance.Accounting.CostCenters.md) (nullable) | Cost center for which the amount from this row will be accounted. [Filter(multi eq)] |
| [LineDealType](Logistics.Procurement.PurchaseInvoiceLines.md#LineDealType) | [Finance.Vat.DealTypes](Finance.Vat.DealTypes.md) (nullable) | Deal type for this line. If deal type in the line is different from deal type in the header another VAT entry is created. [Filter(multi eq)] |
| [OriginCountry](Logistics.Procurement.PurchaseInvoiceLines.md#OriginCountry) | [General.Geography.Countries](General.Geography.Countries.md) (nullable) | The country of origin of the invoiced product. Should be non-null only when this is different from the country of origin from the product definition. [Filter(multi eq)] |
| [Product](Logistics.Procurement.PurchaseInvoiceLines.md#Product) | [General.Products.Products](General.Products.Products.md) | The invoiced product. [Required] [Filter(multi eq)] |
| [PurchaseInvoice](Logistics.Procurement.PurchaseInvoiceLines.md#PurchaseInvoice) | [Logistics.Procurement.PurchaseInvoices](Logistics.Procurement.PurchaseInvoices.md) | The [PurchaseInvoice](Logistics.Procurement.PurchaseInvoiceLines.md#PurchaseInvoice) to which this PurchaseInvoiceLine belongs. [Required] [Filter(multi eq)] [Owner] |
| [QuantityUnit](Logistics.Procurement.PurchaseInvoiceLines.md#QuantityUnit) | [General.MeasurementUnits](General.MeasurementUnits.md) | The measurement unit of Quantity. [Required] [Filter(multi eq)] |
| [ReceivingOrderLine](Logistics.Procurement.PurchaseInvoiceLines.md#ReceivingOrderLine) | [Logistics.Procurement.ReceivingOrderLines](Logistics.Procurement.ReceivingOrderLines.md) (nullable) | The receiving order line, which is invoiced by the current line. null means that this line is not directly related to receiving order line. [Filter(multi eq)] |
| [SaleLineDealType](Logistics.Procurement.PurchaseInvoiceLines.md#SaleLineDealType) | [Finance.Vat.DealTypes](Finance.Vat.DealTypes.md) (nullable) | Sale deal type for this line. If sale deal type in the line is different from sale deal type in the header another Sales VAT entry is created. [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### DeliveryTermsCode

> Mode of delivery, like CIF, FOB, etc. Used also in Intrastat reporting.

_Type_: **[Finance.Intrastat.DeliveryTerms](Logistics.Procurement.PurchaseInvoiceLines.md#DeliveryTermsCode) (nullable)**  
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

### IntrastatApplyDate

> Specifies in which period for Intrastat declaration must be included the current operation. Used only when the invoice is issued in different period than the one, that the operation must be included. If not set the document date is used.

_Type_: **datetime (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### IntrastatTransactionNatureCode

> Transaction nature; used for Intrastat reporting.

_Type_: **[Finance.Intrastat.TransactionNature](Logistics.Procurement.PurchaseInvoiceLines.md#IntrastatTransactionNatureCode) (nullable)**  
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

### IntrastatTransportModeCode

> Transport mode; used for Intrastat reporting.

_Type_: **[Finance.Intrastat.TransportMode](Logistics.Procurement.PurchaseInvoiceLines.md#IntrastatTransportModeCode) (nullable)**  
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

### LineAmount

> The total invoiced amount for this line in the document currency of the invoice. [Currency: PurchaseInvoice.DocumentCurrency] [Required] [Default(0)]

_Type_: **[Amount](../data-types/Amount.md)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### LineNo

> Consecutive line number within the invoice. [Required]

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`(obj.PurchaseInvoice.Lines.Select(c => c.LineNo).DefaultIfEmpty(0).Max() + 10)`

_Front-End Recalc Expressions:_  
`(obj.PurchaseInvoice.Lines.Select(c => c.LineNo).DefaultIfEmpty(0).Max() + 10)`
### Notes

> Notes for this PurchaseInvoiceLine.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ProductName

> The name of the invoiced product, initially copied from the name in the product definition. The field can be edited by the user. [Required]

_Type_: **[MultilanguageString](../data-types/MultilanguageString.md)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`obj.Product.Name`

_Front-End Recalc Expressions:_  
`obj.Product.Name`
### Quantity

> The invoiced quantity. [Unit: QuantityUnit] [Required] [Default(1)]

_Type_: **[Quantity](../data-types/Quantity.md)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### QuantityBase

> The equivalence of Quantity in the base measurement category of the product. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required]

_Type_: **[Quantity](../data-types/Quantity.md)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`IIF((((obj.Quantity == null) OrElse (obj.QuantityUnit == null)) OrElse (obj.Product == null)), obj.QuantityBase, obj.Quantity.ConvertTo(obj.Product.BaseUnit, obj.Product))`

_Front-End Recalc Expressions:_  
`IIF((((obj.Quantity == null) OrElse (obj.QuantityUnit == null)) OrElse (obj.Product == null)), obj.QuantityBase, obj.Quantity.ConvertTo(obj.Product.BaseUnit, obj.Product))`
### StandardQuantityBase

> The theoretical quantity in base measurement unit according to the current measurement dimensions for the product. Used to measure the execution. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] [ReadOnly] (Introduced in version 18.2.100.0)

_Type_: **[Quantity](../data-types/Quantity.md)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`IIF((((obj.Quantity == null) OrElse (obj.QuantityUnit == null)) OrElse (obj.Product == null)), obj.StandardQuantityBase, obj.Quantity.ConvertTo(obj.Product.BaseUnit, obj.Product))`

_Front-End Recalc Expressions:_  
`IIF((((obj.Quantity == null) OrElse (obj.QuantityUnit == null)) OrElse (obj.Product == null)), obj.StandardQuantityBase, obj.Quantity.ConvertTo(obj.Product.BaseUnit, obj.Product))`
### UnitPrice

> The unit price of the invoiced item in the document currency of the invoice. [Currency: PurchaseInvoice.DocumentCurrency] [Required] [Default(0)]

_Type_: **[Amount](../data-types/Amount.md)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  


## Reference Details

### IntrastatDestinationRegion

> Region, which is the final destination of the goods. Used for Intrastat reporting. [Filter(multi eq)]

_Type_: **[General.Geography.AdministrativeRegions](General.Geography.AdministrativeRegions.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### IntrastatTransportCountry

> Country of origin of the transport company; used for Intrastat reporting. [Filter(multi eq)]

_Type_: **[General.Geography.Countries](General.Geography.Countries.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### LineCostCenter

> Cost center for which the amount from this row will be accounted. [Filter(multi eq)]

_Type_: **[Finance.Accounting.CostCenters](Finance.Accounting.CostCenters.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### LineDealType

> Deal type for this line. If deal type in the line is different from deal type in the header another VAT entry is created. [Filter(multi eq)]

_Type_: **[Finance.Vat.DealTypes](Finance.Vat.DealTypes.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### OriginCountry

> The country of origin of the invoiced product. Should be non-null only when this is different from the country of origin from the product definition. [Filter(multi eq)]

_Type_: **[General.Geography.Countries](General.Geography.Countries.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Product

> The invoiced product. [Required] [Filter(multi eq)]

_Type_: **[General.Products.Products](General.Products.Products.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### PurchaseInvoice

> The [PurchaseInvoice](Logistics.Procurement.PurchaseInvoiceLines.md#PurchaseInvoice) to which this PurchaseInvoiceLine belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Logistics.Procurement.PurchaseInvoices](Logistics.Procurement.PurchaseInvoices.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### QuantityUnit

> The measurement unit of Quantity. [Required] [Filter(multi eq)]

_Type_: **[General.MeasurementUnits](General.MeasurementUnits.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### ReceivingOrderLine

> The receiving order line, which is invoiced by the current line. null means that this line is not directly related to receiving order line. [Filter(multi eq)]

_Type_: **[Logistics.Procurement.ReceivingOrderLines](Logistics.Procurement.ReceivingOrderLines.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### SaleLineDealType

> Sale deal type for this line. If sale deal type in the line is different from sale deal type in the header another Sales VAT entry is created. [Filter(multi eq)]

_Type_: **[Finance.Vat.DealTypes](Finance.Vat.DealTypes.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Logistics.Procurement.PurchaseInvoiceLines erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Logistics.Procurement.PurchaseInvoiceLines erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Logistics.Procurement.PurchaseInvoiceLines erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_Procurement_PurchaseInvoiceLines?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_Procurement_PurchaseInvoiceLines?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Scm_Purchase_Invoice_Lines?$top=10>

