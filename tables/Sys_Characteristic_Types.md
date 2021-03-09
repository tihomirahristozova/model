# Table Sys_Characteristic_Types


## Summary

| Name | Type | Description |
| - | - | --- |
|[Id](#id)|`uniqueidentifier` `PK`|Unique Id of the string property|
|[Entity_Name](#entity_name)|`nvarchar(64)` |The system entity containing the objects|
|[Characterstic_Name](#characterstic_name)|`nvarchar(64)` |The name of the string property|
|[Multi_Valued](#multi_valued)|`bit` |1 - allow multiple values (with different Seq_No's in the values). 0 - allow single value only (Seq_No=1)|
|[Default_Value](#default_value)|`nvarchar(64)` |Default value of this property. Nulls means that the property does not have default value|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Entity_Name

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### Characterstic_Name

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### Multi_Valued

| Property | Value |
| - | - |
|Type|bit|

### Default_Value

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


