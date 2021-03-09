# Table Mail_Box_Folders

Contains the folders inside the mailboxes. Entity: Mail_Box_Folders

## Owner Tables Hierarchy

* [Mail_Boxes](Mail_Boxes.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Mail_Box_Id](#mail_box_id)|`uniqueidentifier` Readonly||
|[Folder_Name](#folder_name)|`nvarchar(254)` `ML`|Multi-language folder name|
|[Parent_Folder_Id](#parent_folder_id)|`uniqueidentifier` |The parent folder in the folder hierarchy. Null when the folder is a root folder.|
|[System_Purpose](#system_purpose)|`nvarchar(1)` Allowed: `M`, `I`, `D`, `O`, `S`, `T`, Readonly|When not NULL means that the folder has special system designation. Designations are: M=Mailbox(root folder), I=Inbox, D=Drafts, O=Outbox, S=Sent, T=Trash.|
|[Sync_State](#sync_state)|`nvarchar(2147483647)` |The synchronization state for the folder. The format of the contents is dependant on the server type. For IMAP, this is last message Id, for Exchange - this is SyncState.|
|[Mail_Box_Folder_Id](#mail_box_folder_id)|`uniqueidentifier` `PK`||
|[Server_Folder_ID](#server_folder_id)|`nvarchar(256)` |ID of the folder on the mail server in the format of the mail server|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Mail_Box_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Folder_Name

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Parent_Folder_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### System_Purpose

| Property | Value |
| - | - |
|Type|nvarchar(1)|

### Sync_State

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Mail_Box_Folder_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Server_Folder_ID

| Property | Value |
| - | - |
|Type|nvarchar(256)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


