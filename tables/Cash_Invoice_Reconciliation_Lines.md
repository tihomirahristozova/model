# Table Cash_Invoice_Reconciliation_Lines


## Owner Tables Hierarchy

* [Cash_Invoice_Reconciliations](Cash_Invoice_Reconciliations.md)
* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Invoice_Reconciliation_Line_Id](#invoice_reconciliation_line_id)|`uniqueidentifier` `PK`||
|[Invoice_Reconciliation_Id](#invoice_reconciliation_id)|`uniqueidentifier` ||
|[Invoice_Document_Id](#invoice_document_id)|`uniqueidentifier` |Obsolete. Not used.|
|[Payment_Transaction_Document_Id](#payment_transaction_document_id)|`uniqueidentifier` |Obsolete. Not used.|
|[Covered_Invoice_Amount](#covered_invoice_amount)|`decimal(14, 2)` |Amount from the invoice that is covered by the payment. The amount is in the currency of the invoice.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Invoice_Reconciliation_Line_Id


Invoice_Reconciliation_Line_Id

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
|Derived From|[Cash_Invoice_Reconciliation_Lines](Cash_Invoice_Reconciliation_Lines.md).[Invoice_Reconciliation_Line_Id](Cash_Invoice_Reconciliation_Lines.md#invoice_reconciliation_line_id)|
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

### Invoice_Reconciliation_Id


Invoice_Reconciliation_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|yes|
|Referenced Table|[Cash_Invoice_Reconciliations](Cash_Invoice_Reconciliations.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Cash_Invoice_Reconciliation_Lines](Cash_Invoice_Reconciliation_Lines.md).[Invoice_Reconciliation_Id](Cash_Invoice_Reconciliation_Lines.md#invoice_reconciliation_id)|
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

### Invoice_Document_Id


Invoice_Document_Id


Obsolete. Not used.


Obsolete. Not used.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Documents](Gen_Documents.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Cash_Invoice_Reconciliation_Lines](Cash_Invoice_Reconciliation_Lines.md).[Invoice_Document_Id](Cash_Invoice_Reconciliation_Lines.md#invoice_document_id)|
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

### Payment_Transaction_Document_Id


Payment_Transaction_Document_Id


Obsolete. Not used.


Obsolete. Not used.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Documents](Gen_Documents.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Cash_Invoice_Reconciliation_Lines](Cash_Invoice_Reconciliation_Lines.md).[Payment_Transaction_Document_Id](Cash_Invoice_Reconciliation_Lines.md#payment_transaction_document_id)|
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

### Covered_Invoice_Amount


Covered_Invoice_Amount


Amount from the invoice that is covered by the payment. The amount is in the currency of the invoice.


Amount from the invoice that is covered by the payment. The amount is in the currency of the invoice.

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
|Derived From|[Cash_Invoice_Reconciliation_Lines](Cash_Invoice_Reconciliation_Lines.md).[Covered_Invoice_Amount](Cash_Invoice_Reconciliation_Lines.md#covered_invoice_amount)|
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
|Derived From|[Cash_Invoice_Reconciliation_Lines](Cash_Invoice_Reconciliation_Lines.md).[Row_Version](Cash_Invoice_Reconciliation_Lines.md#row_version)|
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


