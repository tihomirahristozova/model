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


Asset_Id


Asset for which changes in values have occurred.


Asset for which changes in values have occurred.

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
|Derived From|[Ast_Asset_Transaction_Lines](Ast_Asset_Transaction_Lines.md).[Asset_Id](Ast_Asset_Transaction_Lines.md#asset_id)|
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
|Order|1|
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


Valuation model in which the changes of the asset values have occurred (Taxation model or Accounting model or other).


Valuation model in which the changes of the asset values have occurred (Taxation model or Accounting model or other).

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
|Derived From|[Ast_Asset_Transaction_Lines](Ast_Asset_Transaction_Lines.md).[Valuation_Model_Id](Ast_Asset_Transaction_Lines.md#valuation_model_id)|
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

### Purchase_Value


Purchase_Value


Change in the purchase value of the asset (in the currency of the asset).


Change in the purchase value of the asset (in the currency of the asset).

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
|Derived From|[Ast_Asset_Transaction_Lines](Ast_Asset_Transaction_Lines.md).[Purchase_Value](Ast_Asset_Transaction_Lines.md#purchase_value)|
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
|Order|4|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Purchase_Value_Base


Purchase_Value_Base


Change in the purchase value of the asset (in the currency of the enterprise company).


Change in the purchase value of the asset (in the currency of the enterprise company).

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
|Derived From|[Ast_Asset_Transaction_Lines](Ast_Asset_Transaction_Lines.md).[Purchase_Value_Base](Ast_Asset_Transaction_Lines.md#purchase_value_base)|
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

### Depreciation_Value


Depreciation_Value


Change in the depreciation value of the asset (in the currency of the asset).


Change in the depreciation value of the asset (in the currency of the asset).

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
|Derived From|[Ast_Asset_Transaction_Lines](Ast_Asset_Transaction_Lines.md).[Depreciation_Value](Ast_Asset_Transaction_Lines.md#depreciation_value)|
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
|Order|6|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Depreciation_Value_Base


Depreciation_Value_Base


Change in the depreciation value of the asset (in the currency of the enterprise company).


Change in the depreciation value of the asset (in the currency of the enterprise company).

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
|Derived From|[Ast_Asset_Transaction_Lines](Ast_Asset_Transaction_Lines.md).[Depreciation_Value_Base](Ast_Asset_Transaction_Lines.md#depreciation_value_base)|
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
|Order|7|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Salvage_Value


Salvage_Value


Change in the salvage value of the asset (in the currency of the asset).


Change in the salvage value of the asset (in the currency of the asset).

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
|Derived From|[Ast_Asset_Transaction_Lines](Ast_Asset_Transaction_Lines.md).[Salvage_Value](Ast_Asset_Transaction_Lines.md#salvage_value)|
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
|Order|8|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Salvage_Value_Base


Salvage_Value_Base


Change in the salvage value of the asset (in the currency of the enterprise company).


Change in the salvage value of the asset (in the currency of the enterprise company).

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
|Derived From|[Ast_Asset_Transaction_Lines](Ast_Asset_Transaction_Lines.md).[Salvage_Value_Base](Ast_Asset_Transaction_Lines.md#salvage_value_base)|
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
|Order|9|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Positive_Reserve_Value


Positive_Reserve_Value


Change in the value of the positive reserve after asset valuations (in the currency of the asset).


Change in the value of the positive reserve after asset valuations (in the currency of the asset).

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
|Derived From|[Ast_Asset_Transaction_Lines](Ast_Asset_Transaction_Lines.md).[Positive_Reserve_Value](Ast_Asset_Transaction_Lines.md#positive_reserve_value)|
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
|Order|10|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Positive_Reserve_Value_Base


Positive_Reserve_Value_Base


Change in the value of the positive reserve after asset valuations (in the currency of the enterprise company).


Change in the value of the positive reserve after asset valuations (in the currency of the enterprise company).

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
|Derived From|[Ast_Asset_Transaction_Lines](Ast_Asset_Transaction_Lines.md).[Positive_Reserve_Value_Base](Ast_Asset_Transaction_Lines.md#positive_reserve_value_base)|
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
|Order|11|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Negative_Reserve_Value


Negative_Reserve_Value


Change in the value of the negative reserve after asset valuations (in the currency of the asset).


Change in the value of the negative reserve after asset valuations (in the currency of the asset).

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
|Derived From|[Ast_Asset_Transaction_Lines](Ast_Asset_Transaction_Lines.md).[Negative_Reserve_Value](Ast_Asset_Transaction_Lines.md#negative_reserve_value)|
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
|Order|12|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Negative_Reserve_Value_Base


Negative_Reserve_Value_Base


Change in the value of the negative reserve after asset valuations (in the currency of the enterprise company).


Change in the value of the negative reserve after asset valuations (in the currency of the enterprise company).

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
|Derived From|[Ast_Asset_Transaction_Lines](Ast_Asset_Transaction_Lines.md).[Negative_Reserve_Value_Base](Ast_Asset_Transaction_Lines.md#negative_reserve_value_base)|
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
|Order|13|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Asset_Transaction_Line_Id


Asset_Transaction_Line_Id


Unique identification of the asset transaction line.


Unique identification of the asset transaction line.

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
|Derived From|[Ast_Asset_Transaction_Lines](Ast_Asset_Transaction_Lines.md).[Asset_Transaction_Line_Id](Ast_Asset_Transaction_Lines.md#asset_transaction_line_id)|
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

### Asset_Transaction_Id


Asset_Transaction_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|yes|
|Referenced Table|[Ast_Asset_Transactions](Ast_Asset_Transactions.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Ast_Asset_Transaction_Lines](Ast_Asset_Transaction_Lines.md).[Asset_Transaction_Id](Ast_Asset_Transaction_Lines.md#asset_transaction_id)|
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

### Operation_Type


Operation_Type


Type of the current asset operation: PUR = Purchase, SLS = Sale, DEP = Depreciation, ADJ = Adjustment, REV = Reevaluation


Type of the current asset operation: PUR = Purchase, SLS = Sale, DEP = Depreciation, ADJ = Adjustment, REV = Reevaluation

| Property | Value |
| - | - |
|Type|nvarchar(3)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Allowed Values|`ADJ`, `DEP`, `PUR`, `SLS`, `REV`|
|Default Value|ADJ|
|Derived From|[Ast_Asset_Transaction_Lines](Ast_Asset_Transaction_Lines.md).[Operation_Type](Ast_Asset_Transaction_Lines.md#operation_type)|
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
|Max Length|3|
|Order|2147483647|
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
|Derived From|[Ast_Asset_Transaction_Lines](Ast_Asset_Transaction_Lines.md).[Row_Version](Ast_Asset_Transaction_Lines.md#row_version)|
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


