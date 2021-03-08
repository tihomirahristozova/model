# Table Mail_Messages

Represents email messages. Entity: Mail_Messages

# Aggregate Hierarchy

* [Mail_Box_Folders](Mail_Box_Folders.md)
* [Mail_Boxes](Mail_Boxes.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Mail_Message_Id|`Guid`|`PK`, Readonly||
|Body|`String`||The body of the message. |
|Cc_Email_Address_List|`String`||Semicolon-separated list of Cc email addresses. `Filter(like)` |
|Creation_Date_Time|`DateTime`||Date and time when the message was created. `Required` `Default(Now)` `Filter(ge;le)` |
|From_Email_Address|`String`||Sending email address. `Required` `Filter(like)` |
|Is_Encrypted|`Boolean`||True when the message is stored in encrypted format. `Required` `Default(false)` `Filter(eq)` |
|Is_Read|`Boolean`||True when the message was read by the user. `Required` `Default(false)` `Filter(eq)` |
|Received_Date_Time|`DateTime?`||Date and time when the message was received. `Filter(ge;le)` |
|Sent_Date_Time|`DateTime?`||Date and time when the message was sent. `Filter(ge;le)` |
|Server_Message_ID|`String`||Message ID as it appears on the mail server. `Filter(eq)` |
|Subject|`String`||The message subject. `Filter(like)` |
|To_Email_Address_List|`String`||Semicolon-separated list of receiving email addresses. `Filter(like)` |
