# Table Inv_Scrap_Types

Types of scrap. Used in store transactions to categorize scrap, when it occurs. Entity: Inv_Scrap_Types

## Summary

| Name | Type | Description |
| - | - | --- |
|[Scrap_Type_Id](#scrap_type_id)|`uniqueidentifier` `PK`||
|[Description](#description)|`nvarchar(254)` ||
|[Is_Planned](#is_planned)|`bit` |1=Planned (expected) scrap. Scrap of this type will be used to refine planned scrap for future operations. 2=Unexpected scrap|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Scrap_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Description

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Is_Planned

| Property | Value |
| - | - |
|Type|bit|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


