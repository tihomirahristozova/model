# Procedure Cash_Payment_Transactions_Table_Printout


## Summary

| Name | Type | Description |
| - | - | --- |
|[Payment_Transaction_Id](#payment_transaction_id)|`uniqueidentifier` `PK`||
|[Document_Id](#document_id)|`uniqueidentifier` |The document data of the payment transaction|
|[Notes](#notes)|`nvarchar` ||
|[Party_Id](#party_id)|`uniqueidentifier` |The party that is paying or receiving the money|
|[Party_Name](#party_name)|`nvarchar` `ML`|The name of the party|
|[Payment_Account_Id](#payment_account_id)|`uniqueidentifier` |The account towards which the payment was effected|
|[Payment_Account_Name](#payment_account_name)|`nvarchar` ||
|[Total_Amount](#total_amount)|`decimal(18, 2)` |The total amount payed. The distribution of the amount among source orders is specified with payment transacion lines|
|[Total_Amount_Currency_Id](#total_amount_currency_id)|`uniqueidentifier` |The currency of the total amount|
|[Total_Amount_Words](#total_amount_words)|`nvarchar` ||
|[Total_Amount_Currency_Name](#total_amount_currency_name)|`nvarchar` ||
|[Total_Amount_Currency_Sign](#total_amount_currency_sign)|`nvarchar` ||
|[Payment_Slip_Id](#payment_slip_id)|`uniqueidentifier` |When not NULL specifies that this payment was part of a payment slip|
|[Payment_Slip_No](#payment_slip_no)|`nvarchar` |The number of the payment slip. Can be used to directly indicate the number without referring to Payment_Slips|
|[Requires_Allocation](#requires_allocation)|`bit` |1=The total amount should be allocated to payment orders; 0=Payment orders are not required|
|[Direction](#direction)|`nvarchar` Allowed: `I`, `R`|I for Payment issue, R for payment receipt|

## Columns

### Payment_Transaction_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar|

### Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Party_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Payment_Account_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Payment_Account_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Total_Amount

| Property | Value |
| - | - |
|Type|decimal(18, 2)|

### Total_Amount_Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Total_Amount_Words

| Property | Value |
| - | - |
|Type|nvarchar|

### Total_Amount_Currency_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Total_Amount_Currency_Sign

| Property | Value |
| - | - |
|Type|nvarchar|

### Payment_Slip_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Payment_Slip_No

| Property | Value |
| - | - |
|Type|nvarchar|

### Requires_Allocation

| Property | Value |
| - | - |
|Type|bit|

### Direction

| Property | Value |
| - | - |
|Type|nvarchar|


