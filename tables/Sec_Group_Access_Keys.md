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


Group_Access_Key_Id

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
|Derived From|[Sec_Group_Access_Keys](Sec_Group_Access_Keys.md).[Group_Access_Key_Id](Sec_Group_Access_Keys.md#group_access_key_id)|
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

### Access_Key_Id


Access_Key_Id


This access key, to which we are granting access permissions.


This access key, to which we are granting access permissions.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Sec_Access_Keys](Sec_Access_Keys.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sec_Group_Access_Keys](Sec_Group_Access_Keys.md).[Access_Key_Id](Sec_Group_Access_Keys.md#access_key_id)|
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

### Group_Id


Group_Id


The group, which is granted with access permission.


The group, which is granted with access permission.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|yes|
|Referenced Table|[Sec_Groups](Sec_Groups.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sec_Group_Access_Keys](Sec_Group_Access_Keys.md).[Group_Id](Sec_Group_Access_Keys.md#group_id)|
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

### Can_Update


Can_Update


When true, the group is granted with update permission for the entity, protected by the access key.


When true, the group is granted with update permission for the entity, protected by the access key.

| Property | Value |
| - | - |
|Type|bit|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sec_Group_Access_Keys](Sec_Group_Access_Keys.md).[Can_Update](Sec_Group_Access_Keys.md#can_update)|
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

### Can_Delete


Can_Delete


When true, the group is granted with delete permission for the entity, protected by the access key.


When true, the group is granted with delete permission for the entity, protected by the access key.

| Property | Value |
| - | - |
|Type|bit|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sec_Group_Access_Keys](Sec_Group_Access_Keys.md).[Can_Delete](Sec_Group_Access_Keys.md#can_delete)|
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

### Permission1


Permission1


When true, the group is granted with entity-specific permission for the entity, protected by the access key.


When true, the group is granted with entity-specific permission for the entity, protected by the access key.

| Property | Value |
| - | - |
|Type|bit|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|False|
|Derived From|[Sec_Group_Access_Keys](Sec_Group_Access_Keys.md).[Permission1](Sec_Group_Access_Keys.md#permission1)|
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

### Permission2


Permission2


When true, the group is granted with entity-specific permission for the entity, protected by the access key.


When true, the group is granted with entity-specific permission for the entity, protected by the access key.

| Property | Value |
| - | - |
|Type|bit|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|False|
|Derived From|[Sec_Group_Access_Keys](Sec_Group_Access_Keys.md).[Permission2](Sec_Group_Access_Keys.md#permission2)|
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

### Permission3


Permission3


When true, the group is granted with entity-specific permission for the entity, protected by the access key.


When true, the group is granted with entity-specific permission for the entity, protected by the access key.

| Property | Value |
| - | - |
|Type|bit|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|False|
|Derived From|[Sec_Group_Access_Keys](Sec_Group_Access_Keys.md).[Permission3](Sec_Group_Access_Keys.md#permission3)|
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

### Permission4


Permission4


When true, the group is granted with entity-specific permission for the entity, protected by the access key.


When true, the group is granted with entity-specific permission for the entity, protected by the access key.

| Property | Value |
| - | - |
|Type|bit|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|False|
|Derived From|[Sec_Group_Access_Keys](Sec_Group_Access_Keys.md).[Permission4](Sec_Group_Access_Keys.md#permission4)|
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

### Permission5


Permission5


When true, the group is granted with entity-specific permission for the entity, protected by the access key.


When true, the group is granted with entity-specific permission for the entity, protected by the access key.

| Property | Value |
| - | - |
|Type|bit|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|False|
|Derived From|[Sec_Group_Access_Keys](Sec_Group_Access_Keys.md).[Permission5](Sec_Group_Access_Keys.md#permission5)|
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

### Permission6


Permission6


When true, the group is granted with entity-specific permission for the entity, protected by the access key.


When true, the group is granted with entity-specific permission for the entity, protected by the access key.

| Property | Value |
| - | - |
|Type|bit|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|False|
|Derived From|[Sec_Group_Access_Keys](Sec_Group_Access_Keys.md).[Permission6](Sec_Group_Access_Keys.md#permission6)|
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

### Permission7


Permission7


When true, the group is granted with entity-specific permission for the entity, protected by the access key.


When true, the group is granted with entity-specific permission for the entity, protected by the access key.

| Property | Value |
| - | - |
|Type|bit|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|False|
|Derived From|[Sec_Group_Access_Keys](Sec_Group_Access_Keys.md).[Permission7](Sec_Group_Access_Keys.md#permission7)|
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

### Permission8


Permission8


When true, the group is granted with entity-specific permission for the entity, protected by the access key.


When true, the group is granted with entity-specific permission for the entity, protected by the access key.

| Property | Value |
| - | - |
|Type|bit|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|False|
|Derived From|[Sec_Group_Access_Keys](Sec_Group_Access_Keys.md).[Permission8](Sec_Group_Access_Keys.md#permission8)|
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

### Permission9


Permission9


When true, the group is granted with entity-specific permission for the entity, protected by the access key.


When true, the group is granted with entity-specific permission for the entity, protected by the access key.

| Property | Value |
| - | - |
|Type|bit|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|False|
|Derived From|[Sec_Group_Access_Keys](Sec_Group_Access_Keys.md).[Permission9](Sec_Group_Access_Keys.md#permission9)|
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

### Permission10


Permission10


When true, the group is granted with entity-specific permission for the entity, protected by the access key.


When true, the group is granted with entity-specific permission for the entity, protected by the access key.

| Property | Value |
| - | - |
|Type|bit|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|False|
|Derived From|[Sec_Group_Access_Keys](Sec_Group_Access_Keys.md).[Permission10](Sec_Group_Access_Keys.md#permission10)|
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

### Can_Administer


Can_Administer


When true, the group is granted with administrative permission (allowance to change access key) for the entity, protected by the access key.


When true, the group is granted with administrative permission (allowance to change access key) for the entity, protected by the access key.

| Property | Value |
| - | - |
|Type|bit|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|False|
|Derived From|[Sec_Group_Access_Keys](Sec_Group_Access_Keys.md).[Can_Administer](Sec_Group_Access_Keys.md#can_administer)|
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
|Derived From|[Sec_Group_Access_Keys](Sec_Group_Access_Keys.md).[Row_Version](Sec_Group_Access_Keys.md#row_version)|
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


