# Table Cmm_Social_Posts

User post in a social group. Entity: Cmm_Social_Posts (Introduced in version 20.1)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Social_Post_Id](#social_post_id)|`uniqueidentifier` `PK`||
|[Social_Group_Id](#social_group_id)|`uniqueidentifier` |The group in which the post is made.|
|[User_Id](#user_id)|`uniqueidentifier` |The user, who made the post.|
|[Post_Text](#post_text)|`nvarchar(2147483647)` |The post contents in clear text.|
|[Creation_Time_Utc](#creation_time_utc)|`datetime` |The exact server time (in UTC), when the post was created.|
|[Last_Interaction_Time_Utc](#last_interaction_time_utc)|`datetime` |The server time (in UTC) of the last interaction with the post, including comments, replies, likes, etc.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Social_Post_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Social_Group_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### User_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Post_Text

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Creation_Time_Utc

| Property | Value |
| - | - |
|Type|datetime|

### Last_Interaction_Time_Utc

| Property | Value |
| - | - |
|Type|datetime|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


