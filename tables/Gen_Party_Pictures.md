# Table Gen_Party_Pictures

Party pictures - photos, logos, etc. Entity: Gen_Party_Pictures

## Owner Tables Hierarchy

* [Gen_Parties](Gen_Parties.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Picture_No](#picture_no)|`int` |Unique picture number within the party. Also used for sorting|
|[Party_Id](#party_id)|`uniqueidentifier` ||
|[Comments](#comments)|`nvarchar(254)` |Notes for this party picture.|
|[Is_Default](#is_default)|`bit` |1=This is the default picture for the party; 0=otherwise|
|[Picture](#picture)|`varbinary` |The actual party picture data. Can be NULL if we insert only some comments.|
|[Party_Picture_Id](#party_picture_id)|`uniqueidentifier` `PK`||
|[Is_Logo](#is_logo)|`bit` ||
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Picture_No

| Property | Value |
| - | - |
|Type|int|

### Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Comments

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Is_Default

| Property | Value |
| - | - |
|Type|bit|

### Picture

| Property | Value |
| - | - |
|Type|varbinary|

### Party_Picture_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Is_Logo

| Property | Value |
| - | - |
|Type|bit|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


