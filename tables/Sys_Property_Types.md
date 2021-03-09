# Table Sys_Property_Types


## Summary

| Name | Type | Description |
| - | - | --- |
|[Property_Id](#property_id)|`uniqueidentifier` |Unique Id of the property|
|[Entity_Name](#entity_name)|`nvarchar(64)` `PK`|The system entity containing the objects|
|[Property_Name](#property_name)|`nvarchar(64)` `PK`||
|[Domain_Id](#domain_id)|`uniqueidentifier` |Domain of allowed values for this property|
|[Multi_Valued](#multi_valued)|`bit` |1 - allow multiple values (with different Seq_No's in the values). 0 - allow single value only (Seq_No=1)|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Property_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Entity_Name

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### Property_Name

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### Domain_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Multi_Valued

| Property | Value |
| - | - |
|Type|bit|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


