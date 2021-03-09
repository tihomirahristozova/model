# Table Prd_Operation_Instructions

Long (full) instructions for performing an operation. The operations point to the instructions and one instruction can be used for different operations. Entity: Prd_Operation_Instructions

## Summary

| Name | Type | Description |
| - | - | --- |
|[Id](#id)|`uniqueidentifier` `PK`||
|[Instructions](#instructions)|`varbinary` |The operation instructions in OLE format|
|[Description](#description)|`nvarchar(254)` |Short description or notes for the instructions.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Instructions

| Property | Value |
| - | - |
|Type|varbinary|

### Description

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


