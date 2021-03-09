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

| Property | Value |
| - | - |
|Type|int|

### Filter_XML

| Property | Value |
| - | - |
|Type|nvarchar(1073741823)|

### Debit_Account_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Credit_Account_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Amount_Source_Name

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### Amount_Row_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Amount_Row_Name

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Amount_Source_Filter

| Property | Value |
| - | - |
|Type|nvarchar(1073741823)|

### Amount_Column_Name

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### Multiplier

| Property | Value |
| - | - |
|Type|decimal(18, 6)|

### Valid_From_Date

| Property | Value |
| - | - |
|Type|datetime|

### Amount_Condition

| Property | Value |
| - | - |
|Type|nvarchar(1)|

### Template_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Valid_To_Date

| Property | Value |
| - | - |
|Type|datetime|

### Template_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


