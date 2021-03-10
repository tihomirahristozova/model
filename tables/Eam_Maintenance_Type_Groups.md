# Table Eam_Maintenance_Type_Groups

Represents the hierarchy of the groups of maintenance types. Entity: Eam_Maintenance_Type_Groups (Introduced in version 19.1)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Maintenance_Type_Group_Id](#maintenance_type_group_id)|`uniqueidentifier` `PK`||
|[Maintenance_Type_Group_Code](#maintenance_type_group_code)|`nvarchar(16)` |Unique code of the group.|
|[Parent_Maintenance_Type_Group_Id](#parent_maintenance_type_group_id)|`uniqueidentifier` |Parent group. NULL denotes a root group.|
|[Maintenance_Type_Group_Name](#maintenance_type_group_name)|`nvarchar(254)` `ML`|Multilanguage name of the group.|
|[Notes](#notes)|`nvarchar(2147483647)` ||
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Maintenance_Type_Group_Id


Maintenance_Type_Group_Id

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
|Derived From|[Eam_Maintenance_Type_Groups](Eam_Maintenance_Type_Groups.md).[Maintenance_Type_Group_Id](Eam_Maintenance_Type_Groups.md#maintenance_type_group_id)|
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
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Maintenance_Type_Group_Code


Maintenance_Type_Group_Code


Unique code of the group.


Unique code of the group.

| Property | Value |
| - | - |
|Type|nvarchar(16)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|yes|
|Attributes|None|
|Default Value|None|
|Derived From|[Eam_Maintenance_Type_Groups](Eam_Maintenance_Type_Groups.md).[Maintenance_Type_Group_Code](Eam_Maintenance_Type_Groups.md#maintenance_type_group_code)|
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
|Max Length|16|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|yes|
|Like|None|no|no|

### Parent_Maintenance_Type_Group_Id


Parent_Maintenance_Type_Group_Id


Parent group. NULL denotes a root group.


Parent group. NULL denotes a root group.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Eam_Maintenance_Type_Groups](Eam_Maintenance_Type_Groups.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Eam_Maintenance_Type_Groups](Eam_Maintenance_Type_Groups.md).[Parent_Maintenance_Type_Group_Id](Eam_Maintenance_Type_Groups.md#parent_maintenance_type_group_id)|
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

### Maintenance_Type_Group_Name


Maintenance_Type_Group_Name


Multilanguage name of the group.


Multilanguage name of the group.

| Property | Value |
| - | - |
|Type|nvarchar(254)|
|Is Mulitlanguage|yes|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Eam_Maintenance_Type_Groups](Eam_Maintenance_Type_Groups.md).[Maintenance_Type_Group_Name](Eam_Maintenance_Type_Groups.md#maintenance_type_group_name)|
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
|Max Length|254|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|yes|
|Like|None|no|no|

### Notes


Notes

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None, IsLongString|
|Default Value|None|
|Derived From|[Eam_Maintenance_Type_Groups](Eam_Maintenance_Type_Groups.md).[Notes](Eam_Maintenance_Type_Groups.md#notes)|
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
|Derived From|[Eam_Maintenance_Type_Groups](Eam_Maintenance_Type_Groups.md).[Row_Version](Eam_Maintenance_Type_Groups.md#row_version)|
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


