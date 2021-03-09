# Table Sec_Visual_Permissions

Contains permissions, which are honored only by client applications and are used to provide access to (primarily show/hide) different elements of the user interface. Entity: Sec_Visual_Permissions

## Summary

| Name | Type | Description |
| - | - | --- |
|[Visual_Permission_Id](#visual_permission_id)|`uniqueidentifier` `PK`||
|[Application_Name](#application_name)|`nvarchar(64)` |The application for which the permission is specified|
|[Form_Name](#form_name)|`nvarchar(128)` |Optionally, the form which will be secured|
|[Panel_Name](#panel_name)|`nvarchar(128)` |Optionally, the panel from the form which will be secured|
|[Element_Name](#element_name)|`nvarchar(4000)` |Optionally, the element from the panel which will be secured|
|[Operation_Name](#operation_name)|`nvarchar(64)` |Optionally, the operation on the element which will be secured|
|[Access_Key_Id](#access_key_id)|`uniqueidentifier` |The security access key which controls the access to the visual permission|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Visual_Permission_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Application_Name

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### Form_Name

| Property | Value |
| - | - |
|Type|nvarchar(128)|

### Panel_Name

| Property | Value |
| - | - |
|Type|nvarchar(128)|

### Element_Name

| Property | Value |
| - | - |
|Type|nvarchar(4000)|

### Operation_Name

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### Access_Key_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


