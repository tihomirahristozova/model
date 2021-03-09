# Table Prd_Work_Orders

Scheduled and released production orders. Each order can contain the production of many items. Entity: Prd_Work_Orders

## Owner Tables Hierarchy

* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Id](#id)|`uniqueidentifier` `PK`||
|[Document_Id](#document_id)|`uniqueidentifier` |Document Id for the released production orders. NULL for orders that are not yet released|
|[Workgroup_Id](#workgroup_id)|`uniqueidentifier` |The workgroup which performs the operations|
|[Due_Date](#due_date)|`datetime` |The final due date, when the production should be ready.|
|[Release_Date](#release_date)|`datetime` |Scheduled release date. Specifies the date when the order is planned/released to production. NULL means that still there is no plan for releasing the order.|
|[Completion_Date](#completion_date)|`datetime` |Scheduled date of completion. Specifies the date when the workorder was completed. NULL means that the order is not yet completed.|
|[Duration_Hour](#duration_hour)|`decimal(10, 0)` |The duration of all operations in the protocol either planned (for planned orders) or actual (for completed orders)|
|[Notes](#notes)|`nvarchar(2147483647)` |User notes for the production order|
|[Priority](#priority)|`smallint` Allowed: `1`, `2`, `3`, `4`, `5`|Priority of the work order. Higher priority orders might seize resources from lower priority orders. 1=Lowest priority ... 5=Highest|
|[Default_Output_Store_Id](#default_output_store_id)|`uniqueidentifier` |Default output store for the finished products|
|[Default_Materials_Store_Id](#default_materials_store_id)|`uniqueidentifier` |Default materials store for the ingredients|
|[Is_Single_Execution](#is_single_execution)|`bit` Readonly|Specifies whether the document is a single execution of its order document.|
|[Is_Released](#is_released)|`bit` Readonly|True if the document is not void and its state is released or greater|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Workgroup_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Due_Date

| Property | Value |
| - | - |
|Type|datetime|

### Release_Date

| Property | Value |
| - | - |
|Type|datetime|

### Completion_Date

| Property | Value |
| - | - |
|Type|datetime|

### Duration_Hour

| Property | Value |
| - | - |
|Type|decimal(10, 0)|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Priority

| Property | Value |
| - | - |
|Type|smallint|

### Default_Output_Store_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Default_Materials_Store_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Is_Single_Execution

| Property | Value |
| - | - |
|Type|bit|

### Is_Released

| Property | Value |
| - | - |
|Type|bit|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


