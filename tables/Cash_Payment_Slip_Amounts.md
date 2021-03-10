# Table Cash_Payment_Slip_Amounts

Mass payment amount. Each record generates one payment transaction. Entity: Cash_Payment_Slip_Amounts

## Owner Tables Hierarchy

* [Cash_Payment_Slips](Cash_Payment_Slips.md)
* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Party_Id](#party_id)|`uniqueidentifier` |The party that is paying or receiving the money. The column can be left blank if there is no party involved (e.g. the amount is fee) or the party isn't present in the database yet.|
|[Party_Name](#party_name)|`nvarchar(254)` `ML`|The name of the party that is paying or receiving the money. The column can be left blank if there is no party involved (e.g. the amount is fee).|
|[Payment_Date](#payment_date)|`datetime` |The date on which the payment is done|
|[Total_Amount](#total_amount)|`decimal(18, 2)` |The total amount payed. The distribution of the amount amongst the payment orders for this party is specified with payment slip lines. If NULL the total amount is calculated as sum of the amounts in the payment slip lines.|
|[Direction](#direction)|`nvarchar(1)` Allowed: `I`, `R`|'I' for Payment issue, 'R' for payment receipt|
|[Is_Party_Payment](#is_party_payment)|`bit` |Indicates whether the amount is payed or received by party or not (i.e. the amount is for fee, tax, etc.)|
|[Description](#description)|`nvarchar(254)` |Description of the payed amount. The numbers of the documents which are payed for example.|
|[Payment_Slip_Amount_Id](#payment_slip_amount_id)|`uniqueidentifier` `PK`||
|[Payment_Slip_Id](#payment_slip_id)|`uniqueidentifier` ||
|[Payment_Reason_Id](#payment_reason_id)|`uniqueidentifier` |The reason for the payment, as defined in Payment Reasons.|
|[Line_No](#line_no)|`int` |The number of the line within the payment|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Party_Id


Party_Id


The party that is paying or receiving the money. The column can be left blank if there is no party involved (e.g. the amount is fee) or the party isn't present in the database yet.


The party that is paying or receiving the money. The column can be left blank if there is no party involved (e.g. the amount is fee) or the party isn't present in the database yet.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Parties](Gen_Parties.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Cash_Payment_Slip_Amounts](Cash_Payment_Slip_Amounts.md).[Party_Id](Cash_Payment_Slip_Amounts.md#party_id)|
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
|UI Width|Long|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Party_Name


Party_Name


The name of the party that is paying or receiving the money. The column can be left blank if there is no party involved (e.g. the amount is fee).


The name of the party that is paying or receiving the money. The column can be left blank if there is no party involved (e.g. the amount is fee).

| Property | Value |
| - | - |
|Type|nvarchar(254)|
|Is Mulitlanguage|yes|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Cash_Payment_Slip_Amounts](Cash_Payment_Slip_Amounts.md).[Party_Name](Cash_Payment_Slip_Amounts.md#party_name)|
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
|Max Length|254|
|Order|2|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Long|
|Supports EQUALS_IN|no|

### Payment_Date


Payment_Date


The date on which the payment is done


The date on which the payment is done

| Property | Value |
| - | - |
|Type|datetime|
|DateTime Format|DateTime|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Cash_Payment_Slip_Amounts](Cash_Payment_Slip_Amounts.md).[Payment_Date](Cash_Payment_Slip_Amounts.md#payment_date)|
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
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|GreaterThanOrLessThan|None|no|no|

### Total_Amount


Total_Amount


The total amount payed. The distribution of the amount amongst the payment orders for this party is specified with payment slip lines. If NULL the total amount is calculated as sum of the amounts in the payment slip lines.


The total amount payed. The distribution of the amount amongst the payment orders for this party is specified with payment slip lines. If NULL the total amount is calculated as sum of the amounts in the payment slip lines.

| Property | Value |
| - | - |
|Type|decimal(18, 2)|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Cash_Payment_Slip_Amounts](Cash_Payment_Slip_Amounts.md).[Total_Amount](Cash_Payment_Slip_Amounts.md#total_amount)|
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

### Direction


Direction


'I' for Payment issue, 'R' for payment receipt


'I' for Payment issue, 'R' for payment receipt

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
|Default Value|None|
|Derived From|[Cash_Payment_Slip_Amounts](Cash_Payment_Slip_Amounts.md).[Direction](Cash_Payment_Slip_Amounts.md#direction)|
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
|Order|5|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Short|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Is_Party_Payment


Is_Party_Payment


Indicates whether the amount is payed or received by party or not (i.e. the amount is for fee, tax, etc.)


Indicates whether the amount is payed or received by party or not (i.e. the amount is for fee, tax, etc.)

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
|Derived From|[Cash_Payment_Slip_Amounts](Cash_Payment_Slip_Amounts.md).[Is_Party_Payment](Cash_Payment_Slip_Amounts.md#is_party_payment)|
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
|Order|6|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Description


Description


Description of the payed amount. The numbers of the documents which are payed for example.


Description of the payed amount. The numbers of the documents which are payed for example.

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
|Derived From|[Cash_Payment_Slip_Amounts](Cash_Payment_Slip_Amounts.md).[Description](Cash_Payment_Slip_Amounts.md#description)|
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
|Order|7|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Long|
|Supports EQUALS_IN|no|

### Payment_Slip_Amount_Id


Payment_Slip_Amount_Id

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
|Derived From|[Cash_Payment_Slip_Amounts](Cash_Payment_Slip_Amounts.md).[Payment_Slip_Amount_Id](Cash_Payment_Slip_Amounts.md#payment_slip_amount_id)|
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

### Payment_Slip_Id


Payment_Slip_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|yes|
|Referenced Table|[Cash_Payment_Slips](Cash_Payment_Slips.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Cash_Payment_Slip_Amounts](Cash_Payment_Slip_Amounts.md).[Payment_Slip_Id](Cash_Payment_Slip_Amounts.md#payment_slip_id)|
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

### Payment_Reason_Id


Payment_Reason_Id


The reason for the payment, as defined in Payment Reasons.


The reason for the payment, as defined in Payment Reasons.

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
|Derived From|[Cash_Payment_Slip_Amounts](Cash_Payment_Slip_Amounts.md).[Payment_Reason_Id](Cash_Payment_Slip_Amounts.md#payment_reason_id)|
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

### Line_No


Line_No


The number of the line within the payment


The number of the line within the payment

| Property | Value |
| - | - |
|Type|int|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Autoincrement|1|
|Derived From|[Cash_Payment_Slip_Amounts](Cash_Payment_Slip_Amounts.md).[Line_No](Cash_Payment_Slip_Amounts.md#line_no)|
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
|UI Width|Short|
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
|Derived From|[Cash_Payment_Slip_Amounts](Cash_Payment_Slip_Amounts.md).[Row_Version](Cash_Payment_Slip_Amounts.md#row_version)|
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


