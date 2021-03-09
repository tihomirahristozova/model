# Table Gen_Measurement_Categories

Categories of measurement units. The units within a category are directly convertable to each other. Each category contains one base unit and unlimited number of derived units with fixed ratio to the base unit. Entity: Gen_Measurement_Categories

## Summary

| Name | Type | Description |
| - | - | --- |
|[Id](#id)|`uniqueidentifier` `PK`|Unique measurement category Id|
|[Measurement_Category_Name](#measurement_category_name)|`nvarchar(64)` `ML`||
|[Is_Default](#is_default)|`bit` |1=This category is the default category; 0=otherwise|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Measurement_Category_Name

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### Is_Default

| Property | Value |
| - | - |
|Type|bit|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


