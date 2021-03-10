# Table Ast_Depreciation_Plan_Templates

Specifies the default depreciation methods for the asset categories. Different methods can be specified for each valuation model. Entity: Ast_Depreciation_Plan_Templates

## Owner Tables Hierarchy

* [Ast_Asset_Categories](Ast_Asset_Categories.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Depreciation_Plan_Template_Id](#depreciation_plan_template_id)|`uniqueidentifier` `PK`||
|[Asset_Category_Id](#asset_category_id)|`uniqueidentifier` |Asset category for which this template is defined|
|[Valuation_Model_Id](#valuation_model_id)|`uniqueidentifier` |Valuation model for which this template is defined|
|[Depreciation_Method_Id](#depreciation_method_id)|`uniqueidentifier` |Depreciation method by default for the depreciation plans created by this template|
|[Asset_Life](#asset_life)|`int` |Asset life in months by default for the depreciation plans created by this template. NULL means that the asset is booked for this valuation model but is not depreciated in it (i.e. no depreciation plan is created).|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Depreciation_Plan_Template_Id


Depreciation_Plan_Template_Id

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
|Derived From|[Ast_Depreciation_Plan_Templates](Ast_Depreciation_Plan_Templates.md).[Depreciation_Plan_Template_Id](Ast_Depreciation_Plan_Templates.md#depreciation_plan_template_id)|
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

### Asset_Category_Id


Asset_Category_Id


Asset category for which this template is defined


Asset category for which this template is defined

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|yes|
|Referenced Table|[Ast_Asset_Categories](Ast_Asset_Categories.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Ast_Depreciation_Plan_Templates](Ast_Depreciation_Plan_Templates.md).[Asset_Category_Id](Ast_Depreciation_Plan_Templates.md#asset_category_id)|
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

### Valuation_Model_Id


Valuation_Model_Id


Valuation model for which this template is defined


Valuation model for which this template is defined

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Ast_Valuation_Models](Ast_Valuation_Models.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Ast_Depreciation_Plan_Templates](Ast_Depreciation_Plan_Templates.md).[Valuation_Model_Id](Ast_Depreciation_Plan_Templates.md#valuation_model_id)|
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

### Depreciation_Method_Id


Depreciation_Method_Id


Depreciation method by default for the depreciation plans created by this template


Depreciation method by default for the depreciation plans created by this template

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Ast_Depreciation_Methods](Ast_Depreciation_Methods.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Ast_Depreciation_Plan_Templates](Ast_Depreciation_Plan_Templates.md).[Depreciation_Method_Id](Ast_Depreciation_Plan_Templates.md#depreciation_method_id)|
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

### Asset_Life


Asset_Life


Asset life in months by default for the depreciation plans created by this template. NULL means that the asset is booked for this valuation model but is not depreciated in it (i.e. no depreciation plan is created).


Asset life in months by default for the depreciation plans created by this template. NULL means that the asset is booked for this valuation model but is not depreciated in it (i.e. no depreciation plan is created).

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
|Derived From|[Ast_Depreciation_Plan_Templates](Ast_Depreciation_Plan_Templates.md).[Asset_Life](Ast_Depreciation_Plan_Templates.md#asset_life)|
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
|UI Width|Short|
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
|Derived From|[Ast_Depreciation_Plan_Templates](Ast_Depreciation_Plan_Templates.md).[Row_Version](Ast_Depreciation_Plan_Templates.md#row_version)|
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


