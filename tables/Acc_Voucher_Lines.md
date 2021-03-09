# Table Acc_Voucher_Lines

Contains one debit or credit posting within an accounting voucher. Entity: Acc_Voucher_Lines

## Owner Tables Hierarchy

* [Acc_Vouchers](Acc_Vouchers.md)
* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Line_No](#line_no)|`int` |Consecutive number of the line within the voucher|
|[Account_Id](#account_id)|`uniqueidentifier` |The account being debited or credited|
|[Item_Key](#item_key)|`nvarchar(64)` |The item (grouping) key for the account in the line. Account_Id + Item_Key - the smallest unit of calculation for account balance.|
|[Currency_Id](#currency_id)|`uniqueidentifier` |The currency of the movement in this line. If there is defined currency for the account in the line that it should be equal to the value in this field.|
|[Debit](#debit)|`decimal(18, 2)` |The amount of the debit in the currency of the account. 0 means that the account is not debited|
|[Debit_Base](#debit_base)|`decimal(18, 2)` |The amount of debit in base currency|
|[Credit](#credit)|`decimal(18, 2)` |The amount of the credit in the currency of the account. 0 means that the account is not credited|
|[Credit_Base](#credit_base)|`decimal(18, 2)` |The amount of credit in base currency|
|[Referenced_Document_Id](#referenced_document_id)|`uniqueidentifier` |The document which is referenced by the line. By default, this is the document of the voucher|
|[Rate_Multiplier](#rate_multiplier)|`decimal(18, 6)` |The multiplier for conversion from Debit/Credit to base currency|
|[Rate_Divisor](#rate_divisor)|`decimal(18, 6)` |The divisor for conversion from Debit/Credit to base currency|
|[Cost_Center_Id](#cost_center_id)|`uniqueidentifier` |The cost center to which this cost is related|
|[Profit_Center_Id](#profit_center_id)|`uniqueidentifier` |The profit center to which this revenue is related|
|[Correspondance_No](#correspondance_no)|`int` |The number of the correspondance group within the accounting voucher. For each correspondance group, the debits are equal to the credits|
|[Correspondant_Amount](#correspondant_amount)|`decimal(18, 2)` Readonly|The amount (in the currency of the correspondant line) to which the amount in this line is corresponding. This field has value only when the current line is corresponding to only one line (e.g. NULL means that the current line is corresponding to many lines).|
|[Voucher_Line_Id](#voucher_line_id)|`uniqueidentifier` `PK`||
|[Voucher_Id](#voucher_id)|`uniqueidentifier` |The voucher to which this line is attached|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Line_No

| Property | Value |
| - | - |
|Type|int|

### Account_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Item_Key

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Debit

| Property | Value |
| - | - |
|Type|decimal(18, 2)|

### Debit_Base

| Property | Value |
| - | - |
|Type|decimal(18, 2)|

### Credit

| Property | Value |
| - | - |
|Type|decimal(18, 2)|

### Credit_Base

| Property | Value |
| - | - |
|Type|decimal(18, 2)|

### Referenced_Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Rate_Multiplier

| Property | Value |
| - | - |
|Type|decimal(18, 6)|

### Rate_Divisor

| Property | Value |
| - | - |
|Type|decimal(18, 6)|

### Cost_Center_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Profit_Center_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Correspondance_No

| Property | Value |
| - | - |
|Type|int|

### Correspondant_Amount

| Property | Value |
| - | - |
|Type|decimal(18, 2)|

### Voucher_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Voucher_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


