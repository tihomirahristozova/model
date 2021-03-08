# Table Cmm_Social_Group_Members

Represents the membership of a user in a social group. Entity: Cmm_Social_Group_Members (Introduced in version 20.1)

# Aggregate Hierarchy

* [Cmm_Social_Groups](Cmm_Social_Groups.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Social_Group_Member_Id|`Guid`|`PK`, Readonly||
|Join_Time_Utc|`DateTime`||The exact server time (in UTC), when the user joined the group. `Required` `Default(NowUtc)` |
