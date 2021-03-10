# Procedure Acc_Vouchers_Table_Load_Environment_Lines


## Summary

| Name | Type | Description |
| - | - | --- |
|[Voucher_Line_Id](#voucher_line_id)|`uniqueidentifier` `PK`||
|[Voucher_Id](#voucher_id)|`uniqueidentifier` |The voucher to which this line is attached|
|[Line_No](#line_no)|`int` |Consecutive number of the line within the voucher|
|[Account_Id](#account_id)|`uniqueidentifier` |The account being debited or credited|
|[Item_Key](#item_key)|`nvarchar` |The item (grouping) key for the account in the line. Account_Id + Item_Key - the smallest unit of calculation for account balance.|
|[Currency_Id](#currency_id)|`uniqueidentifier` |The currency of the movement in this line. If there is defined currency for the account in the line that it should be equal to the value in this field.|
|[Referenced_Document_Id](#referenced_document_id)|`uniqueidentifier` |The document which is referenced by the line. By default, this is the document of the voucher|
|[Debit](#debit)|`decimal(18, 2)` |The amount of the debit in the currency of the account. 0 means that the account is not debited|
|[Credit](#credit)|`decimal(18, 2)` |The amount of the credit in the currency of the account. 0 means that the account is not credited|
|[Rate_Multiplier](#rate_multiplier)|`decimal(18, 6)` |The multiplier for conversion from Debit/Credit to base currency|
|[Rate_Divisor](#rate_divisor)|`decimal(18, 6)` |The divisor for conversion from Debit/Credit to base currency|
|[Debit_Base](#debit_base)|`decimal(18, 2)` |The amount of debit in base currency|
|[Credit_Base](#credit_base)|`decimal(18, 2)` |The amount of credit in base currency|
|[Cost_Center_Id](#cost_center_id)|`uniqueidentifier` |The cost center to which this cost is related|
|[Profit_Center_Id](#profit_center_id)|`uniqueidentifier` |The profit center to which this revenue is related|
|[Correspondance_No](#correspondance_no)|`int` |The number of the correspondance group within the accounting voucher. For each correspondance group, the debits are equal to the credits|
|[Correspondant_Amount](#correspondant_amount)|`decimal(18, 2)` Readonly|The amount (in the currency of the correspondant line) to which the amount in this line is corresponding. This field has value only when the current line is corresponding to only one line (e.g. NULL means that the current line is corresponding to many lines).|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Voucher_Line_Id


Voucher_Line_Id

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
|Derived From|[Acc_Voucher_Lines](Acc_Voucher_Lines.md).[Voucher_Line_Id](Acc_Voucher_Lines.md#voucher_line_id)|
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

### Voucher_Id


Voucher_Id


The voucher to which this line is attached


The voucher to which this line is attached

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Acc_Vouchers](Acc_Vouchers.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Acc_Voucher_Lines](Acc_Voucher_Lines.md).[Voucher_Id](Acc_Voucher_Lines.md#voucher_id)|
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

### Line_No


Line_No


Consecutive number of the line within the voucher


Consecutive number of the line within the voucher

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
|Autoincrement|10|
|Derived From|[Acc_Voucher_Lines](Acc_Voucher_Lines.md).[Line_No](Acc_Voucher_Lines.md#line_no)|
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
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|25|
|Supports EQUALS_IN|no|

### Account_Id


Account_Id


The account being debited or credited


The account being debited or credited

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Acc_Accounts](Acc_Accounts.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Acc_Voucher_Lines](Acc_Voucher_Lines.md).[Account_Id](Acc_Voucher_Lines.md#account_id)|
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
|UI Width|Long|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Item_Key


Item_Key


The item (grouping) key for the account in the line. Account_Id + Item_Key - the smallest unit of calculation for account balance.


The item (grouping) key for the account in the line. Account_Id + Item_Key - the smallest unit of calculation for account balance.

| Property | Value |
| - | - |
|Type|nvarchar|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Acc_Voucher_Lines](Acc_Voucher_Lines.md).[Item_Key](Acc_Voucher_Lines.md#item_key)|
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
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|yes|
|Like|None|no|no|

### Currency_Id


Currency_Id


The currency of the movement in this line. If there is defined currency for the account in the line that it should be equal to the value in this field.


The currency of the movement in this line. If there is defined currency for the account in the line that it should be equal to the value in this field.

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
|Derived From|[Acc_Voucher_Lines](Acc_Voucher_Lines.md).[Currency_Id](Acc_Voucher_Lines.md#currency_id)|
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
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|50|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|yes|

### Referenced_Document_Id


Referenced_Document_Id


The document which is referenced by the line. By default, this is the document of the voucher


The document which is referenced by the line. By default, this is the document of the voucher

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
|Derived From|[Acc_Voucher_Lines](Acc_Voucher_Lines.md).[Referenced_Document_Id](Acc_Voucher_Lines.md#referenced_document_id)|
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
|UI Width|Long|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Debit


Debit


The amount of the debit in the currency of the account. 0 means that the account is not debited


The amount of the debit in the currency of the account. 0 means that the account is not debited

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
|Derived From|[Acc_Voucher_Lines](Acc_Voucher_Lines.md).[Debit](Acc_Voucher_Lines.md#debit)|
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
|Summary Type|Sum|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Credit


Credit


The amount of the credit in the currency of the account. 0 means that the account is not credited


The amount of the credit in the currency of the account. 0 means that the account is not credited

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
|Derived From|[Acc_Voucher_Lines](Acc_Voucher_Lines.md).[Credit](Acc_Voucher_Lines.md#credit)|
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
|Summary Type|Sum|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Rate_Multiplier


Rate_Multiplier


The multiplier for conversion from Debit/Credit to base currency


The multiplier for conversion from Debit/Credit to base currency

| Property | Value |
| - | - |
|Type|decimal(18, 6)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|1|
|Derived From|[Acc_Voucher_Lines](Acc_Voucher_Lines.md).[Rate_Multiplier](Acc_Voucher_Lines.md#rate_multiplier)|
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
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Rate_Divisor


Rate_Divisor


The divisor for conversion from Debit/Credit to base currency


The divisor for conversion from Debit/Credit to base currency

| Property | Value |
| - | - |
|Type|decimal(18, 6)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|1|
|Derived From|[Acc_Voucher_Lines](Acc_Voucher_Lines.md).[Rate_Divisor](Acc_Voucher_Lines.md#rate_divisor)|
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
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Debit_Base


Debit_Base


The amount of debit in base currency


The amount of debit in base currency

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
|Derived From|[Acc_Voucher_Lines](Acc_Voucher_Lines.md).[Debit_Base](Acc_Voucher_Lines.md#debit_base)|
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
|Order|2147483647|
|Summary Type|Sum|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Credit_Base


Credit_Base


The amount of credit in base currency


The amount of credit in base currency

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
|Derived From|[Acc_Voucher_Lines](Acc_Voucher_Lines.md).[Credit_Base](Acc_Voucher_Lines.md#credit_base)|
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
|Order|2147483647|
|Summary Type|Sum|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Cost_Center_Id


Cost_Center_Id


The cost center to which this cost is related


The cost center to which this cost is related

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Acc_Cost_Centers](Acc_Cost_Centers.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Acc_Voucher_Lines](Acc_Voucher_Lines.md).[Cost_Center_Id](Acc_Voucher_Lines.md#cost_center_id)|
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
|UI Width|Long|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Profit_Center_Id


Profit_Center_Id


The profit center to which this revenue is related


The profit center to which this revenue is related

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Acc_Profit_Centers](Acc_Profit_Centers.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Acc_Voucher_Lines](Acc_Voucher_Lines.md).[Profit_Center_Id](Acc_Voucher_Lines.md#profit_center_id)|
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
|UI Width|Long|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Correspondance_No


Correspondance_No


The number of the correspondance group within the accounting voucher. For each correspondance group, the debits are equal to the credits


The number of the correspondance group within the accounting voucher. For each correspondance group, the debits are equal to the credits

| Property | Value |
| - | - |
|Type|int|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|0|
|Derived From|[Acc_Voucher_Lines](Acc_Voucher_Lines.md).[Correspondance_No](Acc_Voucher_Lines.md#correspondance_no)|
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
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Correspondant_Amount


Correspondant_Amount


The amount (in the currency of the correspondant line) to which the amount in this line is corresponding. This field has value only when the current line is corresponding to only one line (e.g. NULL means that the current line is corresponding to many lines).


The amount (in the currency of the correspondant line) to which the amount in this line is corresponding. This field has value only when the current line is corresponding to only one line (e.g. NULL means that the current line is corresponding to many lines).

| Property | Value |
| - | - |
|Type|decimal(18, 2)|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|yes|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Acc_Voucher_Lines](Acc_Voucher_Lines.md).[Correspondant_Amount](Acc_Voucher_Lines.md#correspondant_amount)|
|Format|N2|
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


