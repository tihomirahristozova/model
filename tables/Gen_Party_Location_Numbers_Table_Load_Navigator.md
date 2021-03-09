# Query Gen_Party_Location_Numbers_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Party_Location_Number_Id](#party_location_number_id)|`uniqueidentifier` `PK`||
|[Party_Id](#party_id)|`uniqueidentifier` |The party for which we are defining the location number.|
|[Partner_Party_Id](#partner_party_id)|`uniqueidentifier` |The party with which we are doing exchange. Depending on the Partner Party, the main Party might have different location number. NULL means that the location number is not dependent on the Partner Party.|
|[Partner_Location_Number](#partner_location_number)|`nvarchar` |The location number of the partner party for which we define the main Party location number. The location number of the main Party might be different depending on the location number of the partner party. NULL means that the location number is not dependent on the partner location number.|
|[Location_Coding_System](#location_coding_system)|`nvarchar` Allowed: `GLN`, `INT`|The coding system for which we are defining the location number.|
|[Location_Number](#location_number)|`nvarchar` |The location number of Party.|
|[Significance](#significance)|`int` |Order of significance of the location number within the main Party. If there are multiple location numbers, only the most significant is used. 0 is the least significant and higher numbers indicate higher significance.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Party_Location_Number_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Partner_Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Partner_Location_Number

| Property | Value |
| - | - |
|Type|nvarchar|

### Location_Coding_System

| Property | Value |
| - | - |
|Type|nvarchar|

### Location_Number

| Property | Value |
| - | - |
|Type|nvarchar|

### Significance

| Property | Value |
| - | - |
|Type|int|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


