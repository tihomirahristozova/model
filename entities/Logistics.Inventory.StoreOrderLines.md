---
uid: Logistics.Inventory.StoreOrderLines
---
# Logistics.Inventory.StoreOrderLines

Detail lines of store orders. Each line represents one planned stock transaction line, but can be executed in parts. E.g. many transaction lines can be bound to one order line. Entity: Inv_Store_Order_Lines

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Logistics.Inventory.StoreOrderLines.md#Id) | guid |  
| [ForOrdering](Logistics.Inventory.StoreOrderLines.md#ForOrdering) | boolean | Specifies that the quantity of the product can be less than free to use quantity, because the product will be supplied . [Required] [Default(false)] 
| [GuaranteePeriodDays](Logistics.Inventory.StoreOrderLines.md#GuaranteePeriodDays) | int32 (nullable) | Guarantee period in days for the offered product. null for non-serviced products. 
| [LineCost](Logistics.Inventory.StoreOrderLines.md#LineCost) | [Amount](../data-types.md#Amount) (nullable) | Total cost for the line in the currency of the document. Equals Quantity * Unit_Cost. [Currency: StoreOrder.DocumentCurrency] 
| [LineNo](Logistics.Inventory.StoreOrderLines.md#LineNo) | int32 | Line number within the store order. [Required] [Filter(eq)] 
| [LotNumber](Logistics.Inventory.StoreOrderLines.md#LotNumber) | string (nullable) | Obsolete. Not used. 
| [Notes](Logistics.Inventory.StoreOrderLines.md#Notes) | string (nullable) | Notes for this StoreOrderLine. 
| [ParentLineId](Logistics.Inventory.StoreOrderLines.md#ParentLineId) | guid (nullable) | Id of the line of the parent document, which generated the store order. null for user-entered store orders or if not applicable. [Filter(multi eq)] 
| [ParentLineNo](Logistics.Inventory.StoreOrderLines.md#ParentLineNo) | int32 (nullable) | The number of the line within the parent document, which the current line executes. null when the current line does not execute parent line. [Filter(eq)] 
| [PersistLot](Logistics.Inventory.StoreOrderLines.md#PersistLot) | boolean | If checked specifies that the lot in the line cannot be changed in the sub-documents created by the current document. [Required] [Default(false)] [Filter(eq)] 
| [Quantity](Logistics.Inventory.StoreOrderLines.md#Quantity) | [Quantity](../data-types.md#Quantity) | Quantity ordered for receipt/issue. [Unit: QuantityUnit] [Required] [Default(0)] 
| [QuantityBase](Logistics.Inventory.StoreOrderLines.md#QuantityBase) | [Quantity](../data-types.md#Quantity) | Quantity in the base (default) measurement unit of the Item (calculated at the time of last update of the current store order line). Should be updated in parallel with each Quantity update. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] [Default(0)] [ReadOnly] 
| [StandardQuantityBase](Logistics.Inventory.StoreOrderLines.md#StandardQuantityBase) | [Quantity](../data-types.md#Quantity) | The theoretical quantity in base measurement unit according to the current measurement dimensions for the product. Used to measure the execution. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] [ReadOnly] (Introduced in version 18.2.100.0) 
| [TransactionTimestamp](Logistics.Inventory.StoreOrderLines.md#TransactionTimestamp) | datetime (nullable) | Exact time when the transaction for this store order line changes the cost of the product. [ReadOnly] 
| [UnitCost](Logistics.Inventory.StoreOrderLines.md#UnitCost) | [Amount](../data-types.md#Amount) (nullable) | Cost for 1 unit of measure in the currency of the document. [Currency: StoreOrder.DocumentCurrency] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Lot](Logistics.Inventory.StoreOrderLines.md#Lot) | [Logistics.Inventory.Lots](Logistics.Inventory.Lots.md) (nullable) | If non-null, contains the specific lot to use for the movement. [Filter(multi eq)] |
| [ParentDocument](Logistics.Inventory.StoreOrderLines.md#ParentDocument) | [General.Documents](General.Documents.md) (nullable) | The document, which the current line executes. null when the current line does not execute another line. [Filter(multi eq)] |
| [Product](Logistics.Inventory.StoreOrderLines.md#Product) | [General.Products.Products](General.Products.Products.md) | The product which should be received/issued. [Required] [Filter(multi eq)] |
| [ProductVariant](Logistics.Inventory.StoreOrderLines.md#ProductVariant) | [General.ProductVariants](General.ProductVariants.md) (nullable) | If specified determines which product variant of the current product in this line is used. [Filter(multi eq)] |
| [QuantityUnit](Logistics.Inventory.StoreOrderLines.md#QuantityUnit) | [General.MeasurementUnits](General.MeasurementUnits.md) | The measurement unit of Quantity. [Required] [Filter(multi eq)] |
| [SalesOrderLine](Logistics.Inventory.StoreOrderLines.md#SalesOrderLine) | [Crm.Sales.SalesOrderLines](Crm.Sales.SalesOrderLines.md) (nullable) | Sales order line which is managed by this store order line. When specified sales order line is used to make the margin analysis. [Filter(multi eq)] |
| [SerialNumber](Logistics.Inventory.StoreOrderLines.md#SerialNumber) | [Logistics.Inventory.SerialNumbers](Logistics.Inventory.SerialNumbers.md) (nullable) | Which serial number to receive/issue. null means that serial number is unknown or not applicable. [Filter(multi eq)] |
| [StoreBin](Logistics.Inventory.StoreOrderLines.md#StoreBin) | [Logistics.Inventory.StoreBins](Logistics.Inventory.StoreBins.md) (nullable) | From/to which store bin to issue/receive the products. null means that the store bin is unknown or not applicable. [Filter(multi eq)] |
| [StoreOrder](Logistics.Inventory.StoreOrderLines.md#StoreOrder) | [Logistics.Inventory.StoreOrders](Logistics.Inventory.StoreOrders.md) | The [StoreOrder](Logistics.Inventory.StoreOrderLines.md#StoreOrder) to which this StoreOrderLine belongs. [Required] [Filter(multi eq)] [Owner] |
| [Document](Logistics.Inventory.StoreOrderLines.md#Document) | [Logistics.Inventory.StoreOrders](Logistics.Inventory.StoreOrders.md) | The [StoreOrder](Logistics.Inventory.StoreOrderLines.md#StoreOrder) to which this StoreOrderLine belongs. [Required] [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### ForOrdering

> Specifies that the quantity of the product can be less than free to use quantity, because the product will be supplied . [Required] [Default(false)]

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### GuaranteePeriodDays

> Guarantee period in days for the offered product. null for non-serviced products.

_Type_: **int32 (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`IIF(obj.Product.ProductType.IsServiced, obj.Product.GuaranteePeriodDays, null)`
### LineCost

> Total cost for the line in the currency of the document. Equals Quantity * Unit_Cost. [Currency: StoreOrder.DocumentCurrency]

_Type_: **[Amount](../data-types.md#Amount) (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### LineNo

> Line number within the store order. [Required] [Filter(eq)]

_Type_: **int32**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`(obj.StoreOrder.Lines.Select(c => c.LineNo).DefaultIfEmpty(0).Max() + 10)`

_Front-End Recalc Expressions:_  
`(obj.StoreOrder.Lines.Select(c => c.LineNo).DefaultIfEmpty(0).Max() + 10)`
### LotNumber

> Obsolete. Not used.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Notes

> Notes for this StoreOrderLine.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ParentLineId

> Id of the line of the parent document, which generated the store order. null for user-entered store orders or if not applicable. [Filter(multi eq)]

_Type_: **guid (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
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

### Quantity

> Quantity ordered for receipt/issue. [Unit: QuantityUnit] [Required] [Default(0)]

_Type_: **[Quantity](../data-types.md#Quantity)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### QuantityBase

> Quantity in the base (default) measurement unit of the Item (calculated at the time of last update of the current store order line). Should be updated in parallel with each Quantity update. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] [Default(0)] [ReadOnly]

_Type_: **[Quantity](../data-types.md#Quantity)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

_Back-End Default Expression:_  
`IIF((((obj.Quantity == null) OrElse (obj.QuantityUnit == null)) OrElse (obj.Product == null)), obj.QuantityBase, obj.Quantity.ConvertTo(obj.Product.BaseUnit, obj.Product))`

_Front-End Recalc Expressions:_  
`IIF((((obj.Quantity == null) OrElse (obj.QuantityUnit == null)) OrElse (obj.Product == null)), obj.QuantityBase, obj.Quantity.ConvertTo(obj.Product.BaseUnit, obj.Product))`
### StandardQuantityBase

> The theoretical quantity in base measurement unit according to the current measurement dimensions for the product. Used to measure the execution. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] [ReadOnly] (Introduced in version 18.2.100.0)

_Type_: **[Quantity](../data-types.md#Quantity)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`IIF((((obj.Quantity == null) OrElse (obj.QuantityUnit == null)) OrElse (obj.Product == null)), obj.StandardQuantityBase, obj.Quantity.ConvertTo(obj.Product.BaseUnit, obj.Product))`

_Front-End Recalc Expressions:_  
`IIF((((obj.Quantity == null) OrElse (obj.QuantityUnit == null)) OrElse (obj.Product == null)), obj.StandardQuantityBase, obj.Quantity.ConvertTo(obj.Product.BaseUnit, obj.Product))`
### TransactionTimestamp

> Exact time when the transaction for this store order line changes the cost of the product. [ReadOnly]

_Type_: **datetime (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### UnitCost

> Cost for 1 unit of measure in the currency of the document. [Currency: StoreOrder.DocumentCurrency]

_Type_: **[Amount](../data-types.md#Amount) (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### Lot

> If non-null, contains the specific lot to use for the movement. [Filter(multi eq)]

_Type_: **[Logistics.Inventory.Lots](Logistics.Inventory.Lots.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### ParentDocument

> The document, which the current line executes. null when the current line does not execute another line. [Filter(multi eq)]

_Type_: **[General.Documents](General.Documents.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Product

> The product which should be received/issued. [Required] [Filter(multi eq)]

_Type_: **[General.Products.Products](General.Products.Products.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### ProductVariant

> If specified determines which product variant of the current product in this line is used. [Filter(multi eq)]

_Type_: **[General.ProductVariants](General.ProductVariants.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### QuantityUnit

> The measurement unit of Quantity. [Required] [Filter(multi eq)]

_Type_: **[General.MeasurementUnits](General.MeasurementUnits.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`obj.Product.MeasurementUnit`
### SalesOrderLine

> Sales order line which is managed by this store order line. When specified sales order line is used to make the margin analysis. [Filter(multi eq)]

_Type_: **[Crm.Sales.SalesOrderLines](Crm.Sales.SalesOrderLines.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### SerialNumber

> Which serial number to receive/issue. null means that serial number is unknown or not applicable. [Filter(multi eq)]

_Type_: **[Logistics.Inventory.SerialNumbers](Logistics.Inventory.SerialNumbers.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### StoreBin

> From/to which store bin to issue/receive the products. null means that the store bin is unknown or not applicable. [Filter(multi eq)]

_Type_: **[Logistics.Inventory.StoreBins](Logistics.Inventory.StoreBins.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### StoreOrder

> The [StoreOrder](Logistics.Inventory.StoreOrderLines.md#StoreOrder) to which this StoreOrderLine belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Logistics.Inventory.StoreOrders](Logistics.Inventory.StoreOrders.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Document

> The [StoreOrder](Logistics.Inventory.StoreOrderLines.md#StoreOrder) to which this StoreOrderLine belongs. [Required] [Filter(multi eq)]

_Type_: **[Logistics.Inventory.StoreOrders](Logistics.Inventory.StoreOrders.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Logistics.Inventory.StoreOrderLines erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Logistics.Inventory.StoreOrderLines erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Logistics.Inventory.StoreOrderLines erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_Inventory_StoreOrderLines?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_Inventory_StoreOrderLines?$top=10>

