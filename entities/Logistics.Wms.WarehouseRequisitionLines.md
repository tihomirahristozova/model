---
uid: Logistics.Wms.WarehouseRequisitionLines
---
# Logistics.Wms.WarehouseRequisitionLines Entity

**Namespace:** [Logistics.Wms](Logistics.Wms.md)  

Request for one product with a warehouse requisition. Entity: Wms_Warehouse_Requisition_Lines (Introduced in version 20.1)

## Default Visualization
Default Display Text Format:  
_{LineNo}. {WarehouseRequisition.DocumentNo} {WarehouseRequisition.DocumentType.TypeName:T}_  
Default Search Member:  
_WarehouseRequisition.DocumentNo_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[Logistics.Wms.WarehouseRequisitions](Logistics.Wms.WarehouseRequisitions.md)  
Aggregate Root:  
[Logistics.Wms.WarehouseRequisitions](Logistics.Wms.WarehouseRequisitions.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Logistics.Wms.WarehouseRequisitionLines.md#id) | guid |  
| [LineNo](Logistics.Wms.WarehouseRequisitionLines.md#lineno) | int32 | The unique, consecutive line number within the requisition. `Required` 
| [Notes](Logistics.Wms.WarehouseRequisitionLines.md#notes) | string (max) __nullable__ | Notes for this WarehouseRequisitionLine. 
| [ParentLineNo](Logistics.Wms.WarehouseRequisitionLines.md#parentlineno) | int32 __nullable__ | The number of the line within the parent document, which the current line executes. null when the current line does not execute line. 
| [Quantity](Logistics.Wms.WarehouseRequisitionLines.md#quantity) | [Quantity (12, 3)](../data-types.md#quantity) | The requested quantity. `Unit: QuantityUnit` `Required` `Filter(eq;ge;le)` 
| [QuantityBase](Logistics.Wms.WarehouseRequisitionLines.md#quantitybase) | [Quantity (12, 3)](../data-types.md#quantity) | Quantity in the base measurement unit of the product. `Unit: Product.BaseMeasurementCategory.BaseUnit` `Required` `Filter(multi eq;ge;le)` `Introduced in version 21.1.1.33` 
| [StandardQuantity](Logistics.Wms.WarehouseRequisitionLines.md#standardquantity) | [Quantity (12, 3)](../data-types.md#quantity) | The theoretical quantity in base measurement unit according to the current measurement dimensions for the product. Used to measure the execution. `Unit: Product.BaseMeasurementCategory.BaseUnit` `Required` `Introduced in version 22.1.4.42` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Document](Logistics.Wms.WarehouseRequisitionLines.md#document) | [WarehouseRequisitions](Logistics.Wms.WarehouseRequisitions.md) | The `WarehouseRequisition`(Logistics.Wms.WarehouseRequisitionLines.md#warehouserequisition) to which this WarehouseRequisitionLine belongs. `Required` `Filter(multi eq)` |
| [Lot](Logistics.Wms.WarehouseRequisitionLines.md#lot) | [Lots](Logistics.Inventory.Lots.md) (nullable) | The requested lot. null means that any lot can be used or the product does not use lots at all. `Filter(multi eq)` |
| [ParentDocument](Logistics.Wms.WarehouseRequisitionLines.md#parentdocument) | [Documents](General.Documents.md) (nullable) | The document, which the current line executes. null when the current line does not execute another line. `Filter(multi eq)` |
| [Product](Logistics.Wms.WarehouseRequisitionLines.md#product) | [Products](General.Products.Products.md) | The requested product. `Required` `Filter(multi eq)` |
| [QuantityUnit](Logistics.Wms.WarehouseRequisitionLines.md#quantityunit) | [MeasurementUnits](General.MeasurementUnits.md) | The measurement unit of Quantity. `Required` `Filter(multi eq)` |
| [SerialNumber](Logistics.Wms.WarehouseRequisitionLines.md#serialnumber) | [SerialNumbers](Logistics.Inventory.SerialNumbers.md) (nullable) | The requested serial number. null means that any serial number can be used or the product does not use serial numbers at all. `Filter(multi eq)` |
| [WarehouseRequisition](Logistics.Wms.WarehouseRequisitionLines.md#warehouserequisition) | [WarehouseRequisitions](Logistics.Wms.WarehouseRequisitions.md) | The `WarehouseRequisition`(Logistics.Wms.WarehouseRequisitionLines.md#warehouserequisition) to which this WarehouseRequisitionLine belongs. `Required` `Filter(multi eq)` `Owner` |


## Attribute Details

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### LineNo

The unique, consecutive line number within the requisition. `Required`

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`( obj.WarehouseRequisition.Lines.Select( c => c.LineNo).DefaultIfEmpty( 0).Max( ) + 10)`

_Front-End Recalc Expressions:_  
`( obj.WarehouseRequisition.Lines.Select( c => c.LineNo).DefaultIfEmpty( 0).Max( ) + 10)`
### Notes

Notes for this WarehouseRequisitionLine.

_Type_: **string (max) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  

### ParentLineNo

The number of the line within the parent document, which the current line executes. null when the current line does not execute line.

_Type_: **int32 __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Quantity

The requested quantity. `Unit: QuantityUnit` `Required` `Filter(eq;ge;le)`

_Type_: **[Quantity (12, 3)](../data-types.md#quantity)**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### QuantityBase

Quantity in the base measurement unit of the product. `Unit: Product.BaseMeasurementCategory.BaseUnit` `Required` `Filter(multi eq;ge;le)` `Introduced in version 21.1.1.33`

_Type_: **[Quantity (12, 3)](../data-types.md#quantity)**  
_Supported Filters_: **Equals, GreaterThanOrLessThan, EqualsIn**  
_Supports Order By_: **False**  

### StandardQuantity

The theoretical quantity in base measurement unit according to the current measurement dimensions for the product. Used to measure the execution. `Unit: Product.BaseMeasurementCategory.BaseUnit` `Required` `Introduced in version 22.1.4.42`

_Type_: **[Quantity (12, 3)](../data-types.md#quantity)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### Document

The `WarehouseRequisition`(Logistics.Wms.WarehouseRequisitionLines.md#warehouserequisition) to which this WarehouseRequisitionLine belongs. `Required` `Filter(multi eq)`

_Type_: **[WarehouseRequisitions](Logistics.Wms.WarehouseRequisitions.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  

### Lot

The requested lot. null means that any lot can be used or the product does not use lots at all. `Filter(multi eq)`

_Type_: **[Lots](Logistics.Inventory.Lots.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### ParentDocument

The document, which the current line executes. null when the current line does not execute another line. `Filter(multi eq)`

_Type_: **[Documents](General.Documents.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### Product

The requested product. `Required` `Filter(multi eq)`

_Type_: **[Products](General.Products.Products.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### QuantityUnit

The measurement unit of Quantity. `Required` `Filter(multi eq)`

_Type_: **[MeasurementUnits](General.MeasurementUnits.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### SerialNumber

The requested serial number. null means that any serial number can be used or the product does not use serial numbers at all. `Filter(multi eq)`

_Type_: **[SerialNumbers](Logistics.Inventory.SerialNumbers.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### WarehouseRequisition

The `WarehouseRequisition`(Logistics.Wms.WarehouseRequisitionLines.md#warehouserequisition) to which this WarehouseRequisitionLine belongs. `Required` `Filter(multi eq)` `Owner`

_Type_: **[WarehouseRequisitions](Logistics.Wms.WarehouseRequisitions.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  



## Business Rules

[!list limit=1000 erp.entity=Logistics.Wms.WarehouseRequisitionLines erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Logistics.Wms.WarehouseRequisitionLines erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_Wms_WarehouseRequisitionLines?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_Wms_WarehouseRequisitionLines?$top=10>

