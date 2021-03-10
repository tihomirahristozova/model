# Table Ast_Depreciation_Plan_Lines

Each record contains one depreciation plan for one valuation model of one asset. Entity: Ast_Depreciation_Plan_Lines

## Owner Tables Hierarchy

* [Ast_Depreciation_Plans](Ast_Depreciation_Plans.md)
* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Depreciation_Plan_Line_Id](#depreciation_plan_line_id)|`uniqueidentifier` `PK`||
|[Depreciation_Plan_Id](#depreciation_plan_id)|`uniqueidentifier` ||
|[Line_No](#line_no)|`int` |Consecutive number of the line within the depreciation plan|
|[Valuation_Model_Id](#valuation_model_id)|`uniqueidentifier` |Valuation model in which the asset is accounted|
|[Asset_Id](#asset_id)|`uniqueidentifier` |The asset that is planned for depreciation|
|[Plan_Depreciation_Value](#plan_depreciation_value)|`decimal(14, 2)` |The part of the total amount of the asset (in the currency of the asset), which is due for depreciation.|
|[Depreciation_Start_Date](#depreciation_start_date)|`datetime` |Start date of the depreciation plan for this asset|
|[Depreciation_End_Date](#depreciation_end_date)|`datetime` |End date of the depreciation plan for this asset|
|[Depreciation_Method_Id](#depreciation_method_id)|`uniqueidentifier` |Depreciation method by which the asset will be depreciated|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Depreciation_Plan_Line_Id


Depreciation_Plan_Line_Id

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
|Derived From|[Ast_Depreciation_Plan_Lines](Ast_Depreciation_Plan_Lines.md).[Depreciation_Plan_Line_Id](Ast_Depreciation_Plan_Lines.md#depreciation_plan_line_id)|
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
|Order|0|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|yes|

### Depreciation_Plan_Id


Depreciation_Plan_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|yes|
|Referenced Table|[Ast_Depreciation_Plans](Ast_Depreciation_Plans.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Ast_Depreciation_Plan_Lines](Ast_Depreciation_Plan_Lines.md).[Depreciation_Plan_Id](Ast_Depreciation_Plan_Lines.md#depreciation_plan_id)|
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
|Equals|NULL|no|yes|

### Line_No


Line_No


Consecutive number of the line within the depreciation plan


Consecutive number of the line within the depreciation plan

| Property | Value |
| - | - |
|Type|int|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Autoincrement|10|
|Derived From|[Ast_Depreciation_Plan_Lines](Ast_Depreciation_Plan_Lines.md).[Line_No](Ast_Depreciation_Plan_Lines.md#line_no)|
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
|Order|2|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Short|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|yes|

### Valuation_Model_Id


Valuation_Model_Id


Valuation model in which the asset is accounted


Valuation model in which the asset is accounted

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
|Derived From|[Ast_Depreciation_Plan_Lines](Ast_Depreciation_Plan_Lines.md).[Valuation_Model_Id](Ast_Depreciation_Plan_Lines.md#valuation_model_id)|
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
|Order|3|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Asset_Id


Asset_Id


The asset that is planned for depreciation


The asset that is planned for depreciation

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Ast_Assets](Ast_Assets.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Ast_Depreciation_Plan_Lines](Ast_Depreciation_Plan_Lines.md).[Asset_Id](Ast_Depreciation_Plan_Lines.md#asset_id)|
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
|Order|4|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Plan_Depreciation_Value


Plan_Depreciation_Value


The part of the total amount of the asset (in the currency of the asset), which is due for depreciation.


The part of the total amount of the asset (in the currency of the asset), which is due for depreciation.

| Property | Value |
| - | - |
|Type|decimal(14, 2)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|0|
|Derived From|[Ast_Depreciation_Plan_Lines](Ast_Depreciation_Plan_Lines.md).[Plan_Depreciation_Value](Ast_Depreciation_Plan_Lines.md#plan_depreciation_value)|
|Format|N2|
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
|Order|5|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Depreciation_Start_Date


Depreciation_Start_Date


Start date of the depreciation plan for this asset


Start date of the depreciation plan for this asset

| Property | Value |
| - | - |
|Type|datetime|
|DateTime Format|DateTime|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Ast_Depreciation_Plan_Lines](Ast_Depreciation_Plan_Lines.md).[Depreciation_Start_Date](Ast_Depreciation_Plan_Lines.md#depreciation_start_date)|
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
|Order|6|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Depreciation_End_Date


Depreciation_End_Date


End date of the depreciation plan for this asset


End date of the depreciation plan for this asset

| Property | Value |
| - | - |
|Type|datetime|
|DateTime Format|DateTime|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Ast_Depreciation_Plan_Lines](Ast_Depreciation_Plan_Lines.md).[Depreciation_End_Date](Ast_Depreciation_Plan_Lines.md#depreciation_end_date)|
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
|Order|7|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Depreciation_Method_Id


Depreciation_Method_Id


Depreciation method by which the asset will be depreciated


Depreciation method by which the asset will be depreciated

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
|Derived From|[Ast_Depreciation_Plan_Lines](Ast_Depreciation_Plan_Lines.md).[Depreciation_Method_Id](Ast_Depreciation_Plan_Lines.md#depreciation_method_id)|
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
|Order|8|
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
|Derived From|[Ast_Depreciation_Plan_Lines](Ast_Depreciation_Plan_Lines.md).[Row_Version](Ast_Depreciation_Plan_Lines.md#row_version)|
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


