# Table Inv_Store_Responsible_Parties

Contains the list of responsible parties (usually persons) for the stores. Stores can have multiple responsible parties. Entity: Inv_Store_Responsible_Parties

## Owner Tables Hierarchy

* [Inv_Stores](Inv_Stores.md)
* [Gen_Parties](Gen_Parties.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Store_Responsible_Party_Id](#store_responsible_party_id)|`uniqueidentifier` `PK`||
|[Store_Id](#store_id)|`uniqueidentifier` |The store for which we specify the responsible party.|
|[Responsible_Party_Id](#responsible_party_id)|`uniqueidentifier` |The responsible party (usually employee) of the store.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Store_Responsible_Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Store_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Responsible_Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


