# Table Cmm_Notification_Settings

User notification settings for the different notification classes. Entity: Cmm_Notification_Settings (Introduced in version 20.1)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Notification_Setting_Id|`Guid`|`PK`, Readonly||
|Notification_Class|`String`||The class of the notification, for which the user is specifying settings. When null, the setting is applied to all notification classes. `Filter(multi eq)` |
|Receive_Mail|`Boolean`||True if the user should receive mail. `Required` `Default(false)` `Filter(eq)` |
|Receive_Notification|`Boolean`||True if the user should receive internal notification. `Required` `Default(true)` `Filter(eq)` |
|Receive_Sms|`Boolean`||True if the user should receive SMS. `Required` `Default(false)` `Filter(eq)` |
