# Table Sys_Form_Layouts

Contains user layouts of the screen forms. Entity: Sys_Form_Layouts

## Summary

| Name | Type | Description |
| - | - | --- |
|[Form_Layout_Id](#form_layout_id)|`uniqueidentifier` `PK`||
|[Application_Name](#application_name)|`nvarchar(64)` |The application, which consumes the layout.|
|[Form_Name](#form_name)|`nvarchar(64)` |The form, for which the layout is applied.|
|[Layout_Name](#layout_name)|`nvarchar(64)` |The name of a named layout. Standard layouts have empty string names.|
|[User_Name](#user_name)|`nvarchar(64)` |The user for which the layout is applied. NULL means that the layout is applied for all users.|
|[Machine_Name](#machine_name)|`nvarchar(128)` ||
|[Panel_Name](#panel_name)|`nvarchar(64)` |The visual panel, for which the layout is applied.|
|[Layout_Xml](#layout_xml)|`nvarchar(1073741823)` ||
|[Access_Key_Id](#access_key_id)|`uniqueidentifier` |The security access key which controls the access to the layout view|
|[Layout](#layout)|`varbinary` |The byte storage of the layout.|
|[Layout_Format](#layout_format)|`nvarchar(1)` Allowed: `D`, `L`, `U`|The format of the data in the Layout column. Values can be: 'U' - uncompressed; 'L' - LZO compressed; 'D' - Deflate compressed.|
|[Role_Id](#role_id)|`uniqueidentifier` |The role, for which the layout is applied.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Form_Layout_Id

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
|Type|nvarchar(64)|

### Layout_Name

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### User_Name

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### Machine_Name

| Property | Value |
| - | - |
|Type|nvarchar(128)|

### Panel_Name

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### Layout_Xml

| Property | Value |
| - | - |
|Type|nvarchar(1073741823)|

### Access_Key_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Layout

| Property | Value |
| - | - |
|Type|varbinary|

### Layout_Format

| Property | Value |
| - | - |
|Type|nvarchar(1)|

### Role_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


