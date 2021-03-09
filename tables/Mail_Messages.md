# Table Mail_Messages

Represents email messages. Entity: Mail_Messages

## Owner Tables Hierarchy

* [Mail_Box_Folders](Mail_Box_Folders.md)
* [Mail_Boxes](Mail_Boxes.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Mail_Message_Id](#mail_message_id)|`uniqueidentifier` `PK`||
|[Mail_Box_Folder_Id](#mail_box_folder_id)|`uniqueidentifier` ||
|[From_Email_Address](#from_email_address)|`nvarchar(512)` |Sending email address|
|[To_Email_Address_List](#to_email_address_list)|`nvarchar(2048)` |Semicolon-separated list of receiving email addresses|
|[Cc_Email_Address_List](#cc_email_address_list)|`nvarchar(2048)` |Semicolon-separated list of Cc email addresses|
|[Subject](#subject)|`nvarchar(1024)` |The message subject|
|[Body](#body)|`nvarchar(2147483647)` |The body of the message|
|[Is_Read](#is_read)|`bit` |1 when the message was read by the user|
|[Server_Message_ID](#server_message_id)|`nvarchar(256)` |Message ID as it appears on the mail server|
|[Creation_Date_Time](#creation_date_time)|`datetime` |Date and time when the message was created|
|[Sent_Date_Time](#sent_date_time)|`datetime` |Date and time when the message was sent|
|[Received_Date_Time](#received_date_time)|`datetime` |Date and time when the message was received|
|[Related_To_Party_Id](#related_to_party_id)|`uniqueidentifier` |The party id of the external participating (sender/receiver) party (customer, supplier, etc.) in this mail. NULL means that the email is still not related to any specific party|
|[Is_Encrypted](#is_encrypted)|`bit` |1 when the message is stored in encrypted format|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Mail_Message_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Mail_Box_Folder_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### From_Email_Address

| Property | Value |
| - | - |
|Type|nvarchar(512)|

### To_Email_Address_List

| Property | Value |
| - | - |
|Type|nvarchar(2048)|

### Cc_Email_Address_List

| Property | Value |
| - | - |
|Type|nvarchar(2048)|

### Subject

| Property | Value |
| - | - |
|Type|nvarchar(1024)|

### Body

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Is_Read

| Property | Value |
| - | - |
|Type|bit|

### Server_Message_ID

| Property | Value |
| - | - |
|Type|nvarchar(256)|

### Creation_Date_Time

| Property | Value |
| - | - |
|Type|datetime|

### Sent_Date_Time

| Property | Value |
| - | - |
|Type|datetime|

### Received_Date_Time

| Property | Value |
| - | - |
|Type|datetime|

### Related_To_Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Is_Encrypted

| Property | Value |
| - | - |
|Type|bit|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


