# Procedure Prd_Work_Orders_Table_Load_Environment_Items


## Summary

| Name | Type | Description |
| - | - | --- |
|[Id](#id)|`uniqueidentifier` `PK`||
|[Work_Order_Id](#work_order_id)|`uniqueidentifier` |The Id of the work order, containing the item|
|[Parent_Line_Id](#parent_line_id)|`uniqueidentifier` |If not NULL contains the Id of the line of the parent document, that created the current row|
|[Recipe_Id](#recipe_id)|`uniqueidentifier` |The base recipe. NULL means that the item is produced without recipe.|
|[Product_Id](#product_id)|`uniqueidentifier` |The Id of the produced product.|
|[Produced_Quantity](#produced_quantity)|`decimal(18, 3)` |The quantity produced in the operation|
|[Lot_Size](#lot_size)|`decimal(18, 3)` |Quantity produced in one production run|
|[Output_Store_Id](#output_store_id)|`uniqueidentifier` |Output store for the production|
|[Release_Date](#release_date)|`datetime` |The date, when the item is released to production. NULL means that still there is no plan when the item will be released to production|
|[Completion_Date](#completion_date)|`datetime` |The date, when the item should be completed. NULL means that there is no constraint for completion date|
|[Line_Ord](#line_ord)|`int` |The order of the line within the work order.|
|[Priority](#priority)|`smallint` Allowed: `1`, `2`, `3`, `4`, `5`|Priority of the production of the item. Initially inherits the priority of the work order. 1=Lowest ... 5=Highest|
|[Scheduled_Start_Date_Time](#scheduled_start_date_time)|`datetime` |Date and time when the production of this item is scheduled to begin|
|[Scheduled_End_Date_Time](#scheduled_end_date_time)|`datetime` |Date and time when the production of this item is scheduled to end|
|[Produced_Quantity_Unit_Id](#produced_quantity_unit_id)|`uniqueidentifier` ||
|[Produced_Quantity_Base](#produced_quantity_base)|`decimal(0, 0)` ||
|[Lot_Id](#lot_id)|`uniqueidentifier` ||
|[Serial_Number_Id](#serial_number_id)|`uniqueidentifier` ||
|[Product_Code_Id](#product_code_id)|`uniqueidentifier` ||
|[Parent_Document_Id](#parent_document_id)|`uniqueidentifier` ||
|[Parent_Line_No](#parent_line_no)|`int` ||
|[Notes](#notes)|`nvarchar` ||
|[Row_Version](#row_version)|`timestamp` ||
|[Store_Bin_Id](#store_bin_id)|`uniqueidentifier` ||
|[Produced_Standard_Quantity_Base](#produced_standard_quantity_base)|`decimal(0, 0)` ||
|[Standard_Cost_Per_Lot](#standard_cost_per_lot)|`decimal(0, 0)` ||
|[Standard_Price_Per_Lot](#standard_price_per_lot)|`decimal(0, 0)` ||

## Columns

### Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Work_Order_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Parent_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Recipe_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Produced_Quantity

| Property | Value |
| - | - |
|Type|decimal(18, 3)|

### Lot_Size

| Property | Value |
| - | - |
|Type|decimal(18, 3)|

### Output_Store_Id

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

### Line_Ord

| Property | Value |
| - | - |
|Type|int|

### Priority

| Property | Value |
| - | - |
|Type|smallint|

### Scheduled_Start_Date_Time

| Property | Value |
| - | - |
|Type|datetime|

### Scheduled_End_Date_Time

| Property | Value |
| - | - |
|Type|datetime|

### Produced_Quantity_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Produced_Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Lot_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Serial_Number_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Code_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Parent_Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Parent_Line_No

| Property | Value |
| - | - |
|Type|int|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|

### Store_Bin_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Produced_Standard_Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Standard_Cost_Per_Lot

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Standard_Price_Per_Lot

| Property | Value |
| - | - |
|Type|decimal(0, 0)|


