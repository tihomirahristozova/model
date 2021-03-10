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


Mail_Box_Id

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
|Derived From|[Mail_Boxes](Mail_Boxes.md).[Mail_Box_Id](Mail_Boxes.md#mail_box_id)|
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
|Equals|NULL|no|yes|

### Owner_User_Id


Owner_User_Id


The user, who owns the mailbox


The user, who owns the mailbox

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Sec_Users](Sec_Users.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Mail_Boxes](Mail_Boxes.md).[Owner_User_Id](Mail_Boxes.md#owner_user_id)|
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
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Email_Address


Email_Address


The email address associated with this mail box


The email address associated with this mail box

| Property | Value |
| - | - |
|Type|nvarchar(254)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Mail_Boxes](Mail_Boxes.md).[Email_Address](Mail_Boxes.md#email_address)|
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
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Sync_Protocol


Sync_Protocol


Synchronization protocol, 'POP3' or 'IMAP'. NULL means that syncrhonization is not setup


Synchronization protocol, 'POP3' or 'IMAP'. NULL means that syncrhonization is not setup

| Property | Value |
| - | - |
|Type|nvarchar(4)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Allowed Values|`IMAP`, `POP3`, `MEWS`|
|Default Value|None|
|Derived From|[Mail_Boxes](Mail_Boxes.md).[Sync_Protocol](Mail_Boxes.md#sync_protocol)|
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
|Max Length|4|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Sync_Server_Address


Sync_Server_Address


Incoming and outgoing mail server internet address. NULL when synchronization is not setup


Incoming and outgoing mail server internet address. NULL when synchronization is not setup

| Property | Value |
| - | - |
|Type|nvarchar(254)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Mail_Boxes](Mail_Boxes.md).[Sync_Server_Address](Mail_Boxes.md#sync_server_address)|
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
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Sync_User_Name


Sync_User_Name


User name to supply to the server, when retrieving email. NULL when the connection is not setup or the server does not require user name


User name to supply to the server, when retrieving email. NULL when the connection is not setup or the server does not require user name

| Property | Value |
| - | - |
|Type|nvarchar(64)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Mail_Boxes](Mail_Boxes.md).[Sync_User_Name](Mail_Boxes.md#sync_user_name)|
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
|Max Length|64|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Sync_Password


Sync_Password


The password to supply to the server when retrieving email. NULL when the connection is not setup or the server does not require user name


The password to supply to the server when retrieving email. NULL when the connection is not setup or the server does not require user name

| Property | Value |
| - | - |
|Type|nvarchar(512)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Mail_Boxes](Mail_Boxes.md).[Sync_Password](Mail_Boxes.md#sync_password)|
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
|Max Length|512|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Active


Active


1 when the mail box is active for mail sinchronization, sending and receiving


1 when the mail box is active for mail sinchronization, sending and receiving

| Property | Value |
| - | - |
|Type|bit|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|True|
|Derived From|[Mail_Boxes](Mail_Boxes.md).[Active](Mail_Boxes.md#active)|
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
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Send_Server_Address


Send_Server_Address


The address of the server to use for sending mail. The same credentials as the sync server are used. When NULL, the mail will be sent using the default server, which is setup at the application server


The address of the server to use for sending mail. The same credentials as the sync server are used. When NULL, the mail will be sent using the default server, which is setup at the application server

| Property | Value |
| - | - |
|Type|nvarchar(254)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Mail_Boxes](Mail_Boxes.md).[Send_Server_Address](Mail_Boxes.md#send_server_address)|
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
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Is_Default


Is_Default


1 when this is the default mailbox for the user.


1 when this is the default mailbox for the user.

| Property | Value |
| - | - |
|Type|bit|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|True|
|Derived From|[Mail_Boxes](Mail_Boxes.md).[Is_Default](Mail_Boxes.md#is_default)|
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
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Is_Encrypted


Is_Encrypted


1 when the mailbox messages are stored in encrypted format


1 when the mailbox messages are stored in encrypted format

| Property | Value |
| - | - |
|Type|bit|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|False|
|Derived From|[Mail_Boxes](Mail_Boxes.md).[Is_Encrypted](Mail_Boxes.md#is_encrypted)|
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
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Reset_On_Next_Sync


Reset_On_Next_Sync


Reset is pending: 1 = next sync should delete and retrieve again all messages; 0 = no pending reset


Reset is pending: 1 = next sync should delete and retrieve again all messages; 0 = no pending reset

| Property | Value |
| - | - |
|Type|bit|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|yes|
|Sortable|no|
|Attributes|None|
|Default Value|False|
|Derived From|[Mail_Boxes](Mail_Boxes.md).[Reset_On_Next_Sync](Mail_Boxes.md#reset_on_next_sync)|
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
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Signature_Html


Signature_Html


Html text of the default signature, when creating new emails from this mailbox. When is NULL, a default generic signature is attached


Html text of the default signature, when creating new emails from this mailbox. When is NULL, a default generic signature is attached

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
|Derived From|[Mail_Boxes](Mail_Boxes.md).[Signature_Html](Mail_Boxes.md#signature_html)|
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
|Max Length|2147483647|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Sent_Items_Folder_Name


Sent_Items_Folder_Name


The name of the SentItems folder. It is left empty, EnterpriseOne won't save the sent mail in any folder (but it is still possible that the actual mail server would nevertheless save the mail in a sent items folder, independently from EnterpriseOne).


The name of the SentItems folder. It is left empty, EnterpriseOne won't save the sent mail in any folder (but it is still possible that the actual mail server would nevertheless save the mail in a sent items folder, independently from EnterpriseOne).

| Property | Value |
| - | - |
|Type|nvarchar(254)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Mail_Boxes](Mail_Boxes.md).[Sent_Items_Folder_Name](Mail_Boxes.md#sent_items_folder_name)|
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
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

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
|Derived From|[Mail_Boxes](Mail_Boxes.md).[Row_Version](Mail_Boxes.md#row_version)|
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


