# Query Eam_Managed_Asset_Type_Tracked_Parameters_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Managed_Asset_Type_Tracked_Parameter_Id](#managed_asset_type_tracked_parameter_id)|`uniqueidentifier` `PK`||
|[Managed_Asset_Type_Id](#managed_asset_type_id)|`uniqueidentifier` |The asset type for which the tracked parameter is defined.|
|[Tracked_Parameter_Id](#tracked_parameter_id)|`uniqueidentifier` |The parameter, which will be tracked for assets of the specified type.|
|[Notes](#notes)|`nvarchar` ||

## Columns

### Managed_Asset_Type_Tracked_Parameter_Id


Managed_Asset_Type_Tracked_Parameter_Id

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
|Derived From|[Eam_Managed_Asset_Type_Tracked_Parameters](Eam_Managed_Asset_Type_Tracked_Parameters.md).[Managed_Asset_Type_Tracked_Parameter_Id](Eam_Managed_Asset_Type_Tracked_Parameters.md#managed_asset_type_tracked_parameter_id)|
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

### Managed_Asset_Type_Id


Managed_Asset_Type_Id


The asset type for which the tracked parameter is defined.


The asset type for which the tracked parameter is defined.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Eam_Managed_Asset_Types](Eam_Managed_Asset_Types.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Eam_Managed_Asset_Type_Tracked_Parameters](Eam_Managed_Asset_Type_Tracked_Parameters.md).[Managed_Asset_Type_Id](Eam_Managed_Asset_Type_Tracked_Parameters.md#managed_asset_type_id)|
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

### Tracked_Parameter_Id


Tracked_Parameter_Id


The parameter, which will be tracked for assets of the specified type.


The parameter, which will be tracked for assets of the specified type.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Eam_Tracked_Parameters](Eam_Tracked_Parameters.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Eam_Managed_Asset_Type_Tracked_Parameters](Eam_Managed_Asset_Type_Tracked_Parameters.md).[Tracked_Parameter_Id](Eam_Managed_Asset_Type_Tracked_Parameters.md#tracked_parameter_id)|
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
|Type|nvarchar|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Eam_Managed_Asset_Type_Tracked_Parameters](Eam_Managed_Asset_Type_Tracked_Parameters.md).[Notes](Eam_Managed_Asset_Type_Tracked_Parameters.md#notes)|
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


