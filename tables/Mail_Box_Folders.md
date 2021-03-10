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


Mail_Box_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|yes|
|Referenced Table|[Mail_Boxes](Mail_Boxes.md)|
|Readonly|yes|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Mail_Box_Folders](Mail_Box_Folders.md).[Mail_Box_Id](Mail_Box_Folders.md#mail_box_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|1|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Folder_Name


Folder_Name


Multi-language folder name


Multi-language folder name

| Property | Value |
| - | - |
|Type|nvarchar(254)|
|Is Mulitlanguage|yes|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Mail_Box_Folders](Mail_Box_Folders.md).[Folder_Name](Mail_Box_Folders.md#folder_name)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|254|
|Order|2|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|
|Like|None|no|no|

### Parent_Folder_Id


Parent_Folder_Id


The parent folder in the folder hierarchy. Null when the folder is a root folder.


The parent folder in the folder hierarchy. Null when the folder is a root folder.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Mail_Box_Folders](Mail_Box_Folders.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Mail_Box_Folders](Mail_Box_Folders.md).[Parent_Folder_Id](Mail_Box_Folders.md#parent_folder_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|3|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### System_Purpose


System_Purpose


When not NULL means that the folder has special system designation. Designations are: M=Mailbox(root folder), I=Inbox, D=Drafts, O=Outbox, S=Sent, T=Trash.


When not NULL means that the folder has special system designation. Designations are: M=Mailbox(root folder), I=Inbox, D=Drafts, O=Outbox, S=Sent, T=Trash.

| Property | Value |
| - | - |
|Type|nvarchar(1)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|yes|
|Sortable|no|
|Attributes|None|
|Allowed Values|`M`, `I`, `D`, `O`, `S`, `T`|
|Default Value|None|
|Derived From|[Mail_Box_Folders](Mail_Box_Folders.md).[System_Purpose](Mail_Box_Folders.md#system_purpose)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|1|
|Order|4|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Sync_State


Sync_State


The synchronization state for the folder. The format of the contents is dependant on the server type. For IMAP, this is last message Id, for Exchange - this is SyncState.


The synchronization state for the folder. The format of the contents is dependant on the server type. For IMAP, this is last message Id, for Exchange - this is SyncState.

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Mail_Box_Folders](Mail_Box_Folders.md).[Sync_State](Mail_Box_Folders.md#sync_state)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|2147483647|
|Order|5|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Mail_Box_Folder_Id


Mail_Box_Folder_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|yes|
|Order in Primary Key|1|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|NewGuid|
|Derived From|[Mail_Box_Folders](Mail_Box_Folders.md).[Mail_Box_Folder_Id](Mail_Box_Folders.md#mail_box_folder_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Server_Folder_ID


Server_Folder_ID


ID of the folder on the mail server in the format of the mail server


ID of the folder on the mail server in the format of the mail server

| Property | Value |
| - | - |
|Type|nvarchar(256)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Mail_Box_Folders](Mail_Box_Folders.md).[Server_Folder_ID](Mail_Box_Folders.md#server_folder_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|256|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Row_Version


Row_Version

| Property | Value |
| - | - |
|Type|timestamp|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Mail_Box_Folders](Mail_Box_Folders.md).[Row_Version](Mail_Box_Folders.md#row_version)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|


