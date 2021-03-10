# Table Dw_Data_Measure_Groups

Contains the groups of measures in the general data warehouse. Entity: Dw_Data_Measure_Groups (Introduced in version 18.2)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Data_Measure_Group_Id](#data_measure_group_id)|`uniqueidentifier` `PK`||
|[Parent_Data_Measure_Group_Id](#parent_data_measure_group_id)|`uniqueidentifier` |Parent data measure group in the hierarchy. Null when this is root node.|
|[Data_Measure_Group_Code](#data_measure_group_code)|`nvarchar(16)` |Unique group code.|
|[Data_Measure_Group_Name](#data_measure_group_name)|`nvarchar(254)` |Group name (multilanguage).|
|[Notes](#notes)|`nvarchar(2147483647)` ||

## Columns

### Data_Measure_Group_Id


Data_Measure_Group_Id

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
|Derived From|[Dw_Data_Measure_Groups](Dw_Data_Measure_Groups.md).[Data_Measure_Group_Id](Dw_Data_Measure_Groups.md#data_measure_group_id)|
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

### Parent_Data_Measure_Group_Id


Parent_Data_Measure_Group_Id


Parent data measure group in the hierarchy. Null when this is root node.


Parent data measure group in the hierarchy. Null when this is root node.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Dw_Data_Measure_Groups](Dw_Data_Measure_Groups.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Dw_Data_Measure_Groups](Dw_Data_Measure_Groups.md).[Parent_Data_Measure_Group_Id](Dw_Data_Measure_Groups.md#parent_data_measure_group_id)|
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

### Data_Measure_Group_Code


Data_Measure_Group_Code


Unique group code.


Unique group code.

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
|Derived From|[Dw_Data_Measure_Groups](Dw_Data_Measure_Groups.md).[Data_Measure_Group_Code](Dw_Data_Measure_Groups.md#data_measure_group_code)|
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
|Equals|NULL|no|no|
|Like|None|no|no|

### Data_Measure_Group_Name


Data_Measure_Group_Name


Group name (multilanguage).


Group name (multilanguage).

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
|Derived From|[Dw_Data_Measure_Groups](Dw_Data_Measure_Groups.md).[Data_Measure_Group_Name](Dw_Data_Measure_Groups.md#data_measure_group_name)|
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
|Attributes|None|
|Default Value|None|
|Derived From|[Dw_Data_Measure_Groups](Dw_Data_Measure_Groups.md).[Notes](Dw_Data_Measure_Groups.md#notes)|
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


