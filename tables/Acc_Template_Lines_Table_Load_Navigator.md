# Query Acc_Template_Lines_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Template_Id](#template_id)|`uniqueidentifier` `PK`||
|[Template_Name](#template_name)|`nvarchar` ||
|[Route_Id](#route_id)|`uniqueidentifier` ||
|[Voucher_Date_Source](#voucher_date_source)|`nvarchar` ||
|[Voucher_Description_Mask](#voucher_description_mask)|`nvarchar` ||
|[Line_No](#line_no)|`int` ||
|[Filter_XML](#filter_xml)|`nvarchar` ||
|[Debit_Account_Id](#debit_account_id)|`uniqueidentifier` ||
|[Credit_Account_Id](#credit_account_id)|`uniqueidentifier` ||
|[Amount_Source_Name](#amount_source_name)|`nvarchar` ||
|[Amount_Row_Id](#amount_row_id)|`uniqueidentifier` ||
|[Amount_Row_Name](#amount_row_name)|`nvarchar` ||
|[Amount_Source_Filter](#amount_source_filter)|`nvarchar` ||
|[Amount_Column_Name](#amount_column_name)|`nvarchar` ||
|[Multiplier](#multiplier)|`decimal(0, 0)` ||
|[Notes](#notes)|`nvarchar` ||
|[Amount_Condition](#amount_condition)|`nvarchar` Allowed: `+`, `-`|Condition for the amount. The line is accounted only when the condition is matched. The condition can be one of: NULL - no condition, the line should be accounted unconditionally; '+' - The amount should be positive; '-' - The amount should be negative. The amount is matched as returned from the source, before applying the Multiplier.|
|[Valid_From_Date](#valid_from_date)|`datetime` |Start date from which the accounting template line is valid|
|[Valid_To_Date](#valid_to_date)|`datetime` |End date to which the accounting template line is valid|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Template_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Template_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Route_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Voucher_Date_Source

| Property | Value |
| - | - |
|Type|nvarchar|

### Voucher_Description_Mask

| Property | Value |
| - | - |
|Type|nvarchar|

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


