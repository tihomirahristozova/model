# Table Cash_Payment_Slip_Payment_Transactions_Templates

Contains options for generation of payment transactions. Each option set is assigned to specific generation route. Entity: Cash_Payment_Slip_Payment_Transactions_Templates (Introduced in version 19.1)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Id](#id)|`uniqueidentifier` `PK`||
|[Route_Id](#route_id)|`uniqueidentifier` |The route to which the current option set is assigned.|
|[CreateIncomePayments](#createincomepayments)|`bit` |True if the generation creates payment transactions for Payment Slip Amounts with direction Income.|
|[CreateExpensePayments](#createexpensepayments)|`bit` |True if the generation creates payment transactions for Payment Slip Amounts with direction Expense.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Id


Id

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
|Default Value|None|
|Derived From|[Cash_Payment_Slip_Payment_Transactions_Templates](Cash_Payment_Slip_Payment_Transactions_Templates.md).[Id](Cash_Payment_Slip_Payment_Transactions_Templates.md#id)|
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

### Route_Id


Route_Id


The route to which the current option set is assigned.


The route to which the current option set is assigned.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Wf_Routes](Wf_Routes.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Cash_Payment_Slip_Payment_Transactions_Templates](Cash_Payment_Slip_Payment_Transactions_Templates.md).[Route_Id](Cash_Payment_Slip_Payment_Transactions_Templates.md#route_id)|
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

### CreateIncomePayments


CreateIncomePayments


True if the generation creates payment transactions for Payment Slip Amounts with direction Income.


True if the generation creates payment transactions for Payment Slip Amounts with direction Income.

| Property | Value |
| - | - |
|Type|bit|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Cash_Payment_Slip_Payment_Transactions_Templates](Cash_Payment_Slip_Payment_Transactions_Templates.md).[CreateIncomePayments](Cash_Payment_Slip_Payment_Transactions_Templates.md#createincomepayments)|
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

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### CreateExpensePayments


CreateExpensePayments


True if the generation creates payment transactions for Payment Slip Amounts with direction Expense.


True if the generation creates payment transactions for Payment Slip Amounts with direction Expense.

| Property | Value |
| - | - |
|Type|bit|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Cash_Payment_Slip_Payment_Transactions_Templates](Cash_Payment_Slip_Payment_Transactions_Templates.md).[CreateExpensePayments](Cash_Payment_Slip_Payment_Transactions_Templates.md#createexpensepayments)|
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
|Derived From|[Cash_Payment_Slip_Payment_Transactions_Templates](Cash_Payment_Slip_Payment_Transactions_Templates.md).[Row_Version](Cash_Payment_Slip_Payment_Transactions_Templates.md#row_version)|
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


