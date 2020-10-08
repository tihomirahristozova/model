---
uid: Logistics.Procurement.RequisitionLines
---
# Logistics.Procurement.RequisitionLines

Detail lines of Requistions. Entity: Scm_Requisition_Lines

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Logistics.Procurement.RequisitionLines.md#id) | guid |  
| [LineNo](Logistics.Procurement.RequisitionLines.md#lineno) | int32 | Line number, unique within the Requisition. Usually is increasing number like 10, 20, 30, ... when initially entering the Requisition (in order to allow insertions with adjustment documents). [Required] 
| [Notes](Logistics.Procurement.RequisitionLines.md#notes) | string (nullable) | Notes for this RequisitionLine. 
| [ProductDescription](Logistics.Procurement.RequisitionLines.md#productdescription) | [MultilanguageString](../data-types.md#multilanguagestring) (nullable) | The description of the required product. When Product is set, this is copied initially from the product name. When Product is null, this contains the manually entered description of the desired product. 
| [Quantity](Logistics.Procurement.RequisitionLines.md#quantity) | [Quantity](../data-types.md#quantity) | The required quantity of the product. [Unit: QuantityUnit] [Required] [Default(0)] [Filter(ge;le)] 
| [QuantityBase](Logistics.Procurement.RequisitionLines.md#quantitybase) | [Quantity](../data-types.md#quantity) | The equivalence of Quantity in the base measurement category of the product. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] [Default(0)] [ReadOnly] 
| [RequiredDeliveryDate](Logistics.Procurement.RequisitionLines.md#requireddeliverydate) | datetime | The desired delivery date. Initially set to the required delivery date in the requisition header or if it is empty - to the document date plus the products lead time. [Required] [Filter(ge;le)] 
| [StandardQuantityBase](Logistics.Procurement.RequisitionLines.md#standardquantitybase) | [Quantity](../data-types.md#quantity) | The theoretical quantity in base measurement unit according to the current measurement dimensions for the product. Used to measure the execution. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] [ReadOnly] (Introduced in version 18.2.100.0) 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Lot](Logistics.Procurement.RequisitionLines.md#lot) | [Logistics.Inventory.Lots](Logistics.Inventory.Lots.md) (nullable) | When not null, indicates a specific lot should be purchased. [Filter(multi eq)] |
| [Product](Logistics.Procurement.RequisitionLines.md#product) | [General.Products.Products](General.Products.Products.md) (nullable) | The required product. When null, the product is unknown to the requisitor and only a description is supplied to the purchase department. [Filter(multi eq)] |
| [QuantityUnit](Logistics.Procurement.RequisitionLines.md#quantityunit) | [General.MeasurementUnits](General.MeasurementUnits.md) | The measurement unit of Quantity. [Required] [Filter(multi eq)] |
| [Requisition](Logistics.Procurement.RequisitionLines.md#requisition) | [Logistics.Procurement.Requisitions](Logistics.Procurement.Requisitions.md) | The [Requisition](Logistics.Procurement.RequisitionLines.md#requisition) to which this RequisitionLine belongs. [Required] [Filter(multi eq)] [Owner] |
| [SuggestedSupplier](Logistics.Procurement.RequisitionLines.md#suggestedsupplier) | [Logistics.Procurement.Suppliers](Logistics.Procurement.Suppliers.md) (nullable) | When the requisitor knows the supplier or has a supplier preference it is denoted in this field. [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### LineNo

> Line number, unique within the Requisition. Usually is increasing number like 10, 20, 30, ... when initially entering the Requisition (in order to allow insertions with adjustment documents). [Required]

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`(obj.Requisition.Lines.Select(c => c.LineNo).DefaultIfEmpty(0).Max() + 10)`

_Front-End Recalc Expressions:_  
`(obj.Requisition.Lines.Select(c => c.LineNo).DefaultIfEmpty(0).Max() + 10)`
### Notes

> Notes for this RequisitionLine.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ProductDescription

> The description of the required product. When Product is set, this is copied initially from the product name. When Product is null, this contains the manually entered description of the desired product.

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring) (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`obj.Product.Name`
### Quantity

> The required quantity of the product. [Unit: QuantityUnit] [Required] [Default(0)] [Filter(ge;le)]

_Type_: **[Quantity](../data-types.md#quantity)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### QuantityBase

> The equivalence of Quantity in the base measurement category of the product. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] [Default(0)] [ReadOnly]

_Type_: **[Quantity](../data-types.md#quantity)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

_Back-End Default Expression:_  
`IIF((((obj.Quantity == null) OrElse (obj.QuantityUnit == null)) OrElse (obj.Product == null)), obj.QuantityBase, obj.Quantity.ConvertTo(obj.Product.BaseUnit, obj.Product))`

_Front-End Recalc Expressions:_  
`IIF((((obj.Quantity == null) OrElse (obj.QuantityUnit == null)) OrElse (obj.Product == null)), obj.QuantityBase, obj.Quantity.ConvertTo(obj.Product.BaseUnit, obj.Product))`
### RequiredDeliveryDate

> The desired delivery date. Initially set to the required delivery date in the requisition header or if it is empty - to the document date plus the products lead time. [Required] [Filter(ge;le)]

_Type_: **datetime**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### StandardQuantityBase

> The theoretical quantity in base measurement unit according to the current measurement dimensions for the product. Used to measure the execution. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] [ReadOnly] (Introduced in version 18.2.100.0)

_Type_: **[Quantity](../data-types.md#quantity)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`IIF((((obj.Quantity == null) OrElse (obj.QuantityUnit == null)) OrElse (obj.Product == null)), obj.StandardQuantityBase, obj.Quantity.ConvertTo(obj.Product.BaseUnit, obj.Product))`

_Front-End Recalc Expressions:_  
`IIF((((obj.Quantity == null) OrElse (obj.QuantityUnit == null)) OrElse (obj.Product == null)), obj.StandardQuantityBase, obj.Quantity.ConvertTo(obj.Product.BaseUnit, obj.Product))`

## Reference Details

### Lot

> When not null, indicates a specific lot should be purchased. [Filter(multi eq)]

_Type_: **[Logistics.Inventory.Lots](Logistics.Inventory.Lots.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### Product

> The required product. When null, the product is unknown to the requisitor and only a description is supplied to the purchase department. [Filter(multi eq)]

_Type_: **[General.Products.Products](General.Products.Products.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### QuantityUnit

> The measurement unit of Quantity. [Required] [Filter(multi eq)]

_Type_: **[General.MeasurementUnits](General.MeasurementUnits.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### Requisition

> The [Requisition](Logistics.Procurement.RequisitionLines.md#requisition) to which this RequisitionLine belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Logistics.Procurement.Requisitions](Logistics.Procurement.Requisitions.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### SuggestedSupplier

> When the requisitor knows the supplier or has a supplier preference it is denoted in this field. [Filter(multi eq)]

_Type_: **[Logistics.Procurement.Suppliers](Logistics.Procurement.Suppliers.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Logistics.Procurement.RequisitionLines erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Logistics.Procurement.RequisitionLines erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Logistics.Procurement.RequisitionLines erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_Procurement_RequisitionLines?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_Procurement_RequisitionLines?$top=10>

