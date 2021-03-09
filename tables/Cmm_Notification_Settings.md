# Table Cmm_Notification_Settings

User notification settings for the different notification classes. Entity: Cmm_Notification_Settings (Introduced in version 20.1)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Notification_Setting_Id](#notification_setting_id)|`uniqueidentifier` `PK`||
|[User_Id](#user_id)|`uniqueidentifier` |The user for whom the notification setting is about.|
|[Notification_Class](#notification_class)|`nvarchar(64)` |The class of the notification, for which the user is specifying settings. When NULL, the setting is applied to all notification classes.|
|[Receive_Notification](#receive_notification)|`bit` |True if the user should receive internal notification.|
|[Receive_Mail](#receive_mail)|`bit` |True if the user should receive mail.|
|[Receive_Sms](#receive_sms)|`bit` |True if the user should receive SMS.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Notification_Setting_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### User_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Notification_Class

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### Receive_Notification

| Property | Value |
| - | - |
|Type|bit|

### Receive_Mail

| Property | Value |
| - | - |
|Type|bit|

### Receive_Sms

| Property | Value |
| - | - |
|Type|bit|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


