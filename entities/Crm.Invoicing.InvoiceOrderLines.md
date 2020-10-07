# Crm.Invoicing.InvoiceOrderLines

Detail records (lines) of Invoice Orders. Entity: Crm_Invoice_Order_Lines

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Crm.Invoicing.InvoiceOrderLines.md#Id) | guid |  
| [BusinessReason](Crm.Invoicing.InvoiceOrderLines.md#BusinessReason) | [Crm.Invoicing.InvoicingBusinessReason](Crm.Invoicing.InvoiceOrderLines.md#BusinessReason) | Business reason for invoicing of this product or service. S=Shipment, P=Payment. [Required] [Default("S")] 
| [LineAmount](Crm.Invoicing.InvoiceOrderLines.md#LineAmount) | [Amount](../data-types/Amount.md) | Amount for the line in the currency of the parent document. Usually equals Quantity * Unit_Price. When Quantity = 0, Unit Price is undefined and this contains the total line amount. [Currency: InvoiceOrder.DocumentCurrency] [Required] [Default(0)] 
| [LineCustomDiscountPercent](Crm.Invoicing.InvoiceOrderLines.md#LineCustomDiscountPercent) | decimal | User-defined discount for the line. [Required] [Default(0)] 
| [LineNo](Crm.Invoicing.InvoiceOrderLines.md#LineNo) | int32 | Line number, unique within the InvoiceOrder. Usually is increasing number like 10, 20, 30, ... when initially entering the InvoiceOrder (in order to allow insertions with adjustment documents). [Required] 
| [LineStandardDiscountPercent](Crm.Invoicing.InvoiceOrderLines.md#LineStandardDiscountPercent) | decimal | Standard discount for the line. This is automatically computed according to discount conditions. [Required] [Default(0)] 
| [ProductDescription](Crm.Invoicing.InvoiceOrderLines.md#ProductDescription) | [MultilanguageString](../data-types/MultilanguageString.md) | The description of Product. Initially copied from the name of the Product or from the generating document. [Required] 
| [Quantity](Crm.Invoicing.InvoiceOrderLines.md#Quantity) | [Quantity](../data-types/Quantity.md) | The quantity of the product to invoice. [Unit: QuantityUnit] [Required] [Default(1)] [Filter(ge;le)] 
| [QuantityBase](Crm.Invoicing.InvoiceOrderLines.md#QuantityBase) | [Quantity](../data-types/Quantity.md) | The equivalent of Quantity in the base measurement unit of the Product. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] 
| [StandardQuantityBase](Crm.Invoicing.InvoiceOrderLines.md#StandardQuantityBase) | [Quantity](../data-types/Quantity.md) | The theoretical quantity in base measurement unit according to the current measurement dimensions for the product. Used to measure the execution. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] [ReadOnly] (Introduced in version 18.2.100.0) 
| [UnitPrice](Crm.Invoicing.InvoiceOrderLines.md#UnitPrice) | [Amount](../data-types/Amount.md) | Unit selling price in the unit of measure, specified in Quantity Unit. [Currency: InvoiceOrder.DocumentCurrency] [Required] [Default(0)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [InvoiceOrder](Crm.Invoicing.InvoiceOrderLines.md#InvoiceOrder) | [Crm.Invoicing.InvoiceOrders](Crm.Invoicing.InvoiceOrders.md) | The [InvoiceOrder](Crm.Invoicing.InvoiceOrderLines.md#InvoiceOrder) to which this InvoiceOrderLine belongs. [Required] [Filter(multi eq)] [Owner] |
| [LineDealType](Crm.Invoicing.InvoiceOrderLines.md#LineDealType) | [Finance.Vat.DealTypes](Finance.Vat.DealTypes.md) (nullable) | Deal type to be passed to the invoice line. If deal type in the line is different from deal type in the header another VAT entry is created from the invoice. [Filter(multi eq)] |
| [LineDiscount](Crm.Invoicing.InvoiceOrderLines.md#LineDiscount) | [Crm.LineDiscounts](Crm.LineDiscounts.md) (nullable) | The line discount type used to form the Line_Standard_Discount_Percent. [Filter(multi eq)] |
| [PaymentTransaction](Crm.Invoicing.InvoiceOrderLines.md#PaymentTransaction) | [Finance.Payments.PaymentTransactions](Finance.Payments.PaymentTransactions.md) (nullable) | The payment transaction, which is to be invoiced by this line, when Business Reason = P. Used to reconcile the invoice with the payments in the case of advance payment. [Filter(multi eq)] |
| [Product](Crm.Invoicing.InvoiceOrderLines.md#Product) | [General.Products.Products](General.Products.Products.md) (nullable) | The product, which is ordered for invoicing. [Filter(multi eq)] |
| [QuantityUnit](Crm.Invoicing.InvoiceOrderLines.md#QuantityUnit) | [General.MeasurementUnits](General.MeasurementUnits.md) | The measurement unit of Quantity. [Required] [Filter(multi eq)] |
| [SalesOrder](Crm.Invoicing.InvoiceOrderLines.md#SalesOrder) | [Crm.Sales.SalesOrders](Crm.Sales.SalesOrders.md) (nullable) | When not null specifies the Sales Order that is ordered to be invoiced by this line. [Filter(multi eq)] |
| [SalesOrderLine](Crm.Invoicing.InvoiceOrderLines.md#SalesOrderLine) | [Crm.Sales.SalesOrderLines](Crm.Sales.SalesOrderLines.md) (nullable) | When not null specifies the Sales Order line that is ordered to be invoiced by this line. [Filter(multi eq)] |
| [SerialNumber](Crm.Invoicing.InvoiceOrderLines.md#SerialNumber) | [Logistics.Inventory.SerialNumbers](Logistics.Inventory.SerialNumbers.md) (nullable) | Which serial number to receive/issue. null means that serial number is unknown or not applicable. [Filter(multi eq)] |
| [TransactionLine](Crm.Invoicing.InvoiceOrderLines.md#TransactionLine) | [Logistics.Inventory.StoreTransactionLines](Logistics.Inventory.StoreTransactionLines.md) (nullable) | The store transaction line that is to be invoiced by this line, for Business Reason = S. [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### BusinessReason

> Business reason for invoicing of this product or service. S=Shipment, P=Payment. [Required] [Default("S")]

_Type_: **[Crm.Invoicing.InvoicingBusinessReason](Crm.Invoicing.InvoiceOrderLines.md#BusinessReason)**  
Generic enum type for InvoicingBusinessReason properties  
_Allowed Values (Enum Members)_  

| Value | Description |
| ---- | --- |
| Payment | Payment value. Stored as 'P'. <br /> _Database Value:_ 'P' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Payment' |
| Shipment | Shipment value. Stored as 'S'. <br /> _Database Value:_ 'S' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'Shipment' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Shipment**  

### LineAmount

> Amount for the line in the currency of the parent document. Usually equals Quantity * Unit_Price. When Quantity = 0, Unit Price is undefined and this contains the total line amount. [Currency: InvoiceOrder.DocumentCurrency] [Required] [Default(0)]

_Type_: **[Amount](../data-types/Amount.md)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

_Front-End Recalc Expressions:_  
`obj.CalculateLineAmount(obj.Quantity, obj.UnitPrice, Convert(obj.LineCustomDiscountPercent, Nullable`1), Convert(obj.LineStandardDiscountPercent, Nullable`1), obj.InvoiceOrder.DocumentCurrency)`
### LineCustomDiscountPercent

> User-defined discount for the line. [Required] [Default(0)]

_Type_: **decimal**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### LineNo

> Line number, unique within the InvoiceOrder. Usually is increasing number like 10, 20, 30, ... when initially entering the InvoiceOrder (in order to allow insertions with adjustment documents). [Required]

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`(obj.InvoiceOrder.Lines.Select(c => c.LineNo).DefaultIfEmpty(0).Max() + 10)`

_Front-End Recalc Expressions:_  
`(obj.InvoiceOrder.Lines.Select(c => c.LineNo).DefaultIfEmpty(0).Max() + 10)`
### LineStandardDiscountPercent

> Standard discount for the line. This is automatically computed according to discount conditions. [Required] [Default(0)]

_Type_: **decimal**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  

_Front-End Recalc Expressions:_  
`IIF((obj.LineDiscount != null), obj.LineDiscount.DiscountPercent, 0)`
### ProductDescription

> The description of Product. Initially copied from the name of the Product or from the generating document. [Required]

_Type_: **[MultilanguageString](../data-types/MultilanguageString.md)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`obj.Product.Name`
### Quantity

> The quantity of the product to invoice. [Unit: QuantityUnit] [Required] [Default(1)] [Filter(ge;le)]

_Type_: **[Quantity](../data-types/Quantity.md)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### QuantityBase

> The equivalent of Quantity in the base measurement unit of the Product. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required]

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

> Unit selling price in the unit of measure, specified in Quantity Unit. [Currency: InvoiceOrder.DocumentCurrency] [Required] [Default(0)]

_Type_: **[Amount](../data-types/Amount.md)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

_Front-End Recalc Expressions:_  
`obj.CalculateUnitPrice(obj.InvoiceOrder, obj.Product)`

## Reference Details

### InvoiceOrder

> The [InvoiceOrder](Crm.Invoicing.InvoiceOrderLines.md#InvoiceOrder) to which this InvoiceOrderLine belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Crm.Invoicing.InvoiceOrders](Crm.Invoicing.InvoiceOrders.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### LineDealType

> Deal type to be passed to the invoice line. If deal type in the line is different from deal type in the header another VAT entry is created from the invoice. [Filter(multi eq)]

_Type_: **[Finance.Vat.DealTypes](Finance.Vat.DealTypes.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`obj.InvoiceOrder.DealType`

_Front-End Recalc Expressions:_  
`obj.InvoiceOrder.DealType`
### LineDiscount

> The line discount type used to form the Line_Standard_Discount_Percent. [Filter(multi eq)]

_Type_: **[Crm.LineDiscounts](Crm.LineDiscounts.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`obj.DetermineLineDiscount(Convert((obj.InvoiceOrder.DeliveryDate ?? obj.InvoiceOrder.DocumentDate), Nullable`1), obj.InvoiceOrder.Customer, obj.Product, obj.Quantity, obj.InvoiceOrder.EnterpriseCompany, obj.InvoiceOrder.EnterpriseCompanyLocation, IIF((obj.SalesOrder == null), null, obj.SalesOrder.DistributionChannel), IIF((obj.SalesOrder == null), null, obj.SalesOrder.PriceList))`
### PaymentTransaction

> The payment transaction, which is to be invoiced by this line, when Business Reason = P. Used to reconcile the invoice with the payments in the case of advance payment. [Filter(multi eq)]

_Type_: **[Finance.Payments.PaymentTransactions](Finance.Payments.PaymentTransactions.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Product

> The product, which is ordered for invoicing. [Filter(multi eq)]

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

> When not null specifies the Sales Order that is ordered to be invoiced by this line. [Filter(multi eq)]

_Type_: **[Crm.Sales.SalesOrders](Crm.Sales.SalesOrders.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`obj.InvoiceOrder.SalesOrder`

_Front-End Recalc Expressions:_  
`obj.InvoiceOrder.SalesOrder`
### SalesOrderLine

> When not null specifies the Sales Order line that is ordered to be invoiced by this line. [Filter(multi eq)]

_Type_: **[Crm.Sales.SalesOrderLines](Crm.Sales.SalesOrderLines.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### SerialNumber

> Which serial number to receive/issue. null means that serial number is unknown or not applicable. [Filter(multi eq)]

_Type_: **[Logistics.Inventory.SerialNumbers](Logistics.Inventory.SerialNumbers.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### TransactionLine

> The store transaction line that is to be invoiced by this line, for Business Reason = S. [Filter(multi eq)]

_Type_: **[Logistics.Inventory.StoreTransactionLines](Logistics.Inventory.StoreTransactionLines.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Crm.Invoicing.InvoiceOrderLines erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Crm.Invoicing.InvoiceOrderLines erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Crm.Invoicing.InvoiceOrderLines erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_Invoicing_InvoiceOrderLines?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Crm_Invoicing_InvoiceOrderLines?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_Invoice_Order_Lines?$top=10>

