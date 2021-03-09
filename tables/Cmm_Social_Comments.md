# Table Cmm_Social_Comments

User comment to any object in the system. Entity: Cmm_Social_Comments (Introduced in version 20.1)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Social_Comment_Id](#social_comment_id)|`uniqueidentifier` `PK`||
|[Data_Object_Id](#data_object_id)|`uniqueidentifier` |The root data object (post, marketplace product, document, etc), for which the comment is made.|
|[Reply_To_Comment_Id](#reply_to_comment_id)|`uniqueidentifier` |When not null, means that the comment is a reply to the specified comment. The comment and the reply should be for the same data object.|
|[User_Id](#user_id)|`uniqueidentifier` |The user, who made the comment.|
|[Comment_Text](#comment_text)|`nvarchar(2147483647)` |The comment contents in clear text.|
|[Creation_Time_Utc](#creation_time_utc)|`datetime` |The exact server time (in UTC), when the comment was created.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Social_Comment_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Data_Object_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Reply_To_Comment_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### User_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Comment_Text

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Creation_Time_Utc

| Property | Value |
| - | - |
|Type|datetime|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


