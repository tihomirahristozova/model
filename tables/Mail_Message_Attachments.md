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


Mail_Message_Attachment_Id

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
|Derived From|[Mail_Message_Attachments](Mail_Message_Attachments.md).[Mail_Message_Attachment_Id](Mail_Message_Attachments.md#mail_message_attachment_id)|
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

### Mail_Message_Id


Mail_Message_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|yes|
|Referenced Table|[Mail_Messages](Mail_Messages.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Mail_Message_Attachments](Mail_Message_Attachments.md).[Mail_Message_Id](Mail_Message_Attachments.md#mail_message_id)|
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

### Name


Name

| Property | Value |
| - | - |
|Type|nvarchar(128)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Mail_Message_Attachments](Mail_Message_Attachments.md).[Name](Mail_Message_Attachments.md#name)|
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
|Max Length|128|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|
|Like|None|no|no|

### Content_Descriptors


Content_Descriptors


Content flags, like "Content-Type: text/plain; charset=utf-8"


Content flags, like "Content-Type: text/plain; charset=utf-8"

| Property | Value |
| - | - |
|Type|nvarchar(4000)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Mail_Message_Attachments](Mail_Message_Attachments.md).[Content_Descriptors](Mail_Message_Attachments.md#content_descriptors)|
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
|Max Length|4000|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Attachment_Content


Attachment_Content


The actual content of the attachment. NULL when the content is not downloaded or is unknown for some other reason


The actual content of the attachment. NULL when the content is not downloaded or is unknown for some other reason

| Property | Value |
| - | - |
|Type|varbinary|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Mail_Message_Attachments](Mail_Message_Attachments.md).[Attachment_Content](Mail_Message_Attachments.md#attachment_content)|
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

### Content_Downloaded


Content_Downloaded


1 when the content is included, 0 when this is only an empty container. Content should be included when sending mail


1 when the content is included, 0 when this is only an empty container. Content should be included when sending mail

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
|Derived From|[Mail_Message_Attachments](Mail_Message_Attachments.md).[Content_Downloaded](Mail_Message_Attachments.md#content_downloaded)|
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
|Derived From|[Mail_Message_Attachments](Mail_Message_Attachments.md).[Row_Version](Mail_Message_Attachments.md#row_version)|
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


