# Table Cmm_Social_Groups

Represents a group of users, sharing interest in the group topic. Entity: Cmm_Social_Groups (Introduced in version 20.1)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Social_Group_Id|`Guid`|`PK`, Readonly||
|Social_Group_Code|`String`||Unique code of the group. Also used as group slug for Internet URL purposes. `Required` `ORD` |
|Social_Group_Name|`String`||Multilanguage name of the group. `Required` |
|Notes|`String`||Notes for this SocialGroup. |
