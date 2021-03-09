# Table Ast_Asset_Transaction_Lines

Asset value transaction lines. Each line changes the values of one asset in one valuation model. Entity: Ast_Asset_Transaction_Lines

## Owner Tables Hierarchy

* [Ast_Asset_Transactions](Ast_Asset_Transactions.md)
* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Asset_Id](#asset_id)|`uniqueidentifier` |Asset for which changes in values have occurred.|
|[Valuation_Model_Id](#valuation_model_id)|`uniqueidentifier` |Valuation model in which the changes of the asset values have occurred (Taxation model or Accounting model or other).|
|[Purchase_Value](#purchase_value)|`decimal(14, 2)` |Change in the purchase value of the asset (in the currency of the asset).|
|[Purchase_Value_Base](#purchase_value_base)|`decimal(14, 2)` |Change in the purchase value of the asset (in the currency of the enterprise company).|
|[Depreciation_Value](#depreciation_value)|`decimal(14, 2)` |Change in the depreciation value of the asset (in the currency of the asset).|
|[Depreciation_Value_Base](#depreciation_value_base)|`decimal(14, 2)` |Change in the depreciation value of the asset (in the currency of the enterprise company).|
|[Salvage_Value](#salvage_value)|`decimal(14, 2)` |Change in the salvage value of the asset (in the currency of the asset).|
|[Salvage_Value_Base](#salvage_value_base)|`decimal(14, 2)` |Change in the salvage value of the asset (in the currency of the enterprise company).|
|[Positive_Reserve_Value](#positive_reserve_value)|`decimal(14, 2)` |Change in the value of the positive reserve after asset valuations (in the currency of the asset).|
|[Positive_Reserve_Value_Base](#positive_reserve_value_base)|`decimal(14, 2)` |Change in the value of the positive reserve after asset valuations (in the currency of the enterprise company).|
|[Negative_Reserve_Value](#negative_reserve_value)|`decimal(14, 2)` |Change in the value of the negative reserve after asset valuations (in the currency of the asset).|
|[Negative_Reserve_Value_Base](#negative_reserve_value_base)|`decimal(14, 2)` |Change in the value of the negative reserve after asset valuations (in the currency of the enterprise company).|
|[Asset_Transaction_Line_Id](#asset_transaction_line_id)|`uniqueidentifier` `PK`|Unique identification of the asset transaction line.|
|[Asset_Transaction_Id](#asset_transaction_id)|`uniqueidentifier` ||
|[Operation_Type](#operation_type)|`nvarchar(3)` Allowed: `ADJ`, `DEP`, `PUR`, `SLS`, `REV`|Type of the current asset operation: PUR = Purchase, SLS = Sale, DEP = Depreciation, ADJ = Adjustment, REV = Reevaluation|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Asset_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Valuation_Model_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Purchase_Value

| Property | Value |
| - | - |
|Type|decimal(14, 2)|

### Purchase_Value_Base

| Property | Value |
| - | - |
|Type|decimal(14, 2)|

### Depreciation_Value

| Property | Value |
| - | - |
|Type|decimal(14, 2)|

### Depreciation_Value_Base

| Property | Value |
| - | - |
|Type|decimal(14, 2)|

### Salvage_Value

| Property | Value |
| - | - |
|Type|decimal(14, 2)|

### Salvage_Value_Base

| Property | Value |
| - | - |
|Type|decimal(14, 2)|

### Positive_Reserve_Value

| Property | Value |
| - | - |
|Type|decimal(14, 2)|

### Positive_Reserve_Value_Base

| Property | Value |
| - | - |
|Type|decimal(14, 2)|

### Negative_Reserve_Value

| Property | Value |
| - | - |
|Type|decimal(14, 2)|

### Negative_Reserve_Value_Base

| Property | Value |
| - | - |
|Type|decimal(14, 2)|

### Asset_Transaction_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Asset_Transaction_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Operation_Type

| Property | Value |
| - | - |
|Type|nvarchar(3)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


