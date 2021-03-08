# Table Mail_Boxes

Represents user mailboxes. Entity: Mail_Boxes

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Mail_Box_Id|`Guid`|`PK`, Readonly||
|Active|`Boolean`||True when the mail box is active for mail sinchronization, sending and receiving. `Required` `Default(true)` `Filter(eq)` |
|Email_Address|`String`||The email address associated with this mail box. `Required` `Filter(eq)` |
|Is_Default|`Boolean`||True when this is the default mailbox for the user. `Required` `Default(true)` `Filter(eq)` |
|Is_Encrypted|`Boolean`||True when the mailbox messages are stored in encrypted format. `Required` `Default(false)` `Filter(eq)` |
|Reset_On_Next_Sync|`Boolean`|Readonly|Reset is pending: true = next sync should delete and retrieve again all messages; false = no pending reset. `Required` `Default(false)` `Filter(eq)` `ReadOnly` |
|Send_Server_Address|`String`||The address of the server to use for sending mail. The same credentials as the sync server are used. When null, the mail will be sent using the default server, which is setup at the application server. |
|Sent_Items_Folder_Name|`String`||The name of the SentItems folder. It is left empty, EnterpriseOne won't save the sent mail in any folder (but it is still possible that the actual mail server would nevertheless save the mail in a sent items folder, independently from EnterpriseOne). |
|Signature_Html|`String`||Html text of the default signature, when creating new emails from this mailbox. When is null, a default generic signature is attached. |
|Sync_Password|`String`||The password to supply to the server when retrieving email. null when the connection is not setup or the server does not require user name. |
|Sync_Protocol|`SyncProtocol?`|Allowed: `IMAP`, `POP3`, `MEWS`|Synchronization protocol, 'POP3' or 'IMAP'. null means that syncrhonization is not setup. |
|Sync_Server_Address|`String`||Incoming and outgoing mail server internet address. null when synchronization is not setup. |
|Sync_User_Name|`String`||User name to supply to the server, when retrieving email. null when the connection is not setup or the server does not require user name. |
