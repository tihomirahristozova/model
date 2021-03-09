# Table Gen_Document_Comments

Contains user comments for documents. Entity: Gen_Document_Comments

## Owner Tables Hierarchy

* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Document_Comment_Id](#document_comment_id)|`uniqueidentifier` `PK`||
|[Document_Id](#document_id)|`uniqueidentifier` |The document to which to attach the comment|
|[Comment_Timestamp](#comment_timestamp)|`datetime` |The exact timestamp of the comment|
|[User_Id](#user_id)|`uniqueidentifier` |The user, who created the comment|
|[Comment](#comment)|`nvarchar(254)` |The user comment.|
|[Assign_To_User_Id](#assign_to_user_id)|`uniqueidentifier` |When not NULL means that the comment is also an assignment of the document to another user. Upon saving the comment, the system assigns the document to the specified user|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Document_Comment_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Comment_Timestamp

| Property | Value |
| - | - |
|Type|datetime|

### User_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Comment

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Assign_To_User_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


