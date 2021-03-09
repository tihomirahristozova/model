# Query Cmm_Notifications_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Notification_Id](#notification_id)|`uniqueidentifier` `PK`||
|[User_Id](#user_id)|`uniqueidentifier` |The user, who is notified.|
|[Data_Object_Id](#data_object_id)|`uniqueidentifier` |The data object about which the notification is created. Null means that the notification is not about any specific data object.|
|[Creation_Time_Utc](#creation_time_utc)|`datetime` |The exact server time (in UTC), when the notification was created.|
|[Notification_Class](#notification_class)|`nvarchar` |The class of the notification from a predefined list of system classes.|
|[Subject](#subject)|`nvarchar` |The short subject of the notification (in the Default Culture of the user).|
|[Is_Read](#is_read)|`bit` |Specifies whether the user has read the notification. If the system changes the notification after first reading, the flag is reset to unread again.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Notification_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### User_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Data_Object_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Creation_Time_Utc

| Property | Value |
| - | - |
|Type|datetime|

### Notification_Class

| Property | Value |
| - | - |
|Type|nvarchar|

### Subject

| Property | Value |
| - | - |
|Type|nvarchar|

### Is_Read

| Property | Value |
| - | - |
|Type|bit|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


