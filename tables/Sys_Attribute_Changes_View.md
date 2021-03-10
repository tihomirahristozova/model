# View Sys_Attribute_Changes_View

Attribute values of an object change. Entity: Sys_Attribute_Changes_View

## Owner Tables Hierarchy

* [Sys_Object_Changes](Sys_Object_Changes.md)
* [Sys_Object_Changesets](Sys_Object_Changesets.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Object_Change_Id](#object_change_id)|`uniqueidentifier` |The object change|
|[Attribute_Name](#attribute_name)|`nvarchar(64)` |The attribute name|
|[New_Value](#new_value)|`nvarchar(2147483647)` |The new value|

## Columns

### Object_Change_Id


Object_Change_Id


The object change


The object change

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|yes|
|Referenced Table|[Sys_Object_Changes](Sys_Object_Changes.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sys_Attribute_Changes](Sys_Attribute_Changes.md).[Object_Change_Id](Sys_Attribute_Changes.md#object_change_id)|
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

### Attribute_Name


Attribute_Name


The attribute name


The attribute name

| Property | Value |
| - | - |
|Type|nvarchar(64)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sys_Attribute_Changes](Sys_Attribute_Changes.md).[Attribute_Name](Sys_Attribute_Changes.md#attribute_name)|
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
|Max Length|64|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### New_Value


New_Value


The new value


The new value

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
|Derived From|[Sys_Attribute_Changes](Sys_Attribute_Changes.md).[New_Value](Sys_Attribute_Changes.md#new_value)|
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

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|yes|
|Like|None|no|no|


