---
uid: Production.ShopFloor.OutputOrderLines
---
# Production.ShopFloor.OutputOrderLines Entity

Detail records of output orders. Entity: Prd_Output_Order_Lines

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [EndTime](Production.ShopFloor.OutputOrderLines.md#endtime) | datetime | Date and time when the operation has ended. [Required] [Default(Now)] [Filter(ge;le)] 
| [Finished](Production.ShopFloor.OutputOrderLines.md#finished) | boolean | True if this output entry completes the operation. false if there might be more entries. [Required] [Default(false)] [Filter(eq)] 
| [Id](Production.ShopFloor.OutputOrderLines.md#id) | guid |  
| [LineOrd](Production.ShopFloor.OutputOrderLines.md#lineord) | int32 | Line number within the order. [Required] 
| [Notes](Production.ShopFloor.OutputOrderLines.md#notes) | string (nullable) | Notes for this OutputOrderLine. 
| [ProducedQuantity](Production.ShopFloor.OutputOrderLines.md#producedquantity) | [Quantity](../data-types.md#quantity) | The processed quantity of the end product. [Unit: ProducedQuantityUnit] [Required] [Default(0)] [Filter(ge;le)] 
| [ProducedQuantityBase](Production.ShopFloor.OutputOrderLines.md#producedquantitybase) | [Quantity](../data-types.md#quantity) | The equivalence of Produced Quantity in the base measurement unit of the product. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] [Default(0)] [ReadOnly] 
| [ProducedStandard<br />QuantityBase](Production.ShopFloor.OutputOrderLines.md#producedstandardquantitybase) | [Quantity](../data-types.md#quantity) | The theoretical quantity in base measurement unit according to the current measurement dimensions for the product. Used to measure the execution. null means to convert the value from Quantity using the measurement ratios. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] [ReadOnly] [Introduced in version 18.2] 
| [StartTime](Production.ShopFloor.OutputOrderLines.md#starttime) | datetime | Date and time when the operation has began. [Required] [Default(Now)] [Filter(ge;le)] 
| [TransactionTimestamp](Production.ShopFloor.OutputOrderLines.md#transactiontimestamp) | datetime (nullable) | Sets the timestamp of the receipt store operations for this output order line. Used in completing output orders. [ReadOnly] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [LineWorkOrder](Production.ShopFloor.OutputOrderLines.md#lineworkorder) | [WorkOrders](Production.ShopFloor.WorkOrders.md) | The work order for which work is being accounted. [Required] [Filter(multi eq)] |
| [Lot](Production.ShopFloor.OutputOrderLines.md#lot) | [Lots](Logistics.Inventory.Lots.md) (nullable) | The lot of the produced product. [Filter(multi eq)] |
| [OutputOrder](Production.ShopFloor.OutputOrderLines.md#outputorder) | [OutputOrders](Production.ShopFloor.OutputOrders.md) | The [OutputOrder](Production.ShopFloor.OutputOrderLines.md#outputorder) to which this OutputOrderLine belongs. [Required] [Filter(multi eq)] [Owner] |
| [ProducedQuantityUnit](Production.ShopFloor.OutputOrderLines.md#producedquantityunit) | [MeasurementUnits](General.MeasurementUnits.md) | The measurement unit of Produced Quantity. [Required] [Filter(multi eq)] |
| [Product](Production.ShopFloor.OutputOrderLines.md#product) | [Products](General.Products.Products.md) | The actually produced product. [Required] [Filter(multi eq)] |
| [ProductCode](Production.ShopFloor.OutputOrderLines.md#productcode) | [ProductCodes](General.Products.ProductCodes.md) (nullable) | Selects the product thru some of the product codes. [Filter(multi eq)] |
| [SerialNumber](Production.ShopFloor.OutputOrderLines.md#serialnumber) | [SerialNumbers](Logistics.Inventory.SerialNumbers.md) (nullable) | If not null, specifies that the product was (has to be) stored with specific serial number. [Filter(multi eq)] |
| [Store](Production.ShopFloor.OutputOrderLines.md#store) | [Stores](Logistics.Inventory.Stores.md) (nullable) | Where to output the produced quantity. Can be null only if Produced_Quantity = 0. [Filter(multi eq)] |
| [StoreBin](Production.ShopFloor.OutputOrderLines.md#storebin) | [StoreBins](Logistics.Inventory.StoreBins.md) (nullable) | If not null, specifies that the product was (has to be) stored to specific store bin. [Filter(multi eq)] |
| [WorkDoneByParty](Production.ShopFloor.OutputOrderLines.md#workdonebyparty) | [Parties](General.Contacts.Parties.md) (nullable) | The party (usually employee worker) who has accomplished the work. null if unknown or N/A. [Filter(multi eq)] |
| [WorkgroupResource](Production.ShopFloor.OutputOrderLines.md#workgroupresource) | [WorkgroupResources](Production.Resources.WorkgroupResources.md) (nullable) | The resource, which was used to perform the operation. [Filter(multi eq)] |
| [WorkOrderItem](Production.ShopFloor.OutputOrderLines.md#workorderitem) | [WorkOrderItems](Production.ShopFloor.WorkOrderItems.md) | The work order item for which this output is recorded. [Required] [Filter(multi eq)] |
| [WorkOrderItemOperation](Production.ShopFloor.OutputOrderLines.md#workorderitemoperation) | [WorkOrderItemOperations](Production.ShopFloor.WorkOrderItemOperations.md) (nullable) | The operation for which this output is recorded. [Filter(multi eq)] |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| OutputOrderDistributed<br />MaterialConsumptions | [OutputOrderDistributedMaterialConsumptions](Production.ShopFloor.OutputOrderDistributedMaterialConsumptions.md) | List of [OutputOrderDistributed<br />MaterialConsumption](Production.ShopFloor.OutputOrderDistributed<br />MaterialConsumptions.md) child objects, based on the [Production.ShopFloor.OutputOrderDistributed<br />MaterialConsumption.OutputOrderLine](Production.ShopFloor.OutputOrderDistributed<br />MaterialConsumptions.md#outputorderline) back  


## Attribute Details

### EndTime

Date and time when the operation has ended. [Required] [Default(Now)] [Filter(ge;le)]

_Type_: **datetime**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **CurrentDateTime**  

### Finished

True if this output entry completes the operation. false if there might be more entries. [Required] [Default(false)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### LineOrd

Line number within the order. [Required]

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`( obj.OutputOrder.Lines.Select( c => c.LineOrd).DefaultIfEmpty( 0).Max( ) + 10)`

_Front-End Recalc Expressions:_  
`( obj.OutputOrder.Lines.Select( c => c.LineOrd).DefaultIfEmpty( 0).Max( ) + 10)`
### Notes

Notes for this OutputOrderLine.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ProducedQuantity

The processed quantity of the end product. [Unit: ProducedQuantityUnit] [Required] [Default(0)] [Filter(ge;le)]

_Type_: **[Quantity](../data-types.md#quantity)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### ProducedQuantityBase

The equivalence of Produced Quantity in the base measurement unit of the product. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] [Default(0)] [ReadOnly]

_Type_: **[Quantity](../data-types.md#quantity)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

_Back-End Default Expression:_  
`IIF( ( ( ( obj.ProducedQuantity == null) OrElse ( obj.ProducedQuantityUnit == null)) OrElse ( obj.Product == null)), obj.ProducedQuantityBase, obj.ProducedQuantity.ConvertTo( obj.Product.BaseUnit, obj.Product))`

_Front-End Recalc Expressions:_  
`IIF( ( ( ( obj.ProducedQuantity == null) OrElse ( obj.ProducedQuantityUnit == null)) OrElse ( obj.Product == null)), obj.ProducedQuantityBase, obj.ProducedQuantity.ConvertTo( obj.Product.BaseUnit, obj.Product))`
### ProducedStandardQuantityBase

The theoretical quantity in base measurement unit according to the current measurement dimensions for the product. Used to measure the execution. null means to convert the value from Quantity using the measurement ratios. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] [ReadOnly] [Introduced in version 18.2]

_Type_: **[Quantity](../data-types.md#quantity)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`IIF( ( ( ( obj.ProducedQuantity == null) OrElse ( obj.ProducedQuantityUnit == null)) OrElse ( obj.Product == null)), obj.ProducedStandardQuantityBase, obj.ProducedQuantity.ConvertTo( obj.Product.BaseUnit, obj.Product))`

_Front-End Recalc Expressions:_  
`IIF( ( ( ( obj.ProducedQuantity == null) OrElse ( obj.ProducedQuantityUnit == null)) OrElse ( obj.Product == null)), obj.ProducedStandardQuantityBase, obj.ProducedQuantity.ConvertTo( obj.Product.BaseUnit, obj.Product))`
### StartTime

Date and time when the operation has began. [Required] [Default(Now)] [Filter(ge;le)]

_Type_: **datetime**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **CurrentDateTime**  

### TransactionTimestamp

Sets the timestamp of the receipt store operations for this output order line. Used in completing output orders. [ReadOnly]

_Type_: **datetime (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### LineWorkOrder

The work order for which work is being accounted. [Required] [Filter(multi eq)]

_Type_: **[WorkOrders](Production.ShopFloor.WorkOrders.md)**  
_Supported Filters_: **Equals, EqualsIn**  

_Back-End Default Expression:_  
`obj.OutputOrder.WorkOrder`

_Front-End Recalc Expressions:_  
`obj.OutputOrder.WorkOrder`
### Lot

The lot of the produced product. [Filter(multi eq)]

_Type_: **[Lots](Logistics.Inventory.Lots.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### OutputOrder

The [OutputOrder](Production.ShopFloor.OutputOrderLines.md#outputorder) to which this OutputOrderLine belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[OutputOrders](Production.ShopFloor.OutputOrders.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### ProducedQuantityUnit

The measurement unit of Produced Quantity. [Required] [Filter(multi eq)]

_Type_: **[MeasurementUnits](General.MeasurementUnits.md)**  
_Supported Filters_: **Equals, EqualsIn**  

_Front-End Recalc Expressions:_  
`IIF( ( ( obj.ProductCode != null) AndAlso ( obj.ProductCode.CodingSystem.DefaultMeasurementUnit != null)), obj.ProductCode.CodingSystem.DefaultMeasurementUnit, obj.Product.MeasurementUnit)`
### Product

The actually produced product. [Required] [Filter(multi eq)]

_Type_: **[Products](General.Products.Products.md)**  
_Supported Filters_: **Equals, EqualsIn**  

_Front-End Recalc Expressions:_  
`obj.ProductCode.Product`
### ProductCode

Selects the product thru some of the product codes. [Filter(multi eq)]

_Type_: **[ProductCodes](General.Products.ProductCodes.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

_Front-End Recalc Expressions:_  
`IIF( ( obj.ProductCode.Product != obj.Product), null, obj.ProductCode)`
### SerialNumber

If not null, specifies that the product was (has to be) stored with specific serial number. [Filter(multi eq)]

_Type_: **[SerialNumbers](Logistics.Inventory.SerialNumbers.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### Store

Where to output the produced quantity. Can be null only if Produced_Quantity = 0. [Filter(multi eq)]

_Type_: **[Stores](Logistics.Inventory.Stores.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### StoreBin

If not null, specifies that the product was (has to be) stored to specific store bin. [Filter(multi eq)]

_Type_: **[StoreBins](Logistics.Inventory.StoreBins.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### WorkDoneByParty

The party (usually employee worker) who has accomplished the work. null if unknown or N/A. [Filter(multi eq)]

_Type_: **[Parties](General.Contacts.Parties.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### WorkgroupResource

The resource, which was used to perform the operation. [Filter(multi eq)]

_Type_: **[WorkgroupResources](Production.Resources.WorkgroupResources.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

_Front-End Recalc Expressions:_  
`obj.WorkOrderItemOperation.WorkgroupResource`
### WorkOrderItem

The work order item for which this output is recorded. [Required] [Filter(multi eq)]

_Type_: **[WorkOrderItems](Production.ShopFloor.WorkOrderItems.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### WorkOrderItemOperation

The operation for which this output is recorded. [Filter(multi eq)]

_Type_: **[WorkOrderItemOperations](Production.ShopFloor.WorkOrderItemOperations.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Production.ShopFloor.OutputOrderLines erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Production.ShopFloor.OutputOrderLines erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Production_ShopFloor_OutputOrderLines?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Production_ShopFloor_OutputOrderLines?$top=10>

