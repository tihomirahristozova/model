# Table Dw_Data_Measure_Groups

Contains the groups of measures in the general data warehouse. Entity: Dw_Data_Measure_Groups (Introduced in version 18.2)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Data_Measure_Group_Id](#data_measure_group_id)|`uniqueidentifier` `PK`||
|[Parent_Data_Measure_Group_Id](#parent_data_measure_group_id)|`uniqueidentifier` |Parent data measure group in the hierarchy. Null when this is root node.|
|[Data_Measure_Group_Code](#data_measure_group_code)|`nvarchar(16)` |Unique group code.|
|[Data_Measure_Group_Name](#data_measure_group_name)|`nvarchar(254)` |Group name (multilanguage).|
|[Notes](#notes)|`nvarchar(2147483647)` ||

## Columns

### Data_Measure_Group_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Parent_Data_Measure_Group_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Data_Measure_Group_Code

| Property | Value |
| - | - |
|Type|nvarchar(16)|

### Data_Measure_Group_Name

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|


