# Table Prd_Work_Order_Items

The different items that are produced with a work order. Entity: Prd_Work_Order_Items

## Owner Tables Hierarchy

* [Prd_Work_Orders](Prd_Work_Orders.md)
* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Line_Ord](#line_ord)|`int` |The order of the line within the work order.|
|[Product_Id](#product_id)|`uniqueidentifier` |The Id of the produced product.|
|[Recipe_Id](#recipe_id)|`uniqueidentifier` |The base recipe. NULL means that the item is produced without recipe.|
|[Produced_Quantity](#produced_quantity)|`decimal(18, 3)` |The quantity produced in the operation|
|[Produced_Quantity_Unit_Id](#produced_quantity_unit_id)|`uniqueidentifier` |The measurement unit of the quantity produced in the operation|
|[Release_Date](#release_date)|`datetime` |The date, when the item is released to production. NULL means that still there is no plan when the item will be released to production|
|[Completion_Date](#completion_date)|`datetime` |The date, when the item should be completed. NULL means that there is no constraint for completion date|
|[Id](#id)|`uniqueidentifier` `PK`||
|[Row_Version](#row_version)|`timestamp` ||
|[Notes](#notes)|`nvarchar(2147483647)` ||
|[Parent_Line_No](#parent_line_no)|`int` |The number of the line within the parent document, which the current line executes. NULL when the current line does not execute another line.|
|[Parent_Document_Id](#parent_document_id)|`uniqueidentifier` |The document, which the current line executes. NULL when the current line does not execute another line.|
|[Product_Code_Id](#product_code_id)|`uniqueidentifier` |Selects the product thru some of the product codes.|
|[Serial_Number_Id](#serial_number_id)|`uniqueidentifier` |If not NULL, specifies that the product was (has to be) produced with specific serial number|
|[Lot_Id](#lot_id)|`uniqueidentifier` |The lot of the produced product.|
|[Scheduled_Start_Date_Time](#scheduled_start_date_time)|`datetime` |Date and time when the production of this item is scheduled to begin|
|[Scheduled_End_Date_Time](#scheduled_end_date_time)|`datetime` |Date and time when the production of this item is scheduled to end|
|[Store_Bin_Id](#store_bin_id)|`uniqueidentifier` |The store bin in which to store the products|
|[Priority](#priority)|`smallint` Allowed: `1`, `2`, `3`, `4`, `5`|Priority of the production of the item. Initially inherits the priority of the work order. 1=Lowest ... 5=Highest|
|[Output_Store_Id](#output_store_id)|`uniqueidentifier` |Output store for the production|
|[Lot_Size](#lot_size)|`decimal(18, 3)` |Quantity produced in one production run|
|[Parent_Line_Id](#parent_line_id)|`uniqueidentifier` |If not NULL contains the Id of the line of the parent document, that created the current row|
|[Work_Order_Id](#work_order_id)|`uniqueidentifier` |The Id of the work order, containing the item|
|[Produced_Quantity_Base](#produced_quantity_base)|`decimal(18, 3)` Readonly|The equivalence of Produced Quantity in the base measurement category of the product.|
|[Produced_Standard_Quantity_Base](#produced_standard_quantity_base)|`decimal(18, 3)` Readonly|The theoretical quantity in base measurement unit according to the current measurement dimensions of the product. Used to measure the execution. NULL means to take the value from Produced Quantity Base.|

## Columns

### Line_Ord

| Property | Value |
| - | - |
|Type|int|

### Product_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Recipe_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Produced_Quantity

| Property | Value |
| - | - |
|Type|decimal(18, 3)|

### Produced_Quantity_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Release_Date

| Property | Value |
| - | - |
|Type|datetime|

### Completion_Date

| Property | Value |
| - | - |
|Type|datetime|

### Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Parent_Line_No

| Property | Value |
| - | - |
|Type|int|

### Parent_Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Code_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Serial_Number_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Lot_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Scheduled_Start_Date_Time

| Property | Value |
| - | - |
|Type|datetime|

### Scheduled_End_Date_Time

| Property | Value |
| - | - |
|Type|datetime|

### Store_Bin_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Priority

| Property | Value |
| - | - |
|Type|smallint|

### Output_Store_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Lot_Size

| Property | Value |
| - | - |
|Type|decimal(18, 3)|

### Parent_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Work_Order_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Produced_Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(18, 3)|

### Produced_Standard_Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(18, 3)|


