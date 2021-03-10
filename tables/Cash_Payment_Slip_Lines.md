# Table Cash_Payment_Slip_Lines

Mass payment line, which is distribution of an amount among payment orders. Each record generates one payment transaction line. Entity: Cash_Payment_Slip_Lines

## Owner Tables Hierarchy

* [Cash_Payment_Slip_Amounts](Cash_Payment_Slip_Amounts.md)
* [Cash_Payment_Slips](Cash_Payment_Slips.md)
* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Amount](#amount)|`decimal(10, 2)` |The part of the total amount in the payment slip amount, that is distributed to the specified payment order|
|[Covered_Order_Amount](#covered_order_amount)|`decimal(10, 2)` |The part of the original payment order amount, that is covered by this payment slip line|
|[Payment_Order_Id](#payment_order_id)|`uniqueidentifier` |The payment order, that is covered by this payment slip line|
|[Payment_Slip_Line_Id](#payment_slip_line_id)|`uniqueidentifier` `PK`||
|[Payment_Slip_Amount_Id](#payment_slip_amount_id)|`uniqueidentifier` Readonly||
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Amount


Amount


The part of the total amount in the payment slip amount, that is distributed to the specified payment order


The part of the total amount in the payment slip amount, that is distributed to the specified payment order

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
|Derived From|[Cash_Payment_Slip_Lines](Cash_Payment_Slip_Lines.md).[Amount](Cash_Payment_Slip_Lines.md#amount)|
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
|Order|0|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Covered_Order_Amount


Covered_Order_Amount


The part of the original payment order amount, that is covered by this payment slip line


The part of the original payment order amount, that is covered by this payment slip line

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
|Derived From|[Cash_Payment_Slip_Lines](Cash_Payment_Slip_Lines.md).[Covered_Order_Amount](Cash_Payment_Slip_Lines.md#covered_order_amount)|
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
|Supports EQUALS_IN|no|

### Payment_Order_Id


Payment_Order_Id


The payment order, that is covered by this payment slip line


The payment order, that is covered by this payment slip line

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
|Derived From|[Cash_Payment_Slip_Lines](Cash_Payment_Slip_Lines.md).[Payment_Order_Id](Cash_Payment_Slip_Lines.md#payment_order_id)|
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
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Payment_Slip_Line_Id


Payment_Slip_Line_Id

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
|Derived From|[Cash_Payment_Slip_Lines](Cash_Payment_Slip_Lines.md).[Payment_Slip_Line_Id](Cash_Payment_Slip_Lines.md#payment_slip_line_id)|
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

### Payment_Slip_Amount_Id


Payment_Slip_Amount_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|yes|
|Referenced Table|[Cash_Payment_Slip_Amounts](Cash_Payment_Slip_Amounts.md)|
|Readonly|yes|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Cash_Payment_Slip_Lines](Cash_Payment_Slip_Lines.md).[Payment_Slip_Amount_Id](Cash_Payment_Slip_Lines.md#payment_slip_amount_id)|
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
|Derived From|[Cash_Payment_Slip_Lines](Cash_Payment_Slip_Lines.md).[Row_Version](Cash_Payment_Slip_Lines.md#row_version)|
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


