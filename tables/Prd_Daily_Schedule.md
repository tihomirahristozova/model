# Table Prd_Daily_Schedule


## Summary

| Name | Type | Description |
| - | - | --- |
|[Id](#id)|`uniqueidentifier` `PK`||
|[Work_Order_Item_Operation_Id](#work_order_item_operation_id)|`uniqueidentifier` ||
|[Calendar_Date](#calendar_date)|`datetime` ||
|[Workgroup_Resource_Id](#workgroup_resource_id)|`uniqueidentifier` ||
|[Usage_Start_Time](#usage_start_time)|`datetime` |Time of day when the operation is expected to start utilising the resource|
|[Usage_End_Time](#usage_end_time)|`datetime` |Time of day when the operation is expected to cease utilising the resource|
|[Usage_Quantity](#usage_quantity)|`decimal(9, 0)` |Quantity of the resource, which will be used for production|
|[Time_Type](#time_type)|`nvarchar(1)` |S=Setup; R=Run; W=Wait; M=Move|
|[Priority](#priority)|`smallint` |Priority of the allocation. 1=Lowest ... 5=Highest|
|[Notes](#notes)|`nvarchar(254)` ||
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

### Time_Type

| Property | Value |
| - | - |
|Type|nvarchar(1)|

### Priority

| Property | Value |
| - | - |
|Type|smallint|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


