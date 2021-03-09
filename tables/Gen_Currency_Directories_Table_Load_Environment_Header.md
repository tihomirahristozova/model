# Procedure Gen_Currency_Directories_Table_Load_Environment_Header


## Summary

| Name | Type | Description |
| - | - | --- |
|[Currency_Directory_Id](#currency_directory_id)|`uniqueidentifier` `PK`||
|[Currency_Directory_Name](#currency_directory_name)|`nvarchar` |The name of the currency directory, used to distinguish it from the other directories on the same date|
|[Document_Id](#document_id)|`uniqueidentifier` ||
|[To_Currency_Id](#to_currency_id)|`uniqueidentifier` |The destination currency for the conversions for this directory|
|[Is_Valid](#is_valid)|`bit` |Shows if the current currency directory is valid to be used in documents|
|[Is_Default](#is_default)|`bit` ||
|[Is_Single_Execution](#is_single_execution)|`bit` ||
|[Is_Released](#is_released)|`bit` ||
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Currency_Directory_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Currency_Directory_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### To_Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Is_Valid

| Property | Value |
| - | - |
|Type|bit|

### Is_Default

| Property | Value |
| - | - |
|Type|bit|

### Is_Single_Execution

| Property | Value |
| - | - |
|Type|bit|

### Is_Released

| Property | Value |
| - | - |
|Type|bit|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


