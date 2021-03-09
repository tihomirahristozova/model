# Table Sys_Object_Changesets

A set of changes, performed in one request. Entity: Sys_Object_Changesets (Introduced in version 19.1)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Object_Changeset_Id](#object_changeset_id)|`uniqueidentifier` `PK`||
|[Time_Utc](#time_utc)|`datetime` |Date and time (in Utc) when the changeset was processed by the server.|
|[User_Id](#user_id)|`uniqueidentifier` |The user which initiated the change. NULL when it is unknown.|
|[Application_Name](#application_name)|`nvarchar(2147483647)` |The application which requested the change. NULL when it is unknown.|
|[Server_Version](#server_version)|`nvarchar(16)` |The version of the application server at the time of the change.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Object_Changeset_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Time_Utc

| Property | Value |
| - | - |
|Type|datetime|

### User_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Application_Name

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Server_Version

| Property | Value |
| - | - |
|Type|nvarchar(16)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


