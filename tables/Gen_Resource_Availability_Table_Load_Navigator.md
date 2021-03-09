# Query Gen_Resource_Availability_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Resource_Availability_Id](#resource_availability_id)|`uniqueidentifier` `PK`||
|[Resource_Id](#resource_id)|`uniqueidentifier` |The resource, for which we provide availability.|
|[From_Date](#from_date)|`date` |The date from which availability starts.|
|[To_Date](#to_date)|`date` |The date to which the availability continues. When NULL, the availability continues infinitely.|
|[Available_Resources](#available_resources)|`decimal(0, 0)` |The quantity of the resource, available for the specified period. For non-discrete resources, this number can contain fractions. When several availability periods for a resource overlap, the total availability is the sum of all.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Resource_Availability_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Resource_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### From_Date

| Property | Value |
| - | - |
|Type|date|

### To_Date

| Property | Value |
| - | - |
|Type|date|

### Available_Resources

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


