# Table Cash_Payment_Transaction_Lines

Contains the distibution of the payments' amounts among the source payment orders. Entity: Cash_Payment_Transaction_Lines

## Owner Tables Hierarchy

* [Cash_Payment_Transactions](Cash_Payment_Transactions.md)
* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Amount](#amount)|`decimal(10, 2)` |The part of the total payed amount by the transaction, that is distributed to the specified payment order|
|[Covered_Order_Amount](#covered_order_amount)|`decimal(10, 2)` |The part of the original payment order amount, that is covered by this transaction line|
|[Payment_Order_Id](#payment_order_id)|`uniqueidentifier` |The payment order, that is covered by this transaction amount distribution (tr.line)|
|[Payment_Transaction_Line_Id](#payment_transaction_line_id)|`uniqueidentifier` `PK`||
|[Payment_Transaction_Id](#payment_transaction_id)|`uniqueidentifier` ||
|[Notes](#notes)|`nvarchar(254)` ||
|[Allow_Overpayment](#allow_overpayment)|`bit` |1-Allows overpayment for the payment order; 0=Does not allow (default)|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Amount


Amount


The part of the total payed amount by the transaction, that is distributed to the specified payment order


The part of the total payed amount by the transaction, that is distributed to the specified payment order

| Property | Value |
| - | - |
|Type|decimal(10, 2)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|0|
|Derived From|[Cash_Payment_Transaction_Lines](Cash_Payment_Transaction_Lines.md).[Amount](Cash_Payment_Transaction_Lines.md#amount)|
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
|Order|0|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Covered_Order_Amount


Covered_Order_Amount


The part of the original payment order amount, that is covered by this transaction line


The part of the original payment order amount, that is covered by this transaction line

| Property | Value |
| - | - |
|Type|decimal(10, 2)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|0|
|Derived From|[Cash_Payment_Transaction_Lines](Cash_Payment_Transaction_Lines.md).[Covered_Order_Amount](Cash_Payment_Transaction_Lines.md#covered_order_amount)|
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
|Order|1|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Payment_Order_Id


Payment_Order_Id


The payment order, that is covered by this transaction amount distribution (tr.line)


The payment order, that is covered by this transaction amount distribution (tr.line)

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Cash_Payment_Orders](Cash_Payment_Orders.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Cash_Payment_Transaction_Lines](Cash_Payment_Transaction_Lines.md).[Payment_Order_Id](Cash_Payment_Transaction_Lines.md#payment_order_id)|
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
|UI Width|Long|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Payment_Transaction_Line_Id


Payment_Transaction_Line_Id

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
|Derived From|[Cash_Payment_Transaction_Lines](Cash_Payment_Transaction_Lines.md).[Payment_Transaction_Line_Id](Cash_Payment_Transaction_Lines.md#payment_transaction_line_id)|
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

### Payment_Transaction_Id


Payment_Transaction_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|yes|
|Referenced Table|[Cash_Payment_Transactions](Cash_Payment_Transactions.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Cash_Payment_Transaction_Lines](Cash_Payment_Transaction_Lines.md).[Payment_Transaction_Id](Cash_Payment_Transaction_Lines.md#payment_transaction_id)|
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

### Notes


Notes

| Property | Value |
| - | - |
|Type|nvarchar(254)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Cash_Payment_Transaction_Lines](Cash_Payment_Transaction_Lines.md).[Notes](Cash_Payment_Transaction_Lines.md#notes)|
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
|Max Length|254|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Allow_Overpayment


Allow_Overpayment


1-Allows overpayment for the payment order; 0=Does not allow (default)


1-Allows overpayment for the payment order; 0=Does not allow (default)

| Property | Value |
| - | - |
|Type|bit|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|False|
|Derived From|[Cash_Payment_Transaction_Lines](Cash_Payment_Transaction_Lines.md).[Allow_Overpayment](Cash_Payment_Transaction_Lines.md#allow_overpayment)|
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
|Derived From|[Cash_Payment_Transaction_Lines](Cash_Payment_Transaction_Lines.md).[Row_Version](Cash_Payment_Transaction_Lines.md#row_version)|
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


