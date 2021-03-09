# Table Sec_Group_Access_Keys

Specifies the access keys for which the user groups have permissions. The existance of a record grants read permission. Additional permissions are granted through specialized fields. Entity: Sec_Group_Access_Keys

## Owner Tables Hierarchy

* [Sec_Groups](Sec_Groups.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Group_Access_Key_Id](#group_access_key_id)|`uniqueidentifier` `PK`||
|[Access_Key_Id](#access_key_id)|`uniqueidentifier` |This access key, to which we are granting access permissions.|
|[Group_Id](#group_id)|`uniqueidentifier` |The group, which is granted with access permission.|
|[Can_Update](#can_update)|`bit` |When true, the group is granted with update permission for the entity, protected by the access key.|
|[Can_Delete](#can_delete)|`bit` |When true, the group is granted with delete permission for the entity, protected by the access key.|
|[Permission1](#permission1)|`bit` |When true, the group is granted with entity-specific permission for the entity, protected by the access key.|
|[Permission2](#permission2)|`bit` |When true, the group is granted with entity-specific permission for the entity, protected by the access key.|
|[Permission3](#permission3)|`bit` |When true, the group is granted with entity-specific permission for the entity, protected by the access key.|
|[Permission4](#permission4)|`bit` |When true, the group is granted with entity-specific permission for the entity, protected by the access key.|
|[Permission5](#permission5)|`bit` |When true, the group is granted with entity-specific permission for the entity, protected by the access key.|
|[Permission6](#permission6)|`bit` |When true, the group is granted with entity-specific permission for the entity, protected by the access key.|
|[Permission7](#permission7)|`bit` |When true, the group is granted with entity-specific permission for the entity, protected by the access key.|
|[Permission8](#permission8)|`bit` |When true, the group is granted with entity-specific permission for the entity, protected by the access key.|
|[Permission9](#permission9)|`bit` |When true, the group is granted with entity-specific permission for the entity, protected by the access key.|
|[Permission10](#permission10)|`bit` |When true, the group is granted with entity-specific permission for the entity, protected by the access key.|
|[Can_Administer](#can_administer)|`bit` |When true, the group is granted with administrative permission (allowance to change access key) for the entity, protected by the access key.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Group_Access_Key_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Access_Key_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Group_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Can_Update

| Property | Value |
| - | - |
|Type|bit|

### Can_Delete

| Property | Value |
| - | - |
|Type|bit|

### Permission1

| Property | Value |
| - | - |
|Type|bit|

### Permission2

| Property | Value |
| - | - |
|Type|bit|

### Permission3

| Property | Value |
| - | - |
|Type|bit|

### Permission4

| Property | Value |
| - | - |
|Type|bit|

### Permission5

| Property | Value |
| - | - |
|Type|bit|

### Permission6

| Property | Value |
| - | - |
|Type|bit|

### Permission7

| Property | Value |
| - | - |
|Type|bit|

### Permission8

| Property | Value |
| - | - |
|Type|bit|

### Permission9

| Property | Value |
| - | - |
|Type|bit|

### Permission10

| Property | Value |
| - | - |
|Type|bit|

### Can_Administer

| Property | Value |
| - | - |
|Type|bit|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


