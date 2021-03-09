# Table Cost_Template_Levels

Represents named hierarchy levels within a cost calculation. The hierarchy levels are used to specify cost allocation mechanisms. Entity: Cost_Template_Levels

## Owner Tables Hierarchy

* [Cost_Templates](Cost_Templates.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Cost_Template_Level_Id](#cost_template_level_id)|`uniqueidentifier` `PK`||
|[Cost_Template_Id](#cost_template_id)|`uniqueidentifier` ||
|[Hierarchy_Level](#hierarchy_level)|`int` |The level within the hierarchy 0=Root, 1=one level below root, etc. (0..9)|
|[Level_Name](#level_name)|`nvarchar(254)` |The name of the hierarchy level.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Cost_Template_Level_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Cost_Template_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Hierarchy_Level

| Property | Value |
| - | - |
|Type|int|

### Level_Name

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


