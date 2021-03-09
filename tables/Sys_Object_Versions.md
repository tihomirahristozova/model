# Table Sys_Object_Versions

Contains history of saved version of the managed objects. Entity: Sys_Object_Versions

## Owner Tables Hierarchy

* [Sys_Objects](Sys_Objects.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Object_Version_Id](#object_version_id)|`uniqueidentifier` `PK`||
|[Object_Id](#object_id)|`uniqueidentifier` |The object, for which a version is stored.|
|[Version](#version)|`int` |The version number of the version, stored in the current row, starting from 1.|
|[User_Id](#user_id)|`uniqueidentifier` |The user, which saved the version.|
|[Version_Time](#version_time)|`datetime` |The timestamp when the version was saved.|
|[Object_Contents](#object_contents)|`varbinary` |The compressed contents of the object.|
|[Version_Type](#version_type)|`nvarchar(1)` Allowed: `C`, `U`|Specifies the action, which occurred on the actual object, referred by the system object.  'C' means that with this version the object was created. 'U' means that this is an update to an existing object.|
|[Server_Version](#server_version)|`nvarchar(15)` |The version of the EnterpriseOne server, which created the version. The version should be in the form (9.9.9.9). NULL means the version is unknown.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Object_Version_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Object_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Version

| Property | Value |
| - | - |
|Type|int|

### User_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Version_Time

| Property | Value |
| - | - |
|Type|datetime|

### Object_Contents

| Property | Value |
| - | - |
|Type|varbinary|

### Version_Type

| Property | Value |
| - | - |
|Type|nvarchar(1)|

### Server_Version

| Property | Value |
| - | - |
|Type|nvarchar(15)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


