# Query Cash_Payment_Orders_Table_Load_Payment_Transaction_Lines


## Summary

| Name | Type | Description |
| - | - | --- |
|[From_Party_Id](#from_party_id)|`uniqueidentifier` ||
|[Document_Date](#document_date)|`date` ||
|[State](#state)|`smallint` Allowed: `0`, `5`, `10`, `20`, `30`, `40`, `50`, Readonly||
|[Party_Id](#party_id)|`uniqueidentifier` ||
|[Payment_Account_Id](#payment_account_id)|`uniqueidentifier` ||
|[Total_Amount](#total_amount)|`decimal(0, 0)` ||
|[Total_Amount_Currency_Id](#total_amount_currency_id)|`uniqueidentifier` ||
|[Amount](#amount)|`decimal(0, 0)` ||
|[Covered_Order_Amount](#covered_order_amount)|`decimal(0, 0)` ||
|[Payment_Order_Id](#payment_order_id)|`uniqueidentifier` ||
|[Document_Type_Id](#document_type_id)|`uniqueidentifier` ||
|[Document_No](#document_no)|`nvarchar` ||
|[To_Party_Id](#to_party_id)|`uniqueidentifier` ||
|[Read_Only](#read_only)|`bit` Readonly||
|[Void](#void)|`bit` Readonly||
|[Master_Document_Id](#master_document_id)|`uniqueidentifier` ||
|[Parent_Document_Id](#parent_document_id)|`uniqueidentifier` ||
|[Adjusted_Document_Id](#adjusted_document_id)|`uniqueidentifier` ||
|[Adjustment_Number](#adjustment_number)|`int` Readonly||
|[Creation_Time](#creation_time)|`datetime` Readonly||
|[Creation_User](#creation_user)|`nvarchar` Readonly||
|[Void_Time](#void_time)|`datetime` Readonly||
|[Void_User](#void_user)|`nvarchar` Readonly||
|[Document_Id](#document_id)|`uniqueidentifier` ||
|[Notes](#notes)|`nvarchar` ||
|[Payment_Transaction_Line_Id](#payment_transaction_line_id)|`uniqueidentifier` `PK`||
|[Payment_Transaction_Id](#payment_transaction_id)|`uniqueidentifier` ||
|[Allow_Overpayment](#allow_overpayment)|`bit` |1-Allows overpayment for the payment order; 0=Does not allow (default)|

## Columns

### From_Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Date

| Property | Value |
| - | - |
|Type|date|

### State

| Property | Value |
| - | - |
|Type|smallint|

### Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Payment_Account_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Total_Amount

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Total_Amount_Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Amount

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Covered_Order_Amount

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Payment_Order_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_No

| Property | Value |
| - | - |
|Type|nvarchar|

### To_Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Read_Only

| Property | Value |
| - | - |
|Type|bit|

### Void

| Property | Value |
| - | - |
|Type|bit|

### Master_Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Parent_Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Adjusted_Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Adjustment_Number

| Property | Value |
| - | - |
|Type|int|

### Creation_Time

| Property | Value |
| - | - |
|Type|datetime|

### Creation_User

| Property | Value |
| - | - |
|Type|nvarchar|

### Void_Time

| Property | Value |
| - | - |
|Type|datetime|

### Void_User

| Property | Value |
| - | - |
|Type|nvarchar|

### Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar|

### Payment_Transaction_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Payment_Transaction_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Allow_Overpayment

| Property | Value |
| - | - |
|Type|bit|


