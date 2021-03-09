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

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Valuation_Model_Name

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Default_Depreciation_Method_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Is_System

| Property | Value |
| - | - |
|Type|bit|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


