# Table Ast_Valuation_Models

Valuation models stand for the different valuations an asset can have. For example Accounting, Tax, External Financial Reports, etc. All asset transactions are posted for specific valuation model, but are usually automatically copied to other models. Entity: Ast_Valuation_Models

## Summary

| Name | Type | Description |
| - | - | --- |
|[Valuation_Model_Id](#valuation_model_id)|`uniqueidentifier` `PK`||
|[Valuation_Model_Name](#valuation_model_name)|`nvarchar(254)` `ML`||
|[Default_Depreciation_Method_Id](#default_depreciation_method_id)|`uniqueidentifier` |Obsolete. Not used.|
|[Is_System](#is_system)|`bit` Readonly|Is_System is True for those valuation models that are managed by the system via update procedures and cannot be edited by the user.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Valuation_Model_Id


Valuation_Model_Id

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
|Derived From|[Ast_Valuation_Models](Ast_Valuation_Models.md).[Valuation_Model_Id](Ast_Valuation_Models.md#valuation_model_id)|
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
|Order|1|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Valuation_Model_Name


Valuation_Model_Name

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
|Derived From|[Ast_Valuation_Models](Ast_Valuation_Models.md).[Valuation_Model_Name](Ast_Valuation_Models.md#valuation_model_name)|
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
|Order|2|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Long|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Like|None|no|no|

### Default_Depreciation_Method_Id


Default_Depreciation_Method_Id


Obsolete. Not used.


Obsolete. Not used.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Ast_Depreciation_Methods](Ast_Depreciation_Methods.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Ast_Valuation_Models](Ast_Valuation_Models.md).[Default_Depreciation_Method_Id](Ast_Valuation_Models.md#default_depreciation_method_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|3|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Is_System


Is_System


Is_System is True for those valuation models that are managed by the system via update procedures and cannot be edited by the user.


Is_System is True for those valuation models that are managed by the system via update procedures and cannot be edited by the user.

| Property | Value |
| - | - |
|Type|bit|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|yes|
|Sortable|no|
|Attributes|None|
|Default Value|False|
|Derived From|[Ast_Valuation_Models](Ast_Valuation_Models.md).[Is_System](Ast_Valuation_Models.md#is_system)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|4|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Short|
|Supports EQUALS_IN|no|

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
|Derived From|[Ast_Valuation_Models](Ast_Valuation_Models.md).[Row_Version](Ast_Valuation_Models.md#row_version)|
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


