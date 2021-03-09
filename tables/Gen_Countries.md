# Table Gen_Countries

List of countries, listed by their internet suffix code. Entity: Gen_Countries

## Summary

| Name | Type | Description |
| - | - | --- |
|[Country_Id](#country_id)|`uniqueidentifier` `PK`|Unique country Id|
|[Code](#code)|`nvarchar(2)` |Internet suffix code of the country|
|[Country_Name](#country_name)|`nvarchar(254)` `ML`|Name of the country|
|[Row_Version](#row_version)|`timestamp` ||
|[Intrastat_Code](#intrastat_code)|`nvarchar(2)` |This code is used when creating the Intrastat Declaration. If the field is empty, then the value from the 'Code' field is used.|

## Columns

### Country_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Code

| Property | Value |
| - | - |
|Type|nvarchar(2)|

### Country_Name

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|

### Intrastat_Code

| Property | Value |
| - | - |
|Type|nvarchar(2)|


