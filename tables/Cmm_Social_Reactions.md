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


Social_Reaction_Id

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
|Derived From|[Cmm_Social_Reactions](Cmm_Social_Reactions.md).[Social_Reaction_Id](Cmm_Social_Reactions.md#social_reaction_id)|
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

### Data_Object_Id


Data_Object_Id


The root data object (post, marketplace product, document, etc), for which the reaction is.


The root data object (post, marketplace product, document, etc), for which the reaction is.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Sys_Objects](Sys_Objects.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Cmm_Social_Reactions](Cmm_Social_Reactions.md).[Data_Object_Id](Cmm_Social_Reactions.md#data_object_id)|
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

### Social_Comment_Id


Social_Comment_Id


When not null, specifies that the reaction is for the specified comment within the data object.


When not null, specifies that the reaction is for the specified comment within the data object.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Cmm_Social_Comments](Cmm_Social_Comments.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Cmm_Social_Reactions](Cmm_Social_Reactions.md).[Social_Comment_Id](Cmm_Social_Reactions.md#social_comment_id)|
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
|Equals|NULL|yes|no|

### User_Id


User_Id


The user, who reacted.


The user, who reacted.

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
|Derived From|[Cmm_Social_Reactions](Cmm_Social_Reactions.md).[User_Id](Cmm_Social_Reactions.md#user_id)|
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

### Reaction_Type


Reaction_Type


The type of the reaction. LIK = Like; LOV = Love; HAH = Haha; WOW = Wow; SAD = Sad; ANG = Angry.


The type of the reaction. LIK = Like; LOV = Love; HAH = Haha; WOW = Wow; SAD = Sad; ANG = Angry.

| Property | Value |
| - | - |
|Type|nvarchar(3)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Allowed Values|`LIK`, `LOV`, `HAH`, `WOW`, `SAD`, `ANG`|
|Default Value|None|
|Derived From|[Cmm_Social_Reactions](Cmm_Social_Reactions.md).[Reaction_Type](Cmm_Social_Reactions.md#reaction_type)|
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
|Max Length|3|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Creation_Time_Utc


Creation_Time_Utc


The exact server time (in UTC), when the reaction was created.


The exact server time (in UTC), when the reaction was created.

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
|Default Value|CurrentDateTimeUtc|
|Derived From|[Cmm_Social_Reactions](Cmm_Social_Reactions.md).[Creation_Time_Utc](Cmm_Social_Reactions.md#creation_time_utc)|
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
|Derived From|[Cmm_Social_Reactions](Cmm_Social_Reactions.md).[Row_Version](Cmm_Social_Reactions.md#row_version)|
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


