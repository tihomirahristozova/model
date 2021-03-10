# Table Eam_Managed_Asset_Types

Types of managed assets. Used to categorize the assets and the tracked parameters for each type. Entity: Eam_Managed_Asset_Types (Introduced in version 19.1)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Managed_Asset_Type_Id](#managed_asset_type_id)|`uniqueidentifier` `PK`|Types of Managed assets. Used to categorize the tracked parameters of the assets.|
|[Managed_Asset_Type_Code](#managed_asset_type_code)|`nvarchar(16)` |Unique code of the asset type.|
|[Managed_Asset_Type_Name](#managed_asset_type_name)|`nvarchar(254)` `ML`|Multilanguage name of the asset type.|
|[Notes](#notes)|`nvarchar(2147483647)` ||
|[Is_Active](#is_active)|`bit` |Specifies whether the asset type is active for choosing in drop-down choices.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Managed_Asset_Type_Id


Managed_Asset_Type_Id


Types of Managed assets. Used to categorize the tracked parameters of the assets.


Types of Managed assets. Used to categorize the tracked parameters of the assets.

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
|Derived From|[Eam_Managed_Asset_Types](Eam_Managed_Asset_Types.md).[Managed_Asset_Type_Id](Eam_Managed_Asset_Types.md#managed_asset_type_id)|
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

### Managed_Asset_Type_Code


Managed_Asset_Type_Code


Unique code of the asset type.


Unique code of the asset type.

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
|Derived From|[Eam_Managed_Asset_Types](Eam_Managed_Asset_Types.md).[Managed_Asset_Type_Code](Eam_Managed_Asset_Types.md#managed_asset_type_code)|
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
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|
|Like|None|no|no|

### Managed_Asset_Type_Name


Managed_Asset_Type_Name


Multilanguage name of the asset type.


Multilanguage name of the asset type.

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
|Derived From|[Eam_Managed_Asset_Types](Eam_Managed_Asset_Types.md).[Managed_Asset_Type_Name](Eam_Managed_Asset_Types.md#managed_asset_type_name)|
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
|Supports EQUALS_IN|yes|

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
|Derived From|[Eam_Managed_Asset_Types](Eam_Managed_Asset_Types.md).[Notes](Eam_Managed_Asset_Types.md#notes)|
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
|UI Memo Editor|yes|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Is_Active


Is_Active


Specifies whether the asset type is active for choosing in drop-down choices.


Specifies whether the asset type is active for choosing in drop-down choices.

| Property | Value |
| - | - |
|Type|bit|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|True|
|Derived From|[Eam_Managed_Asset_Types](Eam_Managed_Asset_Types.md).[Is_Active](Eam_Managed_Asset_Types.md#is_active)|
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
|Derived From|[Eam_Managed_Asset_Types](Eam_Managed_Asset_Types.md).[Row_Version](Eam_Managed_Asset_Types.md#row_version)|
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


