# Query Mail_Boxes_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Mail_Box_Id](#mail_box_id)|`uniqueidentifier` `PK`||
|[Owner_User_Id](#owner_user_id)|`uniqueidentifier` ||
|[Email_Address](#email_address)|`nvarchar` ||
|[Sync_Protocol](#sync_protocol)|`nvarchar` Allowed: `IMAP`, `POP3`, `MEWS`||
|[Sync_Server_Address](#sync_server_address)|`nvarchar` ||
|[Sync_User_Name](#sync_user_name)|`nvarchar` ||
|[Active](#active)|`bit` ||
|[Send_Server_Address](#send_server_address)|`nvarchar` ||
|[Is_Default](#is_default)|`bit` ||
|[Is_Encrypted](#is_encrypted)|`bit` ||
|[Reset_On_Next_Sync](#reset_on_next_sync)|`bit` Readonly||
|[Signature_Html](#signature_html)|`nvarchar` ||
|[Sent_Items_Folder_Name](#sent_items_folder_name)|`nvarchar` |The name of the SentItems folder. It is left empty, EnterpriseOne won't save the sent mail in any folder (but it is still possible that the actual mail server would nevertheless save the mail in a sent items folder, independently from EnterpriseOne).|
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
|Type|nvarchar|

### Sync_Protocol

| Property | Value |
| - | - |
|Type|nvarchar|

### Sync_Server_Address

| Property | Value |
| - | - |
|Type|nvarchar|

### Sync_User_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Active

| Property | Value |
| - | - |
|Type|bit|

### Send_Server_Address

| Property | Value |
| - | - |
|Type|nvarchar|

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
|Type|nvarchar|

### Sent_Items_Folder_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


