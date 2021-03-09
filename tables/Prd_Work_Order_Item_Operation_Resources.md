# Table Prd_Work_Order_Item_Operation_Resources


## Owner Tables Hierarchy

* [Prd_Work_Order_Item_Operations](Prd_Work_Order_Item_Operations.md)
* [Prd_Work_Order_Items](Prd_Work_Order_Items.md)
* [Prd_Work_Orders](Prd_Work_Orders.md)
* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Id](#id)|`uniqueidentifier` `PK`||
|[Work_Order_Item_Operation_Id](#work_order_item_operation_id)|`uniqueidentifier` |The work order item operation, containing the line.|
|[Function_Id](#function_id)|`uniqueidentifier` |Specifies the function, that the resource must be able to perform. This helps the selection of specific resource for the operation. This column is used as search/selection criteria. NULL means that the user must select the resource through all resources|
|[Resource_Id](#resource_id)|`uniqueidentifier` |A resource that will be utilized for this routing step|
|[Workgroup_Resource_Id](#workgroup_resource_id)|`uniqueidentifier` |The workgroup resource that is used for the operation|
|[Locked_Quantity](#locked_quantity)|`decimal(18, 3)` |The quantity locked from the resource. The measurement unit is specified in Prd_Resources.|
|[Line_Ord](#line_ord)|`int` |The order of the line within the item.|
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

### Function_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Resource_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Workgroup_Resource_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Locked_Quantity

| Property | Value |
| - | - |
|Type|decimal(18, 3)|

### Line_Ord

| Property | Value |
| - | - |
|Type|int|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


