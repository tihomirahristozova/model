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

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Asset_Category_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Valuation_Model_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Depreciation_Method_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Asset_Life

| Property | Value |
| - | - |
|Type|int|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


