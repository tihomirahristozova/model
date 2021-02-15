---
uid: Production.ShopFloor.WorkOrderItems
---
# Production.ShopFloor.WorkOrderItems Entity

The different items that are produced with a work order. Entity: Prd_Work_Order_Items

Default Display Text Format:  
_{WorkOrder.DocumentType.Code}:{WorkOrder.DocumentNo}:{LineOrd} - {WorkOrder.DocumentType.TypeName:T}_  
Default Search Member:  
_WorkOrder.DocumentNo_  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [CompletionDate](Production.ShopFloor.WorkOrderItems.md#completiondate) | datetime (nullable) | The date, when the item should be completed. null means that there is no constraint for completion date. 
| [Id](Production.ShopFloor.WorkOrderItems.md#id) | guid |  
| [LineOrd](Production.ShopFloor.WorkOrderItems.md#lineord) | int32 | The order of the line within the work order. [Required] [Filter(eq;like)] 
| [LotSize](Production.ShopFloor.WorkOrderItems.md#lotsize) | [Quantity](../data-types.md#quantity) | Quantity produced in one production run. [Unit: ProducedQuantityUnit] [Required] [Default(1)] 
| [Notes](Production.ShopFloor.WorkOrderItems.md#notes) | string (nullable) | Notes for this WorkOrderItem. 
| [ParentLineId](Production.ShopFloor.WorkOrderItems.md#parentlineid) | guid (nullable) | If not null contains the Id of the line of the parent document, that created the current row. [Filter(multi eq)] 
| [ParentLineNo](Production.ShopFloor.WorkOrderItems.md#parentlineno) | int32 (nullable) | The number of the line within the parent document, which the current line executes. null when the current line does not execute another line. [Filter(eq)] 
| [Priority](Production.ShopFloor.WorkOrderItems.md#priority) | [Priority](Production.ShopFloor.WorkOrderItems.md#priority) | Priority of the production of the item. Initially inherits the priority of the work order. 1=Lowest ... 5=Highest. [Required] [Default(3)] 
| [ProducedQuantity](Production.ShopFloor.WorkOrderItems.md#producedquantity) | [Quantity](../data-types.md#quantity) | The quantity produced in the operation. [Unit: ProducedQuantityUnit] [Required] [Default(1)] 
| [ProducedQuantityBase](Production.ShopFloor.WorkOrderItems.md#producedquantitybase) | [Quantity](../data-types.md#quantity) | The equivalence of Produced Quantity in the base measurement category of the product. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] [ReadOnly] 
| [ProducedStandard<br />QuantityBase](Production.ShopFloor.WorkOrderItems.md#producedstandardquantitybase) | [Quantity](../data-types.md#quantity) | The theoretical quantity in base measurement unit according to the current measurement dimensions of the product. Used to measure the execution. null means to take the value from Produced Quantity Base. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] [ReadOnly] [Introduced in version 18.2] 
| [ReleaseDate](Production.ShopFloor.WorkOrderItems.md#releasedate) | datetime (nullable) | The date, when the item is released to production. null means that still there is no plan when the item will be released to production. 
| [ScheduledEndDateTime](Production.ShopFloor.WorkOrderItems.md#scheduledenddatetime) | datetime (nullable) | Date and time when the production of this item is scheduled to end. 
| [ScheduledStartDateTime](Production.ShopFloor.WorkOrderItems.md#scheduledstartdatetime) | datetime (nullable) | Date and time when the production of this item is scheduled to begin. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Document](Production.ShopFloor.WorkOrderItems.md#document) | [WorkOrders](Production.ShopFloor.WorkOrders.md) | The Id of the work order, containing the item. [Required] [Filter(multi eq)] |
| [Lot](Production.ShopFloor.WorkOrderItems.md#lot) | [Lots](Logistics.Inventory.Lots.md) (nullable) | The lot of the produced product. [Filter(multi eq)] |
| [OutputStore](Production.ShopFloor.WorkOrderItems.md#outputstore) | [Stores](Logistics.Inventory.Stores.md) (nullable) | Output store for the production. [Filter(multi eq)] |
| [ParentDocument](Production.ShopFloor.WorkOrderItems.md#parentdocument) | [Documents](General.Documents.md) (nullable) | The document, which the current line executes. null when the current line does not execute another line. [Filter(multi eq)] |
| [ProducedQuantityUnit](Production.ShopFloor.WorkOrderItems.md#producedquantityunit) | [MeasurementUnits](General.MeasurementUnits.md) | The measurement unit of the quantity produced in the operation. [Required] [Filter(multi eq)] |
| [Product](Production.ShopFloor.WorkOrderItems.md#product) | [Products](General.Products.Products.md) | The Id of the produced product. [Required] [Filter(multi eq)] |
| [ProductCode](Production.ShopFloor.WorkOrderItems.md#productcode) | [ProductCodes](General.Products.ProductCodes.md) (nullable) | Selects the product thru some of the product codes. [Filter(multi eq)] |
| [Recipe](Production.ShopFloor.WorkOrderItems.md#recipe) | [Recipes](Production.Technologies.Recipes.md) (nullable) | The base recipe. null means that the item is produced without recipe. [Filter(multi eq)] |
| [SerialNumber](Production.ShopFloor.WorkOrderItems.md#serialnumber) | [SerialNumbers](Logistics.Inventory.SerialNumbers.md) (nullable) | If not null, specifies that the product was (has to be) produced with specific serial number. [Filter(multi eq)] |
| [StoreBin](Production.ShopFloor.WorkOrderItems.md#storebin) | [StoreBins](Logistics.Inventory.StoreBins.md) (nullable) | The store bin in which to store the products. [Filter(multi eq)] |
| [WorkOrder](Production.ShopFloor.WorkOrderItems.md#workorder) | [WorkOrders](Production.ShopFloor.WorkOrders.md) | The Id of the work order, containing the item. [Required] [Filter(multi eq)] [Owner] |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Operations | [WorkOrderItemOperations](Production.ShopFloor.WorkOrderItemOperations.md) | List of [WorkOrderItemOperation](Production.ShopFloor.WorkOrderItemOperations.md) child objects, based on the [Production.ShopFloor.WorkOrderItemOperation.WorkOrderItem](Production.ShopFloor.WorkOrderItemOperations.md#workorderitem) back reference 


## Attribute Details

### CompletionDate

The date, when the item should be completed. null means that there is no constraint for completion date.

_Type_: **datetime (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`obj.WorkOrder.CompletionDate`

_Front-End Recalc Expressions:_  
`obj.WorkOrder.CompletionDate`
### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### LineOrd

The order of the line within the work order. [Required] [Filter(eq;like)]

_Type_: **int32**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`( obj.WorkOrder.Items.Select( c => c.LineOrd).DefaultIfEmpty( 0).Max( ) + 10)`

_Front-End Recalc Expressions:_  
`( obj.WorkOrder.Items.Select( c => c.LineOrd).DefaultIfEmpty( 0).Max( ) + 10)`
### LotSize

Quantity produced in one production run. [Unit: ProducedQuantityUnit] [Required] [Default(1)]

_Type_: **[Quantity](../data-types.md#quantity)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

_Front-End Recalc Expressions:_  
`IIF( ( ( obj.Recipe != null) AndAlso ( obj.ProducedQuantityUnit != null)), obj.Recipe.ProduceQuantity, obj.ProducedQuantity)`
### Notes

Notes for this WorkOrderItem.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ParentLineId

If not null contains the Id of the line of the parent document, that created the current row. [Filter(multi eq)]

_Type_: **guid (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### ParentLineNo

The number of the line within the parent document, which the current line executes. null when the current line does not execute another line. [Filter(eq)]

_Type_: **int32 (nullable)**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

### Priority

Priority of the production of the item. Initially inherits the priority of the work order. 1=Lowest ... 5=Highest. [Required] [Default(3)]

_Type_: **[Priority](Production.ShopFloor.WorkOrderItems.md#priority)**  
Allowed values for the [Priority](Production.ShopFloor.WorkOrderItems.md#priority) data attribute  
_Allowed Values (Production.ShopFloor.WorkOrderItemsRepository.Priority Enum Members)_  

| Value | Description |
| ---- | --- |
| Lowest | Lowest value. Stored as 1. <br /> _Database Value:_ 1 <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'Lowest' |
| Two | Two value. Stored as 2. <br /> _Database Value:_ 2 <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'Two' |
| Three | Three value. Stored as 3. <br /> _Database Value:_ 3 <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'Three' |
| Four | Four value. Stored as 4. <br /> _Database Value:_ 4 <br /> _Model Value:_ 4 <br /> _Domain API Value:_ 'Four' |
| Highest | Highest value. Stored as 5. <br /> _Database Value:_ 5 <br /> _Model Value:_ 5 <br /> _Domain API Value:_ 'Highest' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **3**  

### ProducedQuantity

The quantity produced in the operation. [Unit: ProducedQuantityUnit] [Required] [Default(1)]

_Type_: **[Quantity](../data-types.md#quantity)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

_Front-End Recalc Expressions:_  
`IIF( ( ( obj.Recipe != null) AndAlso ( obj.ProducedQuantityUnit != null)), obj.Recipe.ProduceQuantity, obj.ProducedQuantity)`
### ProducedQuantityBase

The equivalence of Produced Quantity in the base measurement category of the product. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] [ReadOnly]

_Type_: **[Quantity](../data-types.md#quantity)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`IIF( ( ( ( obj.ProducedQuantity != null) AndAlso ( obj.ProducedQuantityUnit != null)) AndAlso ( obj.Product != null)), obj.ProducedQuantity.ConvertTo( obj.Product.BaseUnit, obj.Product), obj.ProducedQuantityBase)`

_Front-End Recalc Expressions:_  
`IIF( ( ( ( obj.ProducedQuantity != null) AndAlso ( obj.ProducedQuantityUnit != null)) AndAlso ( obj.Product != null)), obj.ProducedQuantity.ConvertTo( obj.Product.BaseUnit, obj.Product), obj.ProducedQuantityBase)`
### ProducedStandardQuantityBase

The theoretical quantity in base measurement unit according to the current measurement dimensions of the product. Used to measure the execution. null means to take the value from Produced Quantity Base. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] [ReadOnly] [Introduced in version 18.2]

_Type_: **[Quantity](../data-types.md#quantity)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`IIF( ( ( ( obj.ProducedQuantity != null) AndAlso ( obj.ProducedQuantityUnit != null)) AndAlso ( obj.Product != null)), IIF( obj.Product.AllowVariableMeasurementRatios, obj.ProducedQuantity.ConvertTo( obj.Product.BaseUnit, obj.Product), obj.ProducedQuantityBase), obj.ProducedStandardQuantityBase)`

_Front-End Recalc Expressions:_  
`IIF( ( ( ( obj.ProducedQuantity != null) AndAlso ( obj.ProducedQuantityUnit != null)) AndAlso ( obj.Product != null)), obj.ProducedQuantity.ConvertTo( obj.Product.BaseUnit, obj.Product), obj.ProducedStandardQuantityBase)`
### ReleaseDate

The date, when the item is released to production. null means that still there is no plan when the item will be released to production.

_Type_: **datetime (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`obj.WorkOrder.ReleaseDate`

_Front-End Recalc Expressions:_  
`obj.WorkOrder.ReleaseDate`
### ScheduledEndDateTime

Date and time when the production of this item is scheduled to end.

_Type_: **datetime (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ScheduledStartDateTime

Date and time when the production of this item is scheduled to begin.

_Type_: **datetime (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### Document

The Id of the work order, containing the item. [Required] [Filter(multi eq)]

_Type_: **[WorkOrders](Production.ShopFloor.WorkOrders.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  

### Lot

The lot of the produced product. [Filter(multi eq)]

_Type_: **[Lots](Logistics.Inventory.Lots.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

_Back-End Default Expression:_  
`IIF( ( obj.Lot.Product != obj.Product), null, obj.Lot)`

_Front-End Recalc Expressions:_  
`IIF( ( obj.Lot.Product != obj.Product), null, obj.Lot)`
### OutputStore

Output store for the production. [Filter(multi eq)]

_Type_: **[Stores](Logistics.Inventory.Stores.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

_Back-End Default Expression:_  
`obj.WorkOrder.DefaultOutputStore`

_Front-End Recalc Expressions:_  
`obj.WorkOrder.DefaultOutputStore`
### ParentDocument

The document, which the current line executes. null when the current line does not execute another line. [Filter(multi eq)]

_Type_: **[Documents](General.Documents.md) (nullable)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  

### ProducedQuantityUnit

The measurement unit of the quantity produced in the operation. [Required] [Filter(multi eq)]

_Type_: **[MeasurementUnits](General.MeasurementUnits.md)**  
_Supported Filters_: **Equals, EqualsIn**  

_Back-End Default Expression:_  
`obj.ProductCode.CodingSystem.DefaultMeasurementUnit.IfNullThen( obj.Product.MeasurementUnit.IfNullThen( obj.ProducedQuantityUnit))`

_Front-End Recalc Expressions:_  
`obj.ProductCode.CodingSystem.DefaultMeasurementUnit.IfNullThen( obj.Product.MeasurementUnit.IfNullThen( obj.ProducedQuantityUnit))`
### Product

The Id of the produced product. [Required] [Filter(multi eq)]

_Type_: **[Products](General.Products.Products.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  

_Back-End Default Expression:_  
`obj.ProductCode.Product.IfNullThen( obj.Product)`

_Front-End Recalc Expressions:_  
`obj.ProductCode.Product.IfNullThen( obj.Product)`
### ProductCode

Selects the product thru some of the product codes. [Filter(multi eq)]

_Type_: **[ProductCodes](General.Products.ProductCodes.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

_Back-End Default Expression:_  
`IIF( ( obj.ProductCode.Product != obj.Product), null, obj.ProductCode)`

_Front-End Recalc Expressions:_  
`IIF( ( obj.ProductCode.Product != obj.Product), null, obj.ProductCode)`
### Recipe

The base recipe. null means that the item is produced without recipe. [Filter(multi eq)]

_Type_: **[Recipes](Production.Technologies.Recipes.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

_Front-End Recalc Expressions:_  
`obj.Product.GetDefaultRecipe( ( obj.ReleaseDate ?? obj.WorkOrder.DocumentDate), obj.OutputStore.IfNullThen( obj.WorkOrder.DefaultOutputStore))`
### SerialNumber

If not null, specifies that the product was (has to be) produced with specific serial number. [Filter(multi eq)]

_Type_: **[SerialNumbers](Logistics.Inventory.SerialNumbers.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### StoreBin

The store bin in which to store the products. [Filter(multi eq)]

_Type_: **[StoreBins](Logistics.Inventory.StoreBins.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### WorkOrder

The Id of the work order, containing the item. [Required] [Filter(multi eq)] [Owner]

_Type_: **[WorkOrders](Production.ShopFloor.WorkOrders.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Production.ShopFloor.WorkOrderItems erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Production.ShopFloor.WorkOrderItems erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Production_ShopFloor_WorkOrderItems?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Production_ShopFloor_WorkOrderItems?$top=10>

