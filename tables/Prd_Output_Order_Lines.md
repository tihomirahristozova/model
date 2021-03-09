# Table Prd_Output_Order_Lines

Detail records of output orders. Entity: Prd_Output_Order_Lines

## Owner Tables Hierarchy

* [Prd_Output_Orders](Prd_Output_Orders.md)
* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Id](#id)|`uniqueidentifier` `PK`||
|[Output_Order_Id](#output_order_id)|`uniqueidentifier` ||
|[Line_Ord](#line_ord)|`int` |Line number within the order|
|[Line_Work_Order_Id](#line_work_order_id)|`uniqueidentifier` |The work order for which work is being accounted|
|[Work_Order_Item_Id](#work_order_item_id)|`uniqueidentifier` |The work order item for which this output is recorded.|
|[Work_Order_Item_Operation_Id](#work_order_item_operation_id)|`uniqueidentifier` |The operation for which this output is recorded.|
|[Transaction_Timestamp](#transaction_timestamp)|`datetime` Readonly|Sets the timestamp of the receipt store operations for this output order line. Used in completing output orders.|
|[Product_Code_Id](#product_code_id)|`uniqueidentifier` |Selects the product thru some of the product codes.|
|[Lot_Id](#lot_id)|`uniqueidentifier` |The lot of the produced product.|
|[Workgroup_Resource_Id](#workgroup_resource_id)|`uniqueidentifier` |The resource, which was used to perform the operation.|
|[Work_Done_By_Party_Id](#work_done_by_party_id)|`uniqueidentifier` |The party (usually employee worker) who has accomplished the work. NULL if unknown or N/A|
|[Notes](#notes)|`nvarchar(2147483647)` ||
|[End_Time](#end_time)|`datetime` |Date and time when the operation has ended|
|[Start_Time](#start_time)|`datetime` |Date and time when the operation has began|
|[Store_Bin_Id](#store_bin_id)|`uniqueidentifier` |If not NULL, specifies that the product was (has to be) stored to specific store bin|
|[Serial_Number_Id](#serial_number_id)|`uniqueidentifier` |If not NULL, specifies that the product was (has to be) stored with specific serial number|
|[Row_Version](#row_version)|`timestamp` ||
|[Store_Id](#store_id)|`uniqueidentifier` |Where to output the produced quantity. Can be NULL only if Produced_Quantity = 0|
|[Produced_Quantity_Base](#produced_quantity_base)|`decimal(18, 3)` Readonly|The equivalence of Produced Quantity in the base measurement unit of the product.|
|[Produced_Quantity_Unit_Id](#produced_quantity_unit_id)|`uniqueidentifier` |The measurement unit of Produced Quantity.|
|[Produced_Quantity](#produced_quantity)|`decimal(18, 3)` |The processed quantity of the end product.|
|[Begin_Date_Time](#begin_date_time)|`datetime` |Not used.|
|[Product_Id](#product_id)|`uniqueidentifier` |The actually produced product|
|[Finished](#finished)|`bit` |1 if this output entry completes the operation. 0 if there might be more entries|
|[Produced_Standard_Quantity_Base](#produced_standard_quantity_base)|`decimal(18, 3)` Readonly|The theoretical quantity in base measurement unit according to the current measurement dimensions for the product. Used to measure the execution. NULL means to convert the value from Quantity using the measurement ratios.|

## Columns

### Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Output_Order_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Line_Ord

| Property | Value |
| - | - |
|Type|int|

### Line_Work_Order_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Work_Order_Item_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Work_Order_Item_Operation_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Transaction_Timestamp

| Property | Value |
| - | - |
|Type|datetime|

### Product_Code_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Lot_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Workgroup_Resource_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Work_Done_By_Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### End_Time

| Property | Value |
| - | - |
|Type|datetime|

### Start_Time

| Property | Value |
| - | - |
|Type|datetime|

### Store_Bin_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Serial_Number_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|

### Store_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Produced_Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(18, 3)|

### Produced_Quantity_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Produced_Quantity

| Property | Value |
| - | - |
|Type|decimal(18, 3)|

### Begin_Date_Time

| Property | Value |
| - | - |
|Type|datetime|

### Product_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Finished

| Property | Value |
| - | - |
|Type|bit|

### Produced_Standard_Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(18, 3)|


