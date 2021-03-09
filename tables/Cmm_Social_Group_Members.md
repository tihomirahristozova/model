# Table Cmm_Social_Group_Members

Represents the membership of a user in a social group. Entity: Cmm_Social_Group_Members (Introduced in version 20.1)

## Owner Tables Hierarchy

* [Cmm_Social_Groups](Cmm_Social_Groups.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Social_Group_Member_Id](#social_group_member_id)|`uniqueidentifier` `PK`||
|[Social_Group_Id](#social_group_id)|`uniqueidentifier` |The group in which the user participates.|
|[User_Id](#user_id)|`uniqueidentifier` |The user, who is a member of the group.|
|[Join_Time_Utc](#join_time_utc)|`datetime` |The exact server time (in UTC), when the user joined the group.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Social_Group_Member_Id

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

### Join_Time_Utc

| Property | Value |
| - | - |
|Type|datetime|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


