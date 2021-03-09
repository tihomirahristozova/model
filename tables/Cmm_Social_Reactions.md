# Table Cmm_Social_Reactions

Reaction of a user to any social comment to an object of the system. Entity: Cmm_Social_Reactions (Introduced in version 20.1)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Social_Reaction_Id](#social_reaction_id)|`uniqueidentifier` `PK`||
|[Data_Object_Id](#data_object_id)|`uniqueidentifier` |The root data object (post, marketplace product, document, etc), for which the reaction is.|
|[Social_Comment_Id](#social_comment_id)|`uniqueidentifier` |When not null, specifies that the reaction is for the specified comment within the data object.|
|[User_Id](#user_id)|`uniqueidentifier` |The user, who reacted.|
|[Reaction_Type](#reaction_type)|`nvarchar(3)` Allowed: `LIK`, `LOV`, `HAH`, `WOW`, `SAD`, `ANG`|The type of the reaction. LIK = Like; LOV = Love; HAH = Haha; WOW = Wow; SAD = Sad; ANG = Angry.|
|[Creation_Time_Utc](#creation_time_utc)|`datetime` |The exact server time (in UTC), when the reaction was created.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Social_Reaction_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Data_Object_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Social_Comment_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### User_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Reaction_Type

| Property | Value |
| - | - |
|Type|nvarchar(3)|

### Creation_Time_Utc

| Property | Value |
| - | - |
|Type|datetime|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


