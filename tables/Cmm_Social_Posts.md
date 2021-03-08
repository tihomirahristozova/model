# Table Cmm_Social_Posts

User post in a social group. Entity: Cmm_Social_Posts (Introduced in version 20.1)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Social_Post_Id|`Guid`|`PK`, Readonly||
|Creation_Time_Utc|`DateTime`||The exact server time (in UTC), when the post was created. `Required` |
|Last_Interaction_Time_Utc|`DateTime`||The server time (in UTC) of the last interaction with the post, including comments, replies, likes, etc. `Required` |
|Post_Text|`String`||The post contents in clear text. `Required` |
