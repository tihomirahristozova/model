# Table Prd_Load

Contains scheduled operations usage of the resources. Entity: Prd_Load

## Owner Tables Hierarchy

* [Prd_Work_Order_Item_Operations](Prd_Work_Order_Item_Operations.md)
* [Prd_Work_Order_Items](Prd_Work_Order_Items.md)
* [Prd_Work_Orders](Prd_Work_Orders.md)
* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Id](#id)|`uniqueidentifier` `PK`||
|[Work_Order_Item_Operation_Id](#work_order_item_operation_id)|`uniqueidentifier` ||
|[Calendar_Date](#calendar_date)|`datetime` |Date of the scheduled load. This is date only. Start_Time and End_Time specify time of day|
|[Workgroup_Resource_Id](#workgroup_resource_id)|`uniqueidentifier` |The exact resource being utilised|
|[Usage_Start_Time](#usage_start_time)|`datetime` |The starting time of the planned usage.|
|[Usage_End_Time](#usage_end_time)|`datetime` |The ending time of the planned usage.|
|[Usage_Quantity](#usage_quantity)|`decimal(9, 0)` |Quantity of the resource, which will be used for production|
|[Usage_Time_Minutes](#usage_time_minutes)|`int` |Time allocated for the operation in minutes|
|[Time_Type](#time_type)|`nvarchar(1)` Allowed: `M`, `R`, `S`, `W`|S=Setup; R=Run; W=Wait; M=Move|
|[Priority](#priority)|`smallint` Allowed: `1`, `2`, `3`, `4`, `5`|Priority of the allocation. 1=Lowest ... 5=Highest|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Work_Order_Item_Operation_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Calendar_Date

| Property | Value |
| - | - |
|Type|datetime|

### Workgroup_Resource_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Usage_Start_Time

| Property | Value |
| - | - |
|Type|datetime|

### Usage_End_Time

| Property | Value |
| - | - |
|Type|datetime|

### Usage_Quantity

| Property | Value |
| - | - |
|Type|decimal(9, 0)|

### Usage_Time_Minutes

| Property | Value |
| - | - |
|Type|int|

### Time_Type

| Property | Value |
| - | - |
|Type|nvarchar(1)|

### Priority

| Property | Value |
| - | - |
|Type|smallint|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


