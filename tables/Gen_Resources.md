# Table Gen_Resources

Enterprise resources, categorized by groups. Entity: Gen_Resources

## Owner Tables Hierarchy

* [Gen_Resource_Groups](Gen_Resource_Groups.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Resource_Id](#resource_id)|`uniqueidentifier` `PK`||
|[Resource_Name](#resource_name)|`nvarchar(254)` `ML`|Resource name. Unique within the resource group|
|[Resource_Group_Id](#resource_group_id)|`uniqueidentifier` ||
|[Notes](#notes)|`nvarchar(2147483647)` ||
|[Costing_Currency_Id](#costing_currency_id)|`uniqueidentifier` |The currency in which resource costs are specified. Required only if resource costs will be specified.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Resource_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Resource_Name

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Resource_Group_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Costing_Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


