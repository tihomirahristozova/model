# Table Sys_Reference_Types


## Summary

| Name | Type | Description |
| - | - | --- |
|[Reference_Type_Id](#reference_type_id)|`uniqueidentifier` `PK`|Unique Id of the reference property|
|[Entity_Name](#entity_name)|`nvarchar(64)` |The system entity containing the objects|
|[Reference_Name](#reference_name)|`nvarchar(64)` |The name of the reference property|
|[Multi_Valued](#multi_valued)|`bit` |1 - allow multiple values (with different Seq_No's in the values). 0 - allow single value only (Seq_No=1)|
|[Referenced_Object_Class_Name](#referenced_object_class_name)|`nvarchar(64)` |The name of the referenced object class|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Reference_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Entity_Name

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### Reference_Name

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### Multi_Valued

| Property | Value |
| - | - |
|Type|bit|

### Referenced_Object_Class_Name

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


