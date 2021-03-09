# Query Sys_Information_Messages_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Information_Message_Id](#information_message_id)|`uniqueidentifier` `PK`||
|[Information_Message_Type](#information_message_type)|`nvarchar` Allowed: `INF`, `WRN`, `ERR`, Readonly|Type of the information message: 'INF' = Information, 'WRN' = Warning, Error = 'ERR'|
|[Information_Message_Time](#information_message_time)|`datetime` Readonly|Date and time when thet message occurred.|
|[User_Name](#user_name)|`nvarchar` Readonly|Login name of the user that has initiated the process which creates the message.|
|[Machine_Name](#machine_name)|`nvarchar` Readonly|Machine name of the computer from which the process which creates the message has been initiated.|
|[Process_Description](#process_description)|`nvarchar` Readonly|Name or description of the process that creates the message.|
|[Message](#message)|`nvarchar` Readonly|The actual content of the information message.|
|[URL](#url)|`nvarchar` ||
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Information_Message_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Information_Message_Type

| Property | Value |
| - | - |
|Type|nvarchar|

### Information_Message_Time

| Property | Value |
| - | - |
|Type|datetime|

### User_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Machine_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Process_Description

| Property | Value |
| - | - |
|Type|nvarchar|

### Message

| Property | Value |
| - | - |
|Type|nvarchar|

### URL

| Property | Value |
| - | - |
|Type|nvarchar|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


