# Query Inv_Transaction_Cost_Corrections_Select


## Summary

| Name | Type | Description |
| - | - | --- |
|[Transaction_Id](#transaction_id)|`uniqueidentifier` |Unique Transaction Id|
|[Transaction_Line_Id](#transaction_line_id)|`uniqueidentifier` `PK`|The transaction line, which is corrected.|
|[Cost_Correction_Amount](#cost_correction_amount)|`decimal(0, 0)` |The amount of correction (plus or minus) for the Amount field of the transaction line.|
|[Product_Cost_Adjustment](#product_cost_adjustment)|`decimal(0, 0)` |The amount of correction (plus or minus) for the Product Cost field of the transaction line.|
|[Store_Cost_Adjustment](#store_cost_adjustment)|`decimal(0, 0)` |The amount of correction (plus or minus) for the Store Cost field of the transaction line.|
|[Base_Cost_Adjustment](#base_cost_adjustment)|`decimal(0, 0)` |The amount of correction (plus or minus) for the Base Cost field of the transaction line.|

## Columns

### Transaction_Id


Transaction_Id


Unique Transaction Id


Unique Transaction Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Inv_Transactions](Inv_Transactions.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Inv_Transaction_Lines](Inv_Transaction_Lines.md).[Transaction_Id](Inv_Transaction_Lines.md#transaction_id)|
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

### Transaction_Line_Id


Transaction_Line_Id


The transaction line, which is corrected.


The transaction line, which is corrected.

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
|Derived From|[Inv_Transaction_Lines](Inv_Transaction_Lines.md).[Transaction_Line_Id](Inv_Transaction_Lines.md#transaction_line_id)|
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

### Cost_Correction_Amount


Cost_Correction_Amount


The amount of correction (plus or minus) for the Amount field of the transaction line.


The amount of correction (plus or minus) for the Amount field of the transaction line.

| Property | Value |
| - | - |
|Type|decimal(0, 0)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Format|#,##0.00|
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

### Product_Cost_Adjustment


Product_Cost_Adjustment


The amount of correction (plus or minus) for the Product Cost field of the transaction line.


The amount of correction (plus or minus) for the Product Cost field of the transaction line.

| Property | Value |
| - | - |
|Type|decimal(0, 0)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Format|#,##0.00|
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

### Store_Cost_Adjustment


Store_Cost_Adjustment


The amount of correction (plus or minus) for the Store Cost field of the transaction line.


The amount of correction (plus or minus) for the Store Cost field of the transaction line.

| Property | Value |
| - | - |
|Type|decimal(0, 0)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Format|#,##0.00|
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

### Base_Cost_Adjustment


Base_Cost_Adjustment


The amount of correction (plus or minus) for the Base Cost field of the transaction line.


The amount of correction (plus or minus) for the Base Cost field of the transaction line.

| Property | Value |
| - | - |
|Type|decimal(0, 0)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Format|#,##0.00|
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


