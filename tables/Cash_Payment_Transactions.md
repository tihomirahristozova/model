# Table Cash_Payment_Transactions

Represents actual payments, which increase or decrease the balance of a payment account. Entity: Cash_Payment_Transactions

## Owner Tables Hierarchy

* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Party_Id](#party_id)|`uniqueidentifier` |The party that is paying or receiving the money|
|[Payment_Account_Id](#payment_account_id)|`uniqueidentifier` |The account towards which the payment was effected|
|[Direction](#direction)|`nvarchar(1)` Allowed: `I`, `R`|I for Payment issue, R for payment receipt|
|[Total_Amount](#total_amount)|`decimal(18, 2)` |The total amount payed. The distribution of the amount among source orders is specified with payment transacion lines|
|[Total_Amount_Currency_Id](#total_amount_currency_id)|`uniqueidentifier` |The currency of the total amount|
|[Requires_Allocation](#requires_allocation)|`bit` |1=The total amount should be allocated to payment orders; 0=Payment orders are not required|
|[Payment_Slip_No](#payment_slip_no)|`nvarchar(20)` |The number of the payment slip. Can be used to directly indicate the number without referring to Payment_Slips|
|[Payment_Slip_Id](#payment_slip_id)|`uniqueidentifier` |When not NULL specifies that this payment was part of a payment slip|
|[Notes](#notes)|`nvarchar(254)` ||
|[Payment_Transaction_Id](#payment_transaction_id)|`uniqueidentifier` `PK`||
|[Document_Id](#document_id)|`uniqueidentifier` |The document data of the payment transaction|
|[Original_Payment_Transaction_Id](#original_payment_transaction_id)|`uniqueidentifier` |Original Payment Transaction|
|[Payment_Reason_Id](#payment_reason_id)|`uniqueidentifier` |The payment reason, as defined in Payment Reasons.|
|[Is_Single_Execution](#is_single_execution)|`bit` Readonly|Specifies whether the document is a single execution of its order document.|
|[Is_Released](#is_released)|`bit` Readonly|True if the document is not void and its state is released or greater|
|[Row_Version](#row_version)|`timestamp` ||
|[Payment_Type_Id](#payment_type_id)|`uniqueidentifier` |Specifies the payment type used to pay, when using this payment account. NULL when the payment type is unknown or unspecified.|
|[Fiscal_Printer_Pos_Device_Id](#fiscal_printer_pos_device_id)|`uniqueidentifier` |For POS Sales Order payments. Specifies the POS Device from fiscal printer type on which the receipt is printed. Null when the payment transaction is not created for a POS Sale Order.|
|[Parent_Payment_Slip_Amount_Id](#parent_payment_slip_amount_id)|`uniqueidentifier` |The Payment Slip Amount, which the current payment transaction fulfills . NULL when the current document does not execute any Payment Slip Amount.|
|[Pos_Location_Id](#pos_location_id)|`uniqueidentifier` |For POS Sales Order payments. Specifies the POS Location, in which the payment is performed. Null when the payment transaction is not created for a POS Sale Order.|
|[Pos_Operator_Id](#pos_operator_id)|`uniqueidentifier` |For POS Sales Order payments. Specifies the POS Operator, who created the payment order. Null when the payment transaction is not created for a POS Sale Order.|
|[Reversal_Reason](#reversal_reason)|`nvarchar(3)` Allowed: `OPE`, `TBR`, `REF`|The reason for the reversal of the payment.|

## Columns

### Party_Id


Party_Id


The party that is paying or receiving the money


The party that is paying or receiving the money

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Parties](Gen_Parties.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Cash_Payment_Transactions](Cash_Payment_Transactions.md).[Party_Id](Cash_Payment_Transactions.md#party_id)|
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

### Payment_Account_Id


Payment_Account_Id


The account towards which the payment was effected


The account towards which the payment was effected

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Cash_Payment_Accounts](Cash_Payment_Accounts.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Cash_Payment_Transactions](Cash_Payment_Transactions.md).[Payment_Account_Id](Cash_Payment_Transactions.md#payment_account_id)|
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
|Equals|NULL|yes|no|

### Direction


Direction


I for Payment issue, R for payment receipt


I for Payment issue, R for payment receipt

| Property | Value |
| - | - |
|Type|nvarchar(1)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Allowed Values|`I`, `R`|
|Default Value|R|
|Derived From|[Cash_Payment_Transactions](Cash_Payment_Transactions.md).[Direction](Cash_Payment_Transactions.md#direction)|
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
|Max Length|1|
|Order|3|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Total_Amount


Total_Amount


The total amount payed. The distribution of the amount among source orders is specified with payment transacion lines


The total amount payed. The distribution of the amount among source orders is specified with payment transacion lines

| Property | Value |
| - | - |
|Type|decimal(18, 2)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|0|
|Derived From|[Cash_Payment_Transactions](Cash_Payment_Transactions.md).[Total_Amount](Cash_Payment_Transactions.md#total_amount)|
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
|Order|4|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Total_Amount_Currency_Id


Total_Amount_Currency_Id


The currency of the total amount


The currency of the total amount

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Currencies](Gen_Currencies.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Cash_Payment_Transactions](Cash_Payment_Transactions.md).[Total_Amount_Currency_Id](Cash_Payment_Transactions.md#total_amount_currency_id)|
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
|Order|5|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|yes|

### Requires_Allocation


Requires_Allocation


1=The total amount should be allocated to payment orders; 0=Payment orders are not required


1=The total amount should be allocated to payment orders; 0=Payment orders are not required

| Property | Value |
| - | - |
|Type|bit|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|True|
|Derived From|[Cash_Payment_Transactions](Cash_Payment_Transactions.md).[Requires_Allocation](Cash_Payment_Transactions.md#requires_allocation)|
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
|Order|6|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Payment_Slip_No


Payment_Slip_No


The number of the payment slip. Can be used to directly indicate the number without referring to Payment_Slips


The number of the payment slip. Can be used to directly indicate the number without referring to Payment_Slips

| Property | Value |
| - | - |
|Type|nvarchar(20)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Cash_Payment_Transactions](Cash_Payment_Transactions.md).[Payment_Slip_No](Cash_Payment_Transactions.md#payment_slip_no)|
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
|Max Length|20|
|Order|7|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Payment_Slip_Id


Payment_Slip_Id


When not NULL specifies that this payment was part of a payment slip


When not NULL specifies that this payment was part of a payment slip

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Cash_Payment_Slips](Cash_Payment_Slips.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Cash_Payment_Transactions](Cash_Payment_Transactions.md).[Payment_Slip_Id](Cash_Payment_Transactions.md#payment_slip_id)|
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
|Visible|no|
|Max Length|-1|
|Order|8|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

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
|Attributes|None, IsLongString|
|Default Value|None|
|Derived From|[Cash_Payment_Transactions](Cash_Payment_Transactions.md).[Notes](Cash_Payment_Transactions.md#notes)|
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
|Order|9|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Short|
|Supports EQUALS_IN|no|

### Payment_Transaction_Id


Payment_Transaction_Id

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
|Derived From|[Cash_Payment_Transactions](Cash_Payment_Transactions.md).[Payment_Transaction_Id](Cash_Payment_Transactions.md#payment_transaction_id)|
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
|Order|10|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Document_Id


Document_Id


The document data of the payment transaction


The document data of the payment transaction

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|yes|
|Referenced Table|[Gen_Documents](Gen_Documents.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Cash_Payment_Transactions](Cash_Payment_Transactions.md).[Document_Id](Cash_Payment_Transactions.md#document_id)|
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
|Order|11|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Original_Payment_Transaction_Id


Original_Payment_Transaction_Id


Original Payment Transaction


Original Payment Transaction

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Cash_Payment_Transactions](Cash_Payment_Transactions.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Cash_Payment_Transactions](Cash_Payment_Transactions.md).[Original_Payment_Transaction_Id](Cash_Payment_Transactions.md#original_payment_transaction_id)|
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
|Equals|NULL|yes|no|

### Payment_Reason_Id


Payment_Reason_Id


The payment reason, as defined in Payment Reasons.


The payment reason, as defined in Payment Reasons.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Cash_Payment_Reasons](Cash_Payment_Reasons.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Cash_Payment_Transactions](Cash_Payment_Transactions.md).[Payment_Reason_Id](Cash_Payment_Transactions.md#payment_reason_id)|
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
|Equals|NULL|yes|no|

### Is_Single_Execution


Is_Single_Execution


Specifies whether the document is a single execution of its order document.


Specifies whether the document is a single execution of its order document.

| Property | Value |
| - | - |
|Type|bit|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|yes|
|Sortable|no|
|Attributes|None|
|Default Value|False|
|Derived From|[Cash_Payment_Transactions](Cash_Payment_Transactions.md).[Is_Single_Execution](Cash_Payment_Transactions.md#is_single_execution)|
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

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|yes|

### Is_Released


Is_Released


True if the document is not void and its state is released or greater


True if the document is not void and its state is released or greater

| Property | Value |
| - | - |
|Type|bit|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|yes|
|Sortable|no|
|Attributes|None|
|Default Value|False|
|Derived From|[Cash_Payment_Transactions](Cash_Payment_Transactions.md).[Is_Released](Cash_Payment_Transactions.md#is_released)|
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

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|yes|

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
|Derived From|[Cash_Payment_Transactions](Cash_Payment_Transactions.md).[Row_Version](Cash_Payment_Transactions.md#row_version)|
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

### Payment_Type_Id


Payment_Type_Id


Specifies the payment type used to pay, when using this payment account. NULL when the payment type is unknown or unspecified.


Specifies the payment type used to pay, when using this payment account. NULL when the payment type is unknown or unspecified.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Cash_Payment_Types](Cash_Payment_Types.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Cash_Payment_Transactions](Cash_Payment_Transactions.md).[Payment_Type_Id](Cash_Payment_Transactions.md#payment_type_id)|
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
|Equals|NULL|yes|no|

### Fiscal_Printer_Pos_Device_Id


Fiscal_Printer_Pos_Device_Id


For POS Sales Order payments. Specifies the POS Device from fiscal printer type on which the receipt is printed. Null when the payment transaction is not created for a POS Sale Order.


For POS Sales Order payments. Specifies the POS Device from fiscal printer type on which the receipt is printed. Null when the payment transaction is not created for a POS Sale Order.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Pos_Devices](Pos_Devices.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Cash_Payment_Transactions](Cash_Payment_Transactions.md).[Fiscal_Printer_Pos_Device_Id](Cash_Payment_Transactions.md#fiscal_printer_pos_device_id)|
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
|Equals|NULL|yes|no|

### Parent_Payment_Slip_Amount_Id


Parent_Payment_Slip_Amount_Id


The Payment Slip Amount, which the current payment transaction fulfills . NULL when the current document does not execute any Payment Slip Amount.


The Payment Slip Amount, which the current payment transaction fulfills . NULL when the current document does not execute any Payment Slip Amount.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Cash_Payment_Slip_Amounts](Cash_Payment_Slip_Amounts.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Cash_Payment_Transactions](Cash_Payment_Transactions.md).[Parent_Payment_Slip_Amount_Id](Cash_Payment_Transactions.md#parent_payment_slip_amount_id)|
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
|Equals|NULL|yes|no|

### Pos_Location_Id


Pos_Location_Id


For POS Sales Order payments. Specifies the POS Location, in which the payment is performed. Null when the payment transaction is not created for a POS Sale Order.


For POS Sales Order payments. Specifies the POS Location, in which the payment is performed. Null when the payment transaction is not created for a POS Sale Order.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Pos_Locations](Pos_Locations.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Cash_Payment_Transactions](Cash_Payment_Transactions.md).[Pos_Location_Id](Cash_Payment_Transactions.md#pos_location_id)|
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
|Equals|NULL|yes|no|

### Pos_Operator_Id


Pos_Operator_Id


For POS Sales Order payments. Specifies the POS Operator, who created the payment order. Null when the payment transaction is not created for a POS Sale Order.


For POS Sales Order payments. Specifies the POS Operator, who created the payment order. Null when the payment transaction is not created for a POS Sale Order.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Pos_Operators](Pos_Operators.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Cash_Payment_Transactions](Cash_Payment_Transactions.md).[Pos_Operator_Id](Cash_Payment_Transactions.md#pos_operator_id)|
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
|Equals|NULL|yes|no|

### Reversal_Reason


Reversal_Reason


The reason for the reversal of the payment.


The reason for the reversal of the payment.

| Property | Value |
| - | - |
|Type|nvarchar(3)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Allowed Values|`OPE`, `TBR`, `REF`|
|Default Value|None|
|Derived From|[Cash_Payment_Transactions](Cash_Payment_Transactions.md).[Reversal_Reason](Cash_Payment_Transactions.md#reversal_reason)|
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
|Max Length|3|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|


