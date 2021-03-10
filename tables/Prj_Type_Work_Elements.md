# Table Prj_Type_Work_Elements

The work elements of the work breakdown structure of each project type. Entity: Prj_Type_Work_Elements

## Owner Tables Hierarchy

* [Prj_Types](Prj_Types.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Project_Type_Work_Element_Id](#project_type_work_element_id)|`uniqueidentifier` `PK`||
|[Project_Type_Id](#project_type_id)|`uniqueidentifier` ||
|[Parent_Full_Path](#parent_full_path)|`nvarchar(25)` |The full path of the parent work element in this project type. NULL when this is root element.|
|[Work_Element_Code](#work_element_code)|`nvarchar(3)` |The code of the work element, unique among the sibling elements within the parent work element.|
|[Work_Element_Name](#work_element_name)|`nvarchar(254)` |The name of the work element, unique among the sibling elements within the parent work element.|
|[Notes](#notes)|`nvarchar(2147483647)` ||
|[Full_Path](#full_path)|`nvarchar(25)` Readonly|The full path of the node in the format of dot-delimited, dot-terminated codes of the parents.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Project_Type_Work_Element_Id


Project_Type_Work_Element_Id

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
|Derived From|[Prj_Type_Work_Elements](Prj_Type_Work_Elements.md).[Project_Type_Work_Element_Id](Prj_Type_Work_Elements.md#project_type_work_element_id)|
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

### Project_Type_Id


Project_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|yes|
|Referenced Table|[Prj_Types](Prj_Types.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Prj_Type_Work_Elements](Prj_Type_Work_Elements.md).[Project_Type_Id](Prj_Type_Work_Elements.md#project_type_id)|
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

### Parent_Full_Path


Parent_Full_Path


The full path of the parent work element in this project type. NULL when this is root element.


The full path of the parent work element in this project type. NULL when this is root element.

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
|Derived From|[Prj_Type_Work_Elements](Prj_Type_Work_Elements.md).[Parent_Full_Path](Prj_Type_Work_Elements.md#parent_full_path)|
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
|Equals|NULL|yes|yes|
|Like|None|no|no|

### Work_Element_Code


Work_Element_Code


The code of the work element, unique among the sibling elements within the parent work element.


The code of the work element, unique among the sibling elements within the parent work element.

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
|Derived From|[Prj_Type_Work_Elements](Prj_Type_Work_Elements.md).[Work_Element_Code](Prj_Type_Work_Elements.md#work_element_code)|
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

### Work_Element_Name


Work_Element_Name


The name of the work element, unique among the sibling elements within the parent work element.


The name of the work element, unique among the sibling elements within the parent work element.

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
|Derived From|[Prj_Type_Work_Elements](Prj_Type_Work_Elements.md).[Work_Element_Name](Prj_Type_Work_Elements.md#work_element_name)|
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
|Derived From|[Prj_Type_Work_Elements](Prj_Type_Work_Elements.md).[Notes](Prj_Type_Work_Elements.md#notes)|
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
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Prj_Type_Work_Elements](Prj_Type_Work_Elements.md).[Full_Path](Prj_Type_Work_Elements.md#full_path)|
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
|Equals|NULL|yes|yes|
|Like|None|no|no|

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
|Derived From|[Prj_Type_Work_Elements](Prj_Type_Work_Elements.md).[Row_Version](Prj_Type_Work_Elements.md#row_version)|
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


