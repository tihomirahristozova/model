---
uid: Production.ShopFloor.ConsumptionOrderLines
---
# Production.ShopFloor.ConsumptionOrderLines

Detail lines of orders for material consumption. Entity: Prd_Consumption_Order_Lines

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Production.ShopFloor.ConsumptionOrderLines.md#Id) | guid |  
| [ConsumedQuantity](Production.ShopFloor.ConsumptionOrderLines.md#ConsumedQuantity) | [Quantity](../data-types.md#Quantity) | Requested quantity of the material. [Unit: ConsumedQuantityUnit] [Required] [Filter(ge;le)] 
| [ConsumedQuantityBase](Production.ShopFloor.ConsumptionOrderLines.md#ConsumedQuantityBase) | [Quantity](../data-types.md#Quantity) | The requested quantity equivalence in the base measurement category of the requested material. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] [ReadOnly] 
| [ConsumedStandardQuantityBase](Production.ShopFloor.ConsumptionOrderLines.md#ConsumedStandardQuantityBase) | [Quantity](../data-types.md#Quantity) | The theoretical quantity in base measurement unit according to the current measurement dimensions for the product. Used to measure the execution. null means to convert the value from Quantity using the measurement ratios. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] [ReadOnly] (Introduced in version 18.2.100.0) 
| [ConsumptionType](Production.ShopFloor.ConsumptionOrderLines.md#ConsumptionType) | [Production.ShopFloor.ConsumptionOrderLinesRepository.ConsumptionType](Production.ShopFloor.ConsumptionOrderLines.md#ConsumptionType) | Determines whether the material cost is distributed among all produced products, or only one (specified in the Work Order Item Ingredient). [Required] [Filter(eq)] [ReadOnly] 
| [LineOrd](Production.ShopFloor.ConsumptionOrderLines.md#LineOrd) | int32 | Non-unique line number within the order. [Required] 
| [Notes](Production.ShopFloor.ConsumptionOrderLines.md#Notes) | string (nullable) | Notes for this ConsumptionOrderLine. 
| [ScheduledDateTime](Production.ShopFloor.ConsumptionOrderLines.md#ScheduledDateTime) | datetime (nullable) | The scheduled date, when the material is needed. [Filter(ge;le)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [ConsumedQuantityUnit](Production.ShopFloor.ConsumptionOrderLines.md#ConsumedQuantityUnit) | [General.MeasurementUnits](General.MeasurementUnits.md) | Measurement unit of the requested quantity. [Required] [Filter(multi eq)] |
| [ConsumptionOrder](Production.ShopFloor.ConsumptionOrderLines.md#ConsumptionOrder) | [Production.ShopFloor.ConsumptionOrders](Production.ShopFloor.ConsumptionOrders.md) | The [ConsumptionOrder](Production.ShopFloor.ConsumptionOrderLines.md#ConsumptionOrder) to which this ConsumptionOrderLine belongs. [Required] [Filter(multi eq)] [Owner] |
| [Lot](Production.ShopFloor.ConsumptionOrderLines.md#Lot) | [Logistics.Inventory.Lots](Logistics.Inventory.Lots.md) (nullable) | If not null, specifies that the material has to be consumed from specific lot. [Filter(multi eq)] |
| [Product](Production.ShopFloor.ConsumptionOrderLines.md#Product) | [General.Products.Products](General.Products.Products.md) | The requested material. [Required] [Filter(multi eq)] |
| [SerialNumber](Production.ShopFloor.ConsumptionOrderLines.md#SerialNumber) | [Logistics.Inventory.SerialNumbers](Logistics.Inventory.SerialNumbers.md) (nullable) | If not null, specifies that the material has to be consumed with specific serial number. [Filter(multi eq)] |
| [StoreBin](Production.ShopFloor.ConsumptionOrderLines.md#StoreBin) | [Logistics.Inventory.StoreBins](Logistics.Inventory.StoreBins.md) (nullable) | If not null, specifies that the material has to be consumed from specific store bin. [Filter(multi eq)] |
| [Store](Production.ShopFloor.ConsumptionOrderLines.md#Store) | [Logistics.Inventory.Stores](Logistics.Inventory.Stores.md) (nullable) | The store, from which the material is requested. [Filter(multi eq)] |
| [WorkOrderItemIngredient](Production.ShopFloor.ConsumptionOrderLines.md#WorkOrderItemIngredient) | [Production.ShopFloor.WorkOrderItemIngredients](Production.ShopFloor.WorkOrderItemIngredients.md) | The Work Order Item Ingredient for which we are ordering materials. [Required] [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### ConsumedQuantity

> Requested quantity of the material. [Unit: ConsumedQuantityUnit] [Required] [Filter(ge;le)]

_Type_: **[Quantity](../data-types.md#Quantity)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`IIF((obj.ConsumedQuantityUnit == null), null, IIF((obj.WorkOrderItemIngredient != null), obj.WorkOrderItemIngredient.GetSumConsumedQuantity(obj.ConsumedQuantityUnit), obj.ConsumedQuantity))`
### ConsumedQuantityBase

> The requested quantity equivalence in the base measurement category of the requested material. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] [ReadOnly]

_Type_: **[Quantity](../data-types.md#Quantity)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`IIF((((obj.ConsumedQuantity == null) OrElse (obj.ConsumedQuantityUnit == null)) OrElse (obj.Product == null)), obj.ConsumedQuantityBase, obj.ConsumedQuantity.ConvertTo(obj.Product.BaseUnit, obj.Product))`

_Front-End Recalc Expressions:_  
`IIF((((obj.ConsumedQuantity == null) OrElse (obj.ConsumedQuantityUnit == null)) OrElse (obj.Product == null)), obj.ConsumedQuantityBase, obj.ConsumedQuantity.ConvertTo(obj.Product.BaseUnit, obj.Product))`
### ConsumedStandardQuantityBase

> The theoretical quantity in base measurement unit according to the current measurement dimensions for the product. Used to measure the execution. null means to convert the value from Quantity using the measurement ratios. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] [ReadOnly] (Introduced in version 18.2.100.0)

_Type_: **[Quantity](../data-types.md#Quantity)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`IIF((((obj.ConsumedQuantity == null) OrElse (obj.ConsumedQuantityUnit == null)) OrElse (obj.Product == null)), obj.ConsumedStandardQuantityBase, obj.ConsumedQuantity.ConvertTo(obj.Product.BaseUnit, obj.Product))`

_Front-End Recalc Expressions:_  
`IIF((((obj.ConsumedQuantity == null) OrElse (obj.ConsumedQuantityUnit == null)) OrElse (obj.Product == null)), obj.ConsumedStandardQuantityBase, obj.ConsumedQuantity.ConvertTo(obj.Product.BaseUnit, obj.Product))`
### ConsumptionType

> Determines whether the material cost is distributed among all produced products, or only one (specified in the Work Order Item Ingredient). [Required] [Filter(eq)] [ReadOnly]

_Type_: **[Production.ShopFloor.ConsumptionOrderLinesRepository.ConsumptionType](Production.ShopFloor.ConsumptionOrderLines.md#ConsumptionType)**  
Allowed values for the [ConsumptionType](Production.ShopFloor.ConsumptionOrderLines.md#ConsumptionType) data attribute  
_Allowed Values (Enum Members)_  

| Value | Description |
| ---- | --- |
| ForSpecifiedItem | ForSpecifiedItem value. Stored as 'S'. <br /> _Database Value:_ 'S' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'ForSpecifiedItem' |
| ForAllItems | ForAllItems value. Stored as 'A'. <br /> _Database Value:_ 'A' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'ForAllItems' |

_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`IIF(((obj.WorkOrderItemIngredient != null) AndAlso (obj.WorkOrderItemIngredient.WorkOrderItem != null)), ForSpecifiedItem, ForAllItems)`
### LineOrd

> Non-unique line number within the order. [Required]

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`(obj.ConsumptionOrder.Lines.Select(c => c.LineOrd).DefaultIfEmpty(0).Max() + 10)`

_Front-End Recalc Expressions:_  
`(obj.ConsumptionOrder.Lines.Select(c => c.LineOrd).DefaultIfEmpty(0).Max() + 10)`
### Notes

> Notes for this ConsumptionOrderLine.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ScheduledDateTime

> The scheduled date, when the material is needed. [Filter(ge;le)]

_Type_: **datetime (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  


## Reference Details

### ConsumedQuantityUnit

> Measurement unit of the requested quantity. [Required] [Filter(multi eq)]

_Type_: **[General.MeasurementUnits](General.MeasurementUnits.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`obj.Product.MeasurementUnit`
### ConsumptionOrder

> The [ConsumptionOrder](Production.ShopFloor.ConsumptionOrderLines.md#ConsumptionOrder) to which this ConsumptionOrderLine belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Production.ShopFloor.ConsumptionOrders](Production.ShopFloor.ConsumptionOrders.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Lot

> If not null, specifies that the material has to be consumed from specific lot. [Filter(multi eq)]

_Type_: **[Logistics.Inventory.Lots](Logistics.Inventory.Lots.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Product

> The requested material. [Required] [Filter(multi eq)]

_Type_: **[General.Products.Products](General.Products.Products.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`obj.WorkOrderItemIngredient.Material`
### SerialNumber

> If not null, specifies that the material has to be consumed with specific serial number. [Filter(multi eq)]

_Type_: **[Logistics.Inventory.SerialNumbers](Logistics.Inventory.SerialNumbers.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### StoreBin

> If not null, specifies that the material has to be consumed from specific store bin. [Filter(multi eq)]

_Type_: **[Logistics.Inventory.StoreBins](Logistics.Inventory.StoreBins.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Store

> The store, from which the material is requested. [Filter(multi eq)]

_Type_: **[Logistics.Inventory.Stores](Logistics.Inventory.Stores.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`obj.ConsumptionOrder.Store`

_Front-End Recalc Expressions:_  
`obj.ConsumptionOrder.Store`
### WorkOrderItemIngredient

> The Work Order Item Ingredient for which we are ordering materials. [Required] [Filter(multi eq)]

_Type_: **[Production.ShopFloor.WorkOrderItemIngredients](Production.ShopFloor.WorkOrderItemIngredients.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Production.ShopFloor.ConsumptionOrderLines erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Production.ShopFloor.ConsumptionOrderLines erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Production.ShopFloor.ConsumptionOrderLines erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Production_ShopFloor_ConsumptionOrderLines?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Production_ShopFloor_ConsumptionOrderLines?$top=10>

