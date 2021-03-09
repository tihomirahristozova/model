# Table Gen_Administrative_Regions

Hierarchical structure of the legally defined administrative regions. Administrative regions are sub-divisions of the countries. Entity: Gen_Administrative_Regions

## Summary

| Name | Type | Description |
| - | - | --- |
|[Administrative_Region_Id](#administrative_region_id)|`uniqueidentifier` `PK`||
|[Administrative_Region_Code](#administrative_region_code)|`nvarchar(16)` |Administrative code of country territorial subdivision|
|[Administrative_Region_Name](#administrative_region_name)|`nvarchar(254)` `ML`|Name of country territorial subdivision|
|[Parent_Full_Path](#parent_full_path)|`nvarchar(254)` |Parent region of the current territorial subdivision|
|[Full_Path](#full_path)|`nvarchar(254)` |Full identification path of the current country territorial subdivision|
|[Country_Id](#country_id)|`uniqueidentifier` |Country of the territorial subdivision|
|[Valid_From](#valid_from)|`date` |Start date of validity of this administrative division. NULL when the starting date is unknown in the past.|
|[Valid_To](#valid_to)|`date` |End date of validity of this administative division. NULL when the division is still active or ending date is unknown|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Administrative_Region_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Administrative_Region_Code

| Property | Value |
| - | - |
|Type|nvarchar(16)|

### Administrative_Region_Name

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Parent_Full_Path

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Full_Path

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Country_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Valid_From

| Property | Value |
| - | - |
|Type|date|

### Valid_To

| Property | Value |
| - | - |
|Type|date|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


