# Table Fleet_Vehicle_Set_Vehicles

Contains lists of vehicles in the vehicle sets. Entity: Fleet_Vehicle_Set_Vehicles

## Owner Tables Hierarchy

* [Fleet_Vehicle_Sets](Fleet_Vehicle_Sets.md)
* [Gen_Enterprise_Companies](Gen_Enterprise_Companies.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Vehicle_Set_Vehicle_Id](#vehicle_set_vehicle_id)|`uniqueidentifier` `PK`||
|[Vehicle_Set_Id](#vehicle_set_id)|`uniqueidentifier` ||
|[Vehicle_Id](#vehicle_id)|`uniqueidentifier` |The Vehicle which is part of the vehicle set|
|[Notes](#notes)|`nvarchar(254)` ||
|[Ordinal_Pos](#ordinal_pos)|`int` |Ordinal position of the vehicle within the vehicle set. Position 0 has special meaning - this is the leading vehicle|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Vehicle_Set_Vehicle_Id


Vehicle_Set_Vehicle_Id

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
|Derived From|[Fleet_Vehicle_Set_Vehicles](Fleet_Vehicle_Set_Vehicles.md).[Vehicle_Set_Vehicle_Id](Fleet_Vehicle_Set_Vehicles.md#vehicle_set_vehicle_id)|
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

### Vehicle_Set_Id


Vehicle_Set_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|yes|
|Referenced Table|[Fleet_Vehicle_Sets](Fleet_Vehicle_Sets.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Fleet_Vehicle_Set_Vehicles](Fleet_Vehicle_Set_Vehicles.md).[Vehicle_Set_Id](Fleet_Vehicle_Set_Vehicles.md#vehicle_set_id)|
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

### Vehicle_Id


Vehicle_Id


The Vehicle which is part of the vehicle set


The Vehicle which is part of the vehicle set

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Fleet_Vehicles](Fleet_Vehicles.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Fleet_Vehicle_Set_Vehicles](Fleet_Vehicle_Set_Vehicles.md).[Vehicle_Id](Fleet_Vehicle_Set_Vehicles.md#vehicle_id)|
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

### Notes


Notes

| Property | Value |
| - | - |
|Type|nvarchar(254)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Fleet_Vehicle_Set_Vehicles](Fleet_Vehicle_Set_Vehicles.md).[Notes](Fleet_Vehicle_Set_Vehicles.md#notes)|
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
|Like|None|no|no|

### Ordinal_Pos


Ordinal_Pos


Ordinal position of the vehicle within the vehicle set. Position 0 has special meaning - this is the leading vehicle


Ordinal position of the vehicle within the vehicle set. Position 0 has special meaning - this is the leading vehicle

| Property | Value |
| - | - |
|Type|int|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Fleet_Vehicle_Set_Vehicles](Fleet_Vehicle_Set_Vehicles.md).[Ordinal_Pos](Fleet_Vehicle_Set_Vehicles.md#ordinal_pos)|
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

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|GreaterThanOrLessThan|None|no|no|

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
|Derived From|[Fleet_Vehicle_Set_Vehicles](Fleet_Vehicle_Set_Vehicles.md).[Row_Version](Fleet_Vehicle_Set_Vehicles.md#row_version)|
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


