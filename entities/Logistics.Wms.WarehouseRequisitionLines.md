---
uid: Logistics.Wms.WarehouseRequisitionLines
---
# Logistics.Wms.WarehouseRequisitionLines

Request for one product with a warehouse requisition. Entity: Wms_Warehouse_Requisition_Lines (Introduced in version 20.1.100.0)

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Logistics.Wms.WarehouseRequisitionLines.md#Id) | guid |  
| [LineNo](Logistics.Wms.WarehouseRequisitionLines.md#LineNo) | int32 | The unique, consecutive line number within the requisition. [Required] 
| [Notes](Logistics.Wms.WarehouseRequisitionLines.md#Notes) | string (nullable) | Notes for this WarehouseRequisitionLine. 
| [ParentLineNo](Logistics.Wms.WarehouseRequisitionLines.md#ParentLineNo) | int32 (nullable) | The number of the line within the parent document, which the current line executes. null when the current line does not execute line. 
| [Quantity](Logistics.Wms.WarehouseRequisitionLines.md#Quantity) | [Quantity](../data-types.md#Quantity) | The requested quantity. [Unit: QuantityUnit] [Required] [Filter(eq;ge;le)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Lot](Logistics.Wms.WarehouseRequisitionLines.md#Lot) | [Logistics.Inventory.Lots](Logistics.Inventory.Lots.md) (nullable) | The requested lot. null means that any lot can be used or the product does not use lots at all. [Filter(multi eq)] |
| [ParentDocument](Logistics.Wms.WarehouseRequisitionLines.md#ParentDocument) | [General.Documents](General.Documents.md) (nullable) | The document, which the current line executes. null when the current line does not execute another line. [Filter(multi eq)] |
| [Product](Logistics.Wms.WarehouseRequisitionLines.md#Product) | [General.Products.Products](General.Products.Products.md) | The requested product. [Required] [Filter(multi eq)] |
| [QuantityUnit](Logistics.Wms.WarehouseRequisitionLines.md#QuantityUnit) | [General.MeasurementUnits](General.MeasurementUnits.md) | The measurement unit of Quantity. [Required] [Filter(multi eq)] |
| [SerialNumber](Logistics.Wms.WarehouseRequisitionLines.md#SerialNumber) | [Logistics.Inventory.SerialNumbers](Logistics.Inventory.SerialNumbers.md) (nullable) | The requested serial number. null means that any serial number can be used or the product does not use serial numbers at all. [Filter(multi eq)] |
| [WarehouseRequisition](Logistics.Wms.WarehouseRequisitionLines.md#WarehouseRequisition) | [Logistics.Wms.WarehouseRequisitions](Logistics.Wms.WarehouseRequisitions.md) | The [WarehouseRequisition](Logistics.Wms.WarehouseRequisitionLines.md#WarehouseRequisition) to which this WarehouseRequisitionLine belongs. [Required] [Filter(multi eq)] [Owner] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### LineNo

> The unique, consecutive line number within the requisition. [Required]

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`(obj.WarehouseRequisition.Lines.Select(c => c.LineNo).DefaultIfEmpty(0).Max() + 10)`

_Front-End Recalc Expressions:_  
`(obj.WarehouseRequisition.Lines.Select(c => c.LineNo).DefaultIfEmpty(0).Max() + 10)`
### Notes

> Notes for this WarehouseRequisitionLine.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ParentLineNo

> The number of the line within the parent document, which the current line executes. null when the current line does not execute line.

_Type_: **int32 (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Quantity

> The requested quantity. [Unit: QuantityUnit] [Required] [Filter(eq;ge;le)]

_Type_: **[Quantity](../data-types.md#Quantity)**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  


## Reference Details

### Lot

> The requested lot. null means that any lot can be used or the product does not use lots at all. [Filter(multi eq)]

_Type_: **[Logistics.Inventory.Lots](Logistics.Inventory.Lots.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### ParentDocument

> The document, which the current line executes. null when the current line does not execute another line. [Filter(multi eq)]

_Type_: **[General.Documents](General.Documents.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Product

> The requested product. [Required] [Filter(multi eq)]

_Type_: **[General.Products.Products](General.Products.Products.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### QuantityUnit

> The measurement unit of Quantity. [Required] [Filter(multi eq)]

_Type_: **[General.MeasurementUnits](General.MeasurementUnits.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### SerialNumber

> The requested serial number. null means that any serial number can be used or the product does not use serial numbers at all. [Filter(multi eq)]

_Type_: **[Logistics.Inventory.SerialNumbers](Logistics.Inventory.SerialNumbers.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### WarehouseRequisition

> The [WarehouseRequisition](Logistics.Wms.WarehouseRequisitionLines.md#WarehouseRequisition) to which this WarehouseRequisitionLine belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Logistics.Wms.WarehouseRequisitions](Logistics.Wms.WarehouseRequisitions.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Logistics.Wms.WarehouseRequisitionLines erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Logistics.Wms.WarehouseRequisitionLines erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Logistics.Wms.WarehouseRequisitionLines erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_Wms_WarehouseRequisitionLines?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_Wms_WarehouseRequisitionLines?$top=10>

