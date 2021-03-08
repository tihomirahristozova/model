# Table Cmm_Social_Comments

User comment to any object in the system. Entity: Cmm_Social_Comments (Introduced in version 20.1)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Social_Comment_Id|`Guid`|`PK`, Readonly||
|Comment_Text|`String`||The comment contents in clear text. `Required` |
|Creation_Time_Utc|`DateTime`||The exact server time (in UTC), when the comment was created. `Required` `ORD` |
