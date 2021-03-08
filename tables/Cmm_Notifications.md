# Table Cmm_Notifications

A single notification of a user. Entity: Cmm_Notifications (Introduced in version 20.1)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Notification_Id|`Guid`|`PK`, Readonly||
|Creation_Time_Utc|`DateTime`|Readonly|The exact server time (in UTC), when the notification was created. `Required` `Default(NowUtc)` `Filter(ge;le)` `ORD` `ReadOnly` |
|Is_Read|`Boolean`||Specifies whether the user has read the notification. If the system changes the notification after first reading, the flag is reset to unread again. `Required` `Default(false)` `Filter(eq)` |
|Notification_Class|`String`||The class of the notification from a predefined list of system classes. `Required` `Filter(multi eq)` |
|Subject|`String`||The short subject of the notification (in the Default Culture of the user). `Filter(eq;like)` |
