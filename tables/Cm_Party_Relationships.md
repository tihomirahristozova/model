# Table Cm_Party_Relationships

Defines the relationships between the parties. The data is preserved over time. Entity: Cm_Party_Relationships

## Summary

| Name | Type | Description |
| - | - | --- |
|[Relationship_Id](#relationship_id)|`uniqueidentifier` `PK`||
|[From_Party_Id](#from_party_id)|`uniqueidentifier` |The first party in the relationship|
|[Relationship_Type_Id](#relationship_type_id)|`uniqueidentifier` |The type of the relationship|
|[To_Party_Id](#to_party_id)|`uniqueidentifier` |The second party in the relationship|
|[From_Date](#from_date)|`datetime` |The starting date of the relationship. NULL means the date is the begining of the time|
|[To_Date](#to_date)|`datetime` |The ending date of the relationship. NULL means the relationship is still active|
|[Notes](#notes)|`nvarchar(254)` ||
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Relationship_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### From_Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Relationship_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### To_Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### From_Date

| Property | Value |
| - | - |
|Type|datetime|

### To_Date

| Property | Value |
| - | - |
|Type|datetime|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


