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

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Party_Name

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Payment_Date

| Property | Value |
| - | - |
|Type|datetime|

### Total_Amount

| Property | Value |
| - | - |
|Type|decimal(18, 2)|

### Direction

| Property | Value |
| - | - |
|Type|nvarchar(1)|

### Is_Party_Payment

| Property | Value |
| - | - |
|Type|bit|

### Description

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Payment_Slip_Amount_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Payment_Slip_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Payment_Reason_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Line_No

| Property | Value |
| - | - |
|Type|int|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


