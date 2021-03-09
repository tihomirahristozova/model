# Table Prd_Workgroups

Production workgroups. Entity: Prd_Workgroups

## Summary

| Name | Type | Description |
| - | - | --- |
|[Id](#id)|`uniqueidentifier` `PK`|Unique workgroup auto-generated Id|
|[Parent](#parent)|`nvarchar(255)` |Path-like parent workgroup name|
|[Workgroup_Name](#workgroup_name)|`nvarchar(64)` |Name of the workgroup|
|[Full_Path](#full_path)|`nvarchar(254)` |The full path to the current node, represented with slash ('/') as leading, trailing and separator character. Example: '/rootnode/subnode/'.|
|[Cost_Currency](#cost_currency)|`nvarchar(3)` ||
|[Notes](#notes)|`nvarchar(254)` |User notes for the workgroup|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Parent

| Property | Value |
| - | - |
|Type|nvarchar(255)|

### Workgroup_Name

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### Full_Path

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Cost_Currency

| Property | Value |
| - | - |
|Type|nvarchar(3)|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


