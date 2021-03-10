# Table Prj_Template_Work_Elements

Contains project work elements, which shall be copied to projects, based on the specified template. Entity: Prj_Template_Work_Elements

## Owner Tables Hierarchy

* [Prj_Templates](Prj_Templates.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Project_Template_Work_Element_Id](#project_template_work_element_id)|`uniqueidentifier` `PK`||
|[Project_Template_Id](#project_template_id)|`uniqueidentifier` ||
|[Project_Type_Work_Element_Id](#project_type_work_element_id)|`uniqueidentifier` |The work element from the project type, which shall be copied as work element in new projects, based on this template.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Project_Template_Work_Element_Id


Project_Template_Work_Element_Id

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
|Derived From|[Prj_Template_Work_Elements](Prj_Template_Work_Elements.md).[Project_Template_Work_Element_Id](Prj_Template_Work_Elements.md#project_template_work_element_id)|
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

### Project_Template_Id


Project_Template_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|yes|
|Referenced Table|[Prj_Templates](Prj_Templates.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Prj_Template_Work_Elements](Prj_Template_Work_Elements.md).[Project_Template_Id](Prj_Template_Work_Elements.md#project_template_id)|
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

### Project_Type_Work_Element_Id


Project_Type_Work_Element_Id


The work element from the project type, which shall be copied as work element in new projects, based on this template.


The work element from the project type, which shall be copied as work element in new projects, based on this template.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Prj_Type_Work_Elements](Prj_Type_Work_Elements.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Prj_Template_Work_Elements](Prj_Template_Work_Elements.md).[Project_Type_Work_Element_Id](Prj_Template_Work_Elements.md#project_type_work_element_id)|
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
|Derived From|[Prj_Template_Work_Elements](Prj_Template_Work_Elements.md).[Row_Version](Prj_Template_Work_Elements.md#row_version)|
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


