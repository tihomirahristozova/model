# Table Inv_Store_Bins

The storage locations within a store. If there are no differentiated storage locations, create only one, called “(Default)” or similar. Entity: Inv_Store_Bins

## Owner Tables Hierarchy

* [Inv_Stores](Inv_Stores.md)
* [Gen_Parties](Gen_Parties.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Id](#id)|`uniqueidentifier` `PK`|Unique store bin id|
|[Store_Id](#store_id)|`uniqueidentifier` |The id of the containing store|
|[Store_Bin_Name](#store_bin_name)|`nvarchar(254)` |Name of the store bin|
|[Blocked_For_Party_Id](#blocked_for_party_id)|`uniqueidentifier` |If not NULL, the goods can only be used by the specified party|
|[Is_Default](#is_default)|`bit` |True, when this is the default storage bin for the specified store.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Store_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Store_Bin_Name

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Blocked_For_Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Is_Default

| Property | Value |
| - | - |
|Type|bit|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


