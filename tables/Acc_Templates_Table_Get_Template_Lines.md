# Procedure Acc_Templates_Table_Get_Template_Lines


## Summary

| Name | Type | Description |
| - | - | --- |
|[Template_Line_Id](#template_line_id)|`uniqueidentifier` `PK`||
|[Template_Id](#template_id)|`uniqueidentifier` ||
|[Line_No](#line_no)|`int` |Consecutive number of the line within the template. Determines the order of execution of the template lines.|
|[Filter_XML](#filter_xml)|`nvarchar` |The line is accounted only when the filter is satisfied compared with the source document header|
|[Debit_Account_Id](#debit_account_id)|`uniqueidentifier` |The account which should be debited|
|[Credit_Account_Id](#credit_account_id)|`uniqueidentifier` |The account which should be credited|
|[Amount_Source_Name](#amount_source_name)|`nvarchar` |The source rowset for the amount. For example: DocLines, DocHeader, Additional Amounts, Stock Types, etc.|
|[Amount_Row_Id](#amount_row_id)|`uniqueidentifier` |The id of the row from the amount rowset where the amount is located. NULL means to account one by one for all rows within the rowset|
|[Amount_Row_Name](#amount_row_name)|`nvarchar` |The name of definition, specified in Amount_Row_Id. NULL means that no Amount_Row_Id is specified or there is no name|
|[Amount_Source_Filter](#amount_source_filter)|`nvarchar` |Filter that further specifies which rows from the amount rowset determine the amount|
|[Amount_Column_Name](#amount_column_name)|`nvarchar` |The name of the column within the amount rowset where the amount is located|
|[Multiplier](#multiplier)|`decimal(0, 0)` ||
|[Notes](#notes)|`nvarchar` ||
|[Amount_Condition](#amount_condition)|`nvarchar` ||
|[Valid_From_Date](#valid_from_date)|`datetime` ||
|[Valid_To_Date](#valid_to_date)|`datetime` ||
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Template_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Template_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Line_No

| Property | Value |
| - | - |
|Type|int|

### Filter_XML

| Property | Value |
| - | - |
|Type|nvarchar|

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
|Type|nvarchar|

### Amount_Row_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Amount_Row_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Amount_Source_Filter

| Property | Value |
| - | - |
|Type|nvarchar|

### Amount_Column_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Multiplier

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar|

### Amount_Condition

| Property | Value |
| - | - |
|Type|nvarchar|

### Valid_From_Date

| Property | Value |
| - | - |
|Type|datetime|

### Valid_To_Date

| Property | Value |
| - | - |
|Type|datetime|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


