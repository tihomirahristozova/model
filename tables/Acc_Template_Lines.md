# Table Acc_Template_Lines

Each template line contains the posting to a single set of debit and credit account. It also specifies the way to calculate the amount. Entity: Acc_Template_Lines

## Owner Tables Hierarchy

* [Acc_Templates](Acc_Templates.md)
* [Wf_Routes](Wf_Routes.md)
* [Gen_Document_Types](Gen_Document_Types.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Line_No](#line_no)|`int` |Consecutive number of the line within the template. Determines the order of execution of the template lines.|
|[Filter_XML](#filter_xml)|`nvarchar(1073741823)` |The line is accounted only when the filter is satisfied compared with the source document header|
|[Debit_Account_Id](#debit_account_id)|`uniqueidentifier` |The account which should be debited|
|[Credit_Account_Id](#credit_account_id)|`uniqueidentifier` |The account which should be credited|
|[Amount_Source_Name](#amount_source_name)|`nvarchar(64)` |The source rowset for the amount. For example: DocLines, DocHeader, Additional Amounts, Stock Types, etc.|
|[Amount_Row_Id](#amount_row_id)|`uniqueidentifier` |The id of the row from the amount rowset where the amount is located. NULL means to account one by one for all rows within the rowset|
|[Amount_Row_Name](#amount_row_name)|`nvarchar(254)` |The name of definition, specified in Amount_Row_Id. NULL means that no Amount_Row_Id is specified or there is no name|
|[Amount_Source_Filter](#amount_source_filter)|`nvarchar(1073741823)` |Filter that further specifies which rows from the amount rowset determine the amount|
|[Amount_Column_Name](#amount_column_name)|`nvarchar(64)` |The name of the column within the amount rowset where the amount is located|
|[Multiplier](#multiplier)|`decimal(18, 6)` |Factor by which the amount from the source will be multiplied|
|[Valid_From_Date](#valid_from_date)|`datetime` |Start date from which the accounting template line is valid|
|[Amount_Condition](#amount_condition)|`nvarchar(1)` Allowed: `+`, `-`|Condition for the amount. The line is accounted only when the condition is matched. The condition can be one of: NULL - no condition, the line should be accounted unconditionally; '+' - The amount should be positive; '-' - The amount should be negative. The amount is matched as returned from the source, before applying the Multiplier.|
|[Template_Line_Id](#template_line_id)|`uniqueidentifier` `PK`||
|[Valid_To_Date](#valid_to_date)|`datetime` |End date to which the accounting template line is valid|
|[Template_Id](#template_id)|`uniqueidentifier` ||
|[Notes](#notes)|`nvarchar(254)` ||
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Line_No


Line_No


Consecutive number of the line within the template. Determines the order of execution of the template lines.


Consecutive number of the line within the template. Determines the order of execution of the template lines.

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
|Derived From|[Acc_Template_Lines](Acc_Template_Lines.md).[Line_No](Acc_Template_Lines.md#line_no)|
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
|UI Width|25|
|Supports EQUALS_IN|no|

### Filter_XML


Filter_XML


The line is accounted only when the filter is satisfied compared with the source document header


The line is accounted only when the filter is satisfied compared with the source document header

| Property | Value |
| - | - |
|Type|nvarchar(1073741823)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Acc_Template_Lines](Acc_Template_Lines.md).[Filter_XML](Acc_Template_Lines.md#filter_xml)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|yes|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|1073741823|
|Order|2|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Short|
|Supports EQUALS_IN|no|

### Debit_Account_Id


Debit_Account_Id


The account which should be debited


The account which should be debited

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
|Derived From|[Acc_Template_Lines](Acc_Template_Lines.md).[Debit_Account_Id](Acc_Template_Lines.md#debit_account_id)|
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

### Credit_Account_Id


Credit_Account_Id


The account which should be credited


The account which should be credited

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
|Derived From|[Acc_Template_Lines](Acc_Template_Lines.md).[Credit_Account_Id](Acc_Template_Lines.md#credit_account_id)|
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
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Amount_Source_Name


Amount_Source_Name


The source rowset for the amount. For example: DocLines, DocHeader, Additional Amounts, Stock Types, etc.


The source rowset for the amount. For example: DocLines, DocHeader, Additional Amounts, Stock Types, etc.

| Property | Value |
| - | - |
|Type|nvarchar(64)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Acc_Template_Lines](Acc_Template_Lines.md).[Amount_Source_Name](Acc_Template_Lines.md#amount_source_name)|
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
|Max Length|64|
|Order|5|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Amount_Row_Id


Amount_Row_Id


The id of the row from the amount rowset where the amount is located. NULL means to account one by one for all rows within the rowset


The id of the row from the amount rowset where the amount is located. NULL means to account one by one for all rows within the rowset

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Acc_Template_Lines](Acc_Template_Lines.md).[Amount_Row_Id](Acc_Template_Lines.md#amount_row_id)|
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
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Amount_Row_Name


Amount_Row_Name


The name of definition, specified in Amount_Row_Id. NULL means that no Amount_Row_Id is specified or there is no name


The name of definition, specified in Amount_Row_Id. NULL means that no Amount_Row_Id is specified or there is no name

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
|Derived From|[Acc_Template_Lines](Acc_Template_Lines.md).[Amount_Row_Name](Acc_Template_Lines.md#amount_row_name)|
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
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Amount_Source_Filter


Amount_Source_Filter


Filter that further specifies which rows from the amount rowset determine the amount


Filter that further specifies which rows from the amount rowset determine the amount

| Property | Value |
| - | - |
|Type|nvarchar(1073741823)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Acc_Template_Lines](Acc_Template_Lines.md).[Amount_Source_Filter](Acc_Template_Lines.md#amount_source_filter)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|yes|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|1073741823|
|Order|8|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Short|
|Supports EQUALS_IN|no|

### Amount_Column_Name


Amount_Column_Name


The name of the column within the amount rowset where the amount is located


The name of the column within the amount rowset where the amount is located

| Property | Value |
| - | - |
|Type|nvarchar(64)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Acc_Template_Lines](Acc_Template_Lines.md).[Amount_Column_Name](Acc_Template_Lines.md#amount_column_name)|
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
|Max Length|64|
|Order|9|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Multiplier


Multiplier


Factor by which the amount from the source will be multiplied


Factor by which the amount from the source will be multiplied

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
|Derived From|[Acc_Template_Lines](Acc_Template_Lines.md).[Multiplier](Acc_Template_Lines.md#multiplier)|
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
|Order|10|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Short|
|Supports EQUALS_IN|no|

### Valid_From_Date


Valid_From_Date


Start date from which the accounting template line is valid


Start date from which the accounting template line is valid

| Property | Value |
| - | - |
|Type|datetime|
|DateTime Format|DateTime|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Acc_Template_Lines](Acc_Template_Lines.md).[Valid_From_Date](Acc_Template_Lines.md#valid_from_date)|
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
|GreaterThanOrLessThan|None|yes|no|

### Amount_Condition


Amount_Condition


Condition for the amount. The line is accounted only when the condition is matched. The condition can be one of: NULL - no condition, the line should be accounted unconditionally; '+' - The amount should be positive; '-' - The amount should be negative. The amount is matched as returned from the source, before applying the Multiplier.


Condition for the amount. The line is accounted only when the condition is matched. The condition can be one of: NULL - no condition, the line should be accounted unconditionally; '+' - The amount should be positive; '-' - The amount should be negative. The amount is matched as returned from the source, before applying the Multiplier.

| Property | Value |
| - | - |
|Type|nvarchar(1)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Allowed Values|`+`, `-`|
|Default Value|None|
|Derived From|[Acc_Template_Lines](Acc_Template_Lines.md).[Amount_Condition](Acc_Template_Lines.md#amount_condition)|
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
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Template_Line_Id


Template_Line_Id

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
|Derived From|[Acc_Template_Lines](Acc_Template_Lines.md).[Template_Line_Id](Acc_Template_Lines.md#template_line_id)|
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

### Valid_To_Date


Valid_To_Date


End date to which the accounting template line is valid


End date to which the accounting template line is valid

| Property | Value |
| - | - |
|Type|datetime|
|DateTime Format|DateTime|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Acc_Template_Lines](Acc_Template_Lines.md).[Valid_To_Date](Acc_Template_Lines.md#valid_to_date)|
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
|GreaterThanOrLessThan|None|yes|no|

### Template_Id


Template_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|yes|
|Referenced Table|[Acc_Templates](Acc_Templates.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Acc_Template_Lines](Acc_Template_Lines.md).[Template_Id](Acc_Template_Lines.md#template_id)|
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
|Derived From|[Acc_Template_Lines](Acc_Template_Lines.md).[Notes](Acc_Template_Lines.md#notes)|
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
|Max Length|254|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
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
|Derived From|[Acc_Template_Lines](Acc_Template_Lines.md).[Row_Version](Acc_Template_Lines.md#row_version)|
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


