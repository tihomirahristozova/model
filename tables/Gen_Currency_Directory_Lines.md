# Table Gen_Currency_Directory_Lines

Contains exchange rate for a currency against the main currency of currency directory. Entity: Gen_Currency_Directory_Lines

## Owner Tables Hierarchy

* [Gen_Currency_Directories](Gen_Currency_Directories.md)
* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Currency_Directory_Line_Id](#currency_directory_line_id)|`uniqueidentifier` `PK`||
|[Currency_Directory_Id](#currency_directory_id)|`uniqueidentifier` ||
|[From_Currency_Id](#from_currency_id)|`uniqueidentifier` |The currency for which the exchange rate is recorded|
|[Rate_Multiplier](#rate_multiplier)|`decimal(18, 6)` |The multiplier for conversion from From_Currency to Directory.To_Currency|
|[Rate_Divisor](#rate_divisor)|`decimal(18, 6)` |The divisor for conversion from From_Currency to Directory.To_Currency|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Currency_Directory_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Currency_Directory_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### From_Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Rate_Multiplier

| Property | Value |
| - | - |
|Type|decimal(18, 6)|

### Rate_Divisor

| Property | Value |
| - | - |
|Type|decimal(18, 6)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


