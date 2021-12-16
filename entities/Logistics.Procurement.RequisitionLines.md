---
uid: Logistics.Procurement.RequisitionLines
---
# Logistics.Procurement.RequisitionLines Entity

**Namespace:** [Logistics.Procurement](Logistics.Procurement.md)  

Detail lines of Requistions. Entity: Scm_Requisition_Lines

## Default Visualization
Default Display Text Format:  
_{LineNo}. {Requisition.DocumentNo} {Requisition.DocumentType.TypeName:T}_  
Default Search Members:  
_Requisition.DocumentNo_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[Logistics.Procurement.Requisitions](Logistics.Procurement.Requisitions.md)  
Aggregate Root:  
[Logistics.Procurement.Requisitions](Logistics.Procurement.Requisitions.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Logistics.Procurement.RequisitionLines.md#id) | guid |  
| [LineNo](Logistics.Procurement.RequisitionLines.md#lineno) | int32 | Line number, unique within the Requisition. Usually is increasing number like 10, 20, 30, ... when initially entering the Requisition (in order to allow insertions with adjustment documents). `Required` 
| [Notes](Logistics.Procurement.RequisitionLines.md#notes) | string (254) __nullable__ | Notes for this RequisitionLine. 
| [ProductDescription](Logistics.Procurement.RequisitionLines.md#productdescription) | [MultilanguageString](../data-types.md#multilanguagestring) __nullable__ | The description of the required product. When Product is set, this is copied initially from the product name. When Product is null, this contains the manually entered description of the desired product. 
| [Quantity](Logistics.Procurement.RequisitionLines.md#quantity) | [Quantity (18, 3)](../data-types.md#quantity) | The required quantity of the product. `Unit: QuantityUnit` `Required` `Default(0)` `Filter(ge;le)` 
| [QuantityBase](Logistics.Procurement.RequisitionLines.md#quantitybase) | [Quantity (18, 3)](../data-types.md#quantity) | The equivalence of Quantity in the base measurement category of the product. `Unit: Product.BaseMeasurementCategory.BaseUnit` `Required` `Default(0)` `ReadOnly` 
| [RequiredDeliveryDate](Logistics.Procurement.RequisitionLines.md#requireddeliverydate) | datetime | The desired delivery date. Initially set to the required delivery date in the requisition header or if it is empty - to the document date plus the products lead time. `Required` `Filter(ge;le)` 
| [RowVersion](Logistics.Procurement.RequisitionLines.md#rowversion) | byte[] |  
| [StandardQuantityBase](Logistics.Procurement.RequisitionLines.md#standardquantitybase) | [Quantity (18, 3)](../data-types.md#quantity) | The theoretical quantity in base measurement unit according to the current measurement dimensions for the product. Used to measure the execution. `Unit: Product.BaseMeasurementCategory.BaseUnit` `Required` `ReadOnly` `Introduced in version 18.2` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Document](Logistics.Procurement.RequisitionLines.md#document) | [Requisitions](Logistics.Procurement.Requisitions.md) | The <see cref="Requisition"/> to which this RequisitionLine belongs. `Required` `Filter(multi eq)` |
| [Lot](Logistics.Procurement.RequisitionLines.md#lot) | [Lots](Logistics.Inventory.Lots.md) (nullable) | When not null, indicates a specific lot should be purchased. `Filter(multi eq)` |
| [Product](Logistics.Procurement.RequisitionLines.md#product) | [Products](General.Products.Products.md) (nullable) | The required product. When null, the product is unknown to the requisitor and only a description is supplied to the purchase department. `Filter(multi eq)` |
| [QuantityUnit](Logistics.Procurement.RequisitionLines.md#quantityunit) | [MeasurementUnits](General.MeasurementUnits.md) | The measurement unit of Quantity. `Required` `Filter(multi eq)` |
| [Requisition](Logistics.Procurement.RequisitionLines.md#requisition) | [Requisitions](Logistics.Procurement.Requisitions.md) | The <see cref="Requisition"/> to which this RequisitionLine belongs. `Required` `Filter(multi eq)` `Owner` |
| [SuggestedSupplier](Logistics.Procurement.RequisitionLines.md#suggestedsupplier) | [Suppliers](Logistics.Procurement.Suppliers.md) (nullable) | When the requisitor knows the supplier or has a supplier preference it is denoted in this field. `Filter(multi eq)` |


## Attribute Details

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### LineNo

Line number, unique within the Requisition. Usually is increasing number like 10, 20, 30, ... when initially entering the Requisition (in order to allow insertions with adjustment documents). `Required`

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`( obj.Requisition.Lines.Select( c => c.LineNo).DefaultIfEmpty( 0).Max( ) + 10)`

_Front-End Recalc Expressions:_  
`( obj.Requisition.Lines.Select( c => c.LineNo).DefaultIfEmpty( 0).Max( ) + 10)`
### Notes

Notes for this RequisitionLine.

_Type_: **string (254) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  

### ProductDescription

The description of the required product. When Product is set, this is copied initially from the product name. When Product is null, this contains the manually entered description of the desired product.

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`obj.Product.Name`
### Quantity

The required quantity of the product. `Unit: QuantityUnit` `Required` `Default(0)` `Filter(ge;le)`

_Type_: **[Quantity (18, 3)](../data-types.md#quantity)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### QuantityBase

The equivalence of Quantity in the base measurement category of the product. `Unit: Product.BaseMeasurementCategory.BaseUnit` `Required` `Default(0)` `ReadOnly`

_Type_: **[Quantity (18, 3)](../data-types.md#quantity)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

_Back-End Default Expression:_  
`IIF( ( ( ( obj.Quantity == null) OrElse ( obj.QuantityUnit == null)) OrElse ( obj.Product == null)), obj.QuantityBase, obj.Quantity.ConvertTo( obj.Product.BaseUnit, obj.Product))`

_Front-End Recalc Expressions:_  
`IIF( ( ( ( obj.Quantity == null) OrElse ( obj.QuantityUnit == null)) OrElse ( obj.Product == null)), obj.QuantityBase, obj.Quantity.ConvertTo( obj.Product.BaseUnit, obj.Product))`
### RequiredDeliveryDate

The desired delivery date. Initially set to the required delivery date in the requisition header or if it is empty - to the document date plus the products lead time. `Required` `Filter(ge;le)`

_Type_: **datetime**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### RowVersion

_Type_: **byte[]**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### StandardQuantityBase

The theoretical quantity in base measurement unit according to the current measurement dimensions for the product. Used to measure the execution. `Unit: Product.BaseMeasurementCategory.BaseUnit` `Required` `ReadOnly` `Introduced in version 18.2`

_Type_: **[Quantity (18, 3)](../data-types.md#quantity)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`IIF( ( ( ( obj.Quantity == null) OrElse ( obj.QuantityUnit == null)) OrElse ( obj.Product == null)), obj.StandardQuantityBase, obj.Quantity.ConvertTo( obj.Product.BaseUnit, obj.Product))`

_Front-End Recalc Expressions:_  
`IIF( ( ( ( obj.Quantity == null) OrElse ( obj.QuantityUnit == null)) OrElse ( obj.Product == null)), obj.StandardQuantityBase, obj.Quantity.ConvertTo( obj.Product.BaseUnit, obj.Product))`

## Reference Details

### Document

The <see cref="Requisition"/> to which this RequisitionLine belongs. `Required` `Filter(multi eq)`

_Type_: **[Requisitions](Logistics.Procurement.Requisitions.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  

### Lot

When not null, indicates a specific lot should be purchased. `Filter(multi eq)`

_Type_: **[Lots](Logistics.Inventory.Lots.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### Product

The required product. When null, the product is unknown to the requisitor and only a description is supplied to the purchase department. `Filter(multi eq)`

_Type_: **[Products](General.Products.Products.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### QuantityUnit

The measurement unit of Quantity. `Required` `Filter(multi eq)`

_Type_: **[MeasurementUnits](General.MeasurementUnits.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### Requisition

The <see cref="Requisition"/> to which this RequisitionLine belongs. `Required` `Filter(multi eq)` `Owner`

_Type_: **[Requisitions](Logistics.Procurement.Requisitions.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  

### SuggestedSupplier

When the requisitor knows the supplier or has a supplier preference it is denoted in this field. `Filter(multi eq)`

_Type_: **[Suppliers](Logistics.Procurement.Suppliers.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list limit=1000 erp.entity=Logistics.Procurement.RequisitionLines erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Logistics.Procurement.RequisitionLines erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_Procurement_RequisitionLines?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_Procurement_RequisitionLines?$top=10>

