# Table Wf_Processes

Contains the business process diagrams. Entity: Wf_Processes

## Summary

| Name | Type | Description |
| - | - | --- |
|[Process_Id](#process_id)|`uniqueidentifier` `PK`||
|[Process_Name](#process_name)|`nvarchar(128)` `ML`||
|[Schema_Layout](#schema_layout)|`nvarchar(2147483647)` |Contains the actual presentation layout of the business process. The layout is stored in the format, specified by Schema Format.|
|[Schema_Format](#schema_format)|`nvarchar(1)` |Application specific format of the Schema Layout.|
|[Thumbnail](#thumbnail)|`varbinary` |Contains the visual thumbnail of the presentation of the business process. It is stored in bitmap (BMP) format.|
|[Creation_Time](#creation_time)|`datetime` Readonly||
|[Creation_User](#creation_user)|`nvarchar(64)` Readonly||
|[Update_Time](#update_time)|`datetime` Readonly||
|[Update_User](#update_user)|`nvarchar(64)` Readonly||
|[Notes](#notes)|`nvarchar(2000)` ||
|[Is_Landscape](#is_landscape)|`bit` |Specifies whether the process diagram is intended to be viewed in landscape mode.|
|[Start_Event](#start_event)|`nvarchar(3)` |USR=User created; EML=Email receive (still not supported). NULL means that there is no starting event for this process|
|[Start_Role_Id](#start_role_id)|`uniqueidentifier` |When Start_Event='USR' then specifies the role which the user must play in order to start the process. NULL when Start_Event<>'USR'|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Process_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Process_Name

| Property | Value |
| - | - |
|Type|nvarchar(128)|

### Schema_Layout

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Schema_Format

| Property | Value |
| - | - |
|Type|nvarchar(1)|

### Thumbnail

| Property | Value |
| - | - |
|Type|varbinary|

### Creation_Time

| Property | Value |
| - | - |
|Type|datetime|

### Creation_User

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### Update_Time

| Property | Value |
| - | - |
|Type|datetime|

### Update_User

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(2000)|

### Is_Landscape

| Property | Value |
| - | - |
|Type|bit|

### Start_Event

| Property | Value |
| - | - |
|Type|nvarchar(3)|

### Start_Role_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


