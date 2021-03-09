# Table Log_Shipment_Lines

Represents detail lines of shipments. Each line contains the shipment of one product. Entity: Log_Shipment_Lines

## Owner Tables Hierarchy

* [Log_Shipments](Log_Shipments.md)
* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Shipment_Line_Id](#shipment_line_id)|`uniqueidentifier` `PK`||
|[Shipment_Id](#shipment_id)|`uniqueidentifier` ||
|[Line_No](#line_no)|`int` |Line number, unique for the shipment|
|[Shipment_Order_Line_Id](#shipment_order_line_id)|`uniqueidentifier` |Shipment order line for which this quantity is shipped|
|[Parent_Sales_Order_Line_Id](#parent_sales_order_line_id)|`uniqueidentifier` |Sales order line which is shipped|
|[Quantity](#quantity)|`decimal(12, 3)` |The quantity to be shipped|
|[Quantity_Unit_Id](#quantity_unit_id)|`uniqueidentifier` |The measurement unit of Quantity|
|[Finished](#finished)|`bit` |1 if this shipment should prohibit further shipments for the sales order line|
|[Store_Bin_Id](#store_bin_id)|`uniqueidentifier` |The store bin from which to take the goods|
|[Lot_Id](#lot_id)|`uniqueidentifier` |The store lot from which to take the goods|
|[Serial_Number_Id](#serial_number_id)|`uniqueidentifier` |The serial number of the shipped product. NULL means that serial number is unknown or not applicable.|
|[Guarantee_Period_Days](#guarantee_period_days)|`int` |Guarantee period in days for the offered product. NULL for non-serviced products|
|[Parent_Document_Id](#parent_document_id)|`uniqueidentifier` |The document, which the current line executes. NULL when the current line does not execute another line.|
|[Notes](#notes)|`nvarchar(2147483647)` ||
|[Quantity_Base](#quantity_base)|`decimal(12, 3)` |The equivalence of Quantity in the base measurement category of the product.|
|[Transaction_Line_Id](#transaction_line_id)|`uniqueidentifier` |The Transaction Line, based on which this shipment line was created. The transaction line contains the store issue operation of the shipped product.|
|[Line_Required_Delivery_Date](#line_required_delivery_date)|`datetime` |Required delivery date for this lines. Depending on the shipment route travel time, the shipment should be released accordingly|
|[Parent_Line_No](#parent_line_no)|`int` |The number of the line within the parent document, which the current line executes. NULL when the current line does not execute parent line.|
|[Length_m](#length_m)|`decimal(12, 3)` |The length of the package in meters. NULL means unknown|
|[Pallet_No](#pallet_no)|`int` |The number of the pallet in which the goods are packaged. NULL means unknown|
|[Width_m](#width_m)|`decimal(12, 3)` |The width of the package in meters. NULL means unknown|
|[Row_Version](#row_version)|`timestamp` ||
|[Height_m](#height_m)|`decimal(12, 3)` |The height of the package in meters. NULL means unknown|
|[Volume_l](#volume_l)|`decimal(12, 3)` |The volume in litres of the whole batch. NULL means unknown|
|[Gross_Weight_kg](#gross_weight_kg)|`decimal(12, 3)` |The gross weight of the whole line in kilogramms. NULL means unknown|
|[Net_Weight_kg](#net_weight_kg)|`decimal(12, 3)` |The net weight of the entire batch of goods in kilograms. NULL means unknown|
|[Box_Count](#box_count)|`int` |The count of boxes in which the goods are packaged. NULL means unknown|
|[Standard_Quantity_Base](#standard_quantity_base)|`decimal(12, 3)` Readonly|The theoretical quantity in base measurement unit according to the current measurement dimensions for the product. Used to measure the execution.|

## Columns

### Shipment_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Shipment_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Line_No

| Property | Value |
| - | - |
|Type|int|

### Shipment_Order_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Parent_Sales_Order_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Quantity

| Property | Value |
| - | - |
|Type|decimal(12, 3)|

### Quantity_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Finished

| Property | Value |
| - | - |
|Type|bit|

### Store_Bin_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Lot_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Serial_Number_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Guarantee_Period_Days

| Property | Value |
| - | - |
|Type|int|

### Parent_Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(12, 3)|

### Transaction_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Line_Required_Delivery_Date

| Property | Value |
| - | - |
|Type|datetime|

### Parent_Line_No

| Property | Value |
| - | - |
|Type|int|

### Length_m

| Property | Value |
| - | - |
|Type|decimal(12, 3)|

### Pallet_No

| Property | Value |
| - | - |
|Type|int|

### Width_m

| Property | Value |
| - | - |
|Type|decimal(12, 3)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|

### Height_m

| Property | Value |
| - | - |
|Type|decimal(12, 3)|

### Volume_l

| Property | Value |
| - | - |
|Type|decimal(12, 3)|

### Gross_Weight_kg

| Property | Value |
| - | - |
|Type|decimal(12, 3)|

### Net_Weight_kg

| Property | Value |
| - | - |
|Type|decimal(12, 3)|

### Box_Count

| Property | Value |
| - | - |
|Type|int|

### Standard_Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(12, 3)|


