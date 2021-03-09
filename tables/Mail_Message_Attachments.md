# Table Mail_Message_Attachments

Represents attachments to mail messages. Entity: Mail_Message_Attachments

## Owner Tables Hierarchy

* [Mail_Messages](Mail_Messages.md)
* [Mail_Box_Folders](Mail_Box_Folders.md)
* [Mail_Boxes](Mail_Boxes.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Mail_Message_Attachment_Id](#mail_message_attachment_id)|`uniqueidentifier` `PK`||
|[Mail_Message_Id](#mail_message_id)|`uniqueidentifier` ||
|[Name](#name)|`nvarchar(128)` ||
|[Content_Descriptors](#content_descriptors)|`nvarchar(4000)` |Content flags, like "Content-Type: text/plain; charset=utf-8"|
|[Attachment_Content](#attachment_content)|`varbinary` |The actual content of the attachment. NULL when the content is not downloaded or is unknown for some other reason|
|[Content_Downloaded](#content_downloaded)|`bit` |1 when the content is included, 0 when this is only an empty container. Content should be included when sending mail|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Mail_Message_Attachment_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Mail_Message_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Name

| Property | Value |
| - | - |
|Type|nvarchar(128)|

### Content_Descriptors

| Property | Value |
| - | - |
|Type|nvarchar(4000)|

### Attachment_Content

| Property | Value |
| - | - |
|Type|varbinary|

### Content_Downloaded

| Property | Value |
| - | - |
|Type|bit|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


