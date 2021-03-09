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

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Depreciation_Plan_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Line_No

| Property | Value |
| - | - |
|Type|int|

### Valuation_Model_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Asset_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Plan_Depreciation_Value

| Property | Value |
| - | - |
|Type|decimal(14, 2)|

### Depreciation_Start_Date

| Property | Value |
| - | - |
|Type|datetime|

### Depreciation_End_Date

| Property | Value |
| - | - |
|Type|datetime|

### Depreciation_Method_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


