# Table Scm_Requisition_Lines

Detail lines of Requistions. Entity: Scm_Requisition_Lines

## Owner Tables Hierarchy

* [Scm_Requisitions](Scm_Requisitions.md)
* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Requisition_Line_Id](#requisition_line_id)|`uniqueidentifier` `PK`||
|[Requisition_Id](#requisition_id)|`uniqueidentifier` ||
|[Line_No](#line_no)|`int` ||
|[Product_Id](#product_id)|`uniqueidentifier` |The required product. When null, the product is unknown to the requisitor and only a description is supplied to the purchase department.|
|[Product_Description](#product_description)|`nvarchar(254)` `ML`|The description of the required product. When Product is set, this is copied initially from the product name. When Product is null, this contains the manually entered description of the desired product.|
|[Suggested_Supplier_Id](#suggested_supplier_id)|`uniqueidentifier` |When the requisitor knows the supplier or has a supplier preference it is denoted in this field.|
|[Quantity](#quantity)|`decimal(18, 3)` |The required quantity of the product.|
|[Quantity_Unit_Id](#quantity_unit_id)|`uniqueidentifier` |The measurement unit of Quantity.|
|[Required_Delivery_Date](#required_delivery_date)|`datetime` |The desired delivery date. Initially set to the required delivery date in the requisition header or if it is empty - to the document date plus the products lead time.|
|[Notes](#notes)|`nvarchar(254)` ||
|[Quantity_Base](#quantity_base)|`decimal(18, 3)` Readonly|The equivalence of Quantity in the base measurement category of the product.|
|[Lot_Id](#lot_id)|`uniqueidentifier` |When not null, indicates a specific lot should be purchased.|
|[Row_Version](#row_version)|`timestamp` ||
|[Standard_Quantity_Base](#standard_quantity_base)|`decimal(18, 3)` Readonly|The theoretical quantity in base measurement unit according to the current measurement dimensions for the product. Used to measure the execution.|

## Columns

### Requisition_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Requisition_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Line_No

| Property | Value |
| - | - |
|Type|int|

### Product_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Description

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Suggested_Supplier_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Quantity

| Property | Value |
| - | - |
|Type|decimal(18, 3)|

### Quantity_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Required_Delivery_Date

| Property | Value |
| - | - |
|Type|datetime|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(18, 3)|

### Lot_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|

### Standard_Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(18, 3)|


