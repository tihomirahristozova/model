# Table Rent_Asset_Groups

Groups the rentable assets in hierarchy of logical groups. Entity: Rent_Asset_Groups

## Summary

| Name | Type | Description |
| - | - | --- |
|[Rental_Asset_Group_Id](#rental_asset_group_id)|`uniqueidentifier` `PK`||
|[Rental_Asset_Group_Code](#rental_asset_group_code)|`nvarchar(3)` |Asset group code, unique within the parent node.|
|[Rental_Asset_Group_Name](#rental_asset_group_name)|`nvarchar(254)` |Asset group name, unique within the parent node.|
|[Notes](#notes)|`nvarchar(2147483647)` ||
|[Parent_Full_Path](#parent_full_path)|`nvarchar(25)` |The full path of the parent node.|
|[Full_Path](#full_path)|`nvarchar(25)` Readonly|The full path of the node in the format of dot-delimited, dot-terminated codes of the parents.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Rental_Asset_Group_Id


Rental_Asset_Group_Id

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
|Derived From|[Rent_Asset_Groups](Rent_Asset_Groups.md).[Rental_Asset_Group_Id](Rent_Asset_Groups.md#rental_asset_group_id)|
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
|Equals|NULL|no|yes|

### Rental_Asset_Group_Code


Rental_Asset_Group_Code


Asset group code, unique within the parent node.


Asset group code, unique within the parent node.

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
|Default Value|None|
|Derived From|[Rent_Asset_Groups](Rent_Asset_Groups.md).[Rental_Asset_Group_Code](Rent_Asset_Groups.md#rental_asset_group_code)|
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
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|
|Like|None|no|no|

### Rental_Asset_Group_Name


Rental_Asset_Group_Name


Asset group name, unique within the parent node.


Asset group name, unique within the parent node.

| Property | Value |
| - | - |
|Type|nvarchar(254)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Rent_Asset_Groups](Rent_Asset_Groups.md).[Rental_Asset_Group_Name](Rent_Asset_Groups.md#rental_asset_group_name)|
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
|UI Width|Long|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|
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
|Derived From|[Rent_Asset_Groups](Rent_Asset_Groups.md).[Notes](Rent_Asset_Groups.md#notes)|
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

### Parent_Full_Path


Parent_Full_Path


The full path of the parent node.


The full path of the parent node.

| Property | Value |
| - | - |
|Type|nvarchar(25)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Rent_Asset_Groups](Rent_Asset_Groups.md).[Parent_Full_Path](Rent_Asset_Groups.md#parent_full_path)|
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
|Max Length|25|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Full_Path


Full_Path


The full path of the node in the format of dot-delimited, dot-terminated codes of the parents.


The full path of the node in the format of dot-delimited, dot-terminated codes of the parents.

| Property | Value |
| - | - |
|Type|nvarchar(25)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|yes|
|Sortable|yes|
|Attributes|None|
|Default Value|None|
|Derived From|[Rent_Asset_Groups](Rent_Asset_Groups.md).[Full_Path](Rent_Asset_Groups.md#full_path)|
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
|Max Length|25|
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
|Derived From|[Rent_Asset_Groups](Rent_Asset_Groups.md).[Row_Version](Rent_Asset_Groups.md#row_version)|
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


