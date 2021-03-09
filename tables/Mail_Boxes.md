# Table Mail_Boxes

Represents user mailboxes. Entity: Mail_Boxes

## Summary

| Name | Type | Description |
| - | - | --- |
|[Mail_Box_Id](#mail_box_id)|`uniqueidentifier` `PK`||
|[Owner_User_Id](#owner_user_id)|`uniqueidentifier` |The user, who owns the mailbox|
|[Email_Address](#email_address)|`nvarchar(254)` |The email address associated with this mail box|
|[Sync_Protocol](#sync_protocol)|`nvarchar(4)` Allowed: `IMAP`, `POP3`, `MEWS`|Synchronization protocol, 'POP3' or 'IMAP'. NULL means that syncrhonization is not setup|
|[Sync_Server_Address](#sync_server_address)|`nvarchar(254)` |Incoming and outgoing mail server internet address. NULL when synchronization is not setup|
|[Sync_User_Name](#sync_user_name)|`nvarchar(64)` |User name to supply to the server, when retrieving email. NULL when the connection is not setup or the server does not require user name|
|[Sync_Password](#sync_password)|`nvarchar(512)` |The password to supply to the server when retrieving email. NULL when the connection is not setup or the server does not require user name|
|[Active](#active)|`bit` |1 when the mail box is active for mail sinchronization, sending and receiving|
|[Send_Server_Address](#send_server_address)|`nvarchar(254)` |The address of the server to use for sending mail. The same credentials as the sync server are used. When NULL, the mail will be sent using the default server, which is setup at the application server|
|[Is_Default](#is_default)|`bit` |1 when this is the default mailbox for the user.|
|[Is_Encrypted](#is_encrypted)|`bit` |1 when the mailbox messages are stored in encrypted format|
|[Reset_On_Next_Sync](#reset_on_next_sync)|`bit` Readonly|Reset is pending: 1 = next sync should delete and retrieve again all messages; 0 = no pending reset|
|[Signature_Html](#signature_html)|`nvarchar(2147483647)` |Html text of the default signature, when creating new emails from this mailbox. When is NULL, a default generic signature is attached|
|[Sent_Items_Folder_Name](#sent_items_folder_name)|`nvarchar(254)` |The name of the SentItems folder. It is left empty, EnterpriseOne won't save the sent mail in any folder (but it is still possible that the actual mail server would nevertheless save the mail in a sent items folder, independently from EnterpriseOne).|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Mail_Box_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Owner_User_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Email_Address

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Sync_Protocol

| Property | Value |
| - | - |
|Type|nvarchar(4)|

### Sync_Server_Address

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Sync_User_Name

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### Sync_Password

| Property | Value |
| - | - |
|Type|nvarchar(512)|

### Active

| Property | Value |
| - | - |
|Type|bit|

### Send_Server_Address

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Is_Default

| Property | Value |
| - | - |
|Type|bit|

### Is_Encrypted

| Property | Value |
| - | - |
|Type|bit|

### Reset_On_Next_Sync

| Property | Value |
| - | - |
|Type|bit|

### Signature_Html

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Sent_Items_Folder_Name

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


