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


Social_Post_Id

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
|Derived From|[Cmm_Social_Posts](Cmm_Social_Posts.md).[Social_Post_Id](Cmm_Social_Posts.md#social_post_id)|
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

### Social_Group_Id


Social_Group_Id


The group in which the post is made.


The group in which the post is made.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Cmm_Social_Groups](Cmm_Social_Groups.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Cmm_Social_Posts](Cmm_Social_Posts.md).[Social_Group_Id](Cmm_Social_Posts.md#social_group_id)|
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

### User_Id


User_Id


The user, who made the post.


The user, who made the post.

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
|Derived From|[Cmm_Social_Posts](Cmm_Social_Posts.md).[User_Id](Cmm_Social_Posts.md#user_id)|
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

### Post_Text


Post_Text


The post contents in clear text.


The post contents in clear text.

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Cmm_Social_Posts](Cmm_Social_Posts.md).[Post_Text](Cmm_Social_Posts.md#post_text)|
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

### Creation_Time_Utc


Creation_Time_Utc


The exact server time (in UTC), when the post was created.


The exact server time (in UTC), when the post was created.

| Property | Value |
| - | - |
|Type|datetime|
|DateTime Format|DateTime|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Cmm_Social_Posts](Cmm_Social_Posts.md).[Creation_Time_Utc](Cmm_Social_Posts.md#creation_time_utc)|
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

### Last_Interaction_Time_Utc


Last_Interaction_Time_Utc


The server time (in UTC) of the last interaction with the post, including comments, replies, likes, etc.


The server time (in UTC) of the last interaction with the post, including comments, replies, likes, etc.

| Property | Value |
| - | - |
|Type|datetime|
|DateTime Format|DateTime|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Cmm_Social_Posts](Cmm_Social_Posts.md).[Last_Interaction_Time_Utc](Cmm_Social_Posts.md#last_interaction_time_utc)|
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
|Derived From|[Cmm_Social_Posts](Cmm_Social_Posts.md).[Row_Version](Cmm_Social_Posts.md#row_version)|
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


