# Table Cm_Activity_Resources

Contains the resources, allocated to the activities. Entity: Cm_Activity_Resources

## Owner Tables Hierarchy

* [Cm_Activities](Cm_Activities.md)
* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Activity_Resource_Id](#activity_resource_id)|`uniqueidentifier` `PK`||
|[Activity_Id](#activity_id)|`uniqueidentifier` ||
|[Resource_Id](#resource_id)|`uniqueidentifier` |The resource, which is required by the activity.|
|[Resource_Usage_Percent](#resource_usage_percent)|`decimal(18, 4)` |The planned resource usage for this activity in percents (100% = 1). Values of more than 100% are allowed when more than 1 resource is required.|
|[Notes](#notes)|`nvarchar(255)` ||
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Activity_Resource_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Activity_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Resource_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Resource_Usage_Percent

| Property | Value |
| - | - |
|Type|decimal(18, 4)|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(255)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


