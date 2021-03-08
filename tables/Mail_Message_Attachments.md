# Table Mail_Message_Attachments

Represents attachments to mail messages. Entity: Mail_Message_Attachments

# Aggregate Hierarchy

* [Mail_Messages](Mail_Messages.md)
* [Mail_Box_Folders](Mail_Box_Folders.md)
* [Mail_Boxes](Mail_Boxes.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Mail_Message_Attachment_Id|`Guid`|`PK`, Readonly||
|Attachment_Content|`Byte[]`|`BLOB`|The actual content of the attachment. null when the content is not downloaded or is unknown for some other reason. |
|Content_Descriptors|`String`||Content flags, like "Content-Type: text/plain; charset=utf-8". |
|Content_Downloaded|`Boolean`||True when the content is included, false when this is only an empty container. Content should be included when sending mail. `Required` `Default(false)` `Filter(eq)` |
|Name|`String`||The name of this MessageAttachment. `Filter(eq;like)` |
