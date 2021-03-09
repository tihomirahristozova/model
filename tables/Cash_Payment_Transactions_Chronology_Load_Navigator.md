# Query Cash_Payment_Transactions_Chronology_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[From_Party_Id](#from_party_id)|`uniqueidentifier` ||
|[Document_Date](#document_date)|`date` ||
|[State](#state)|`smallint` Allowed: `0`, `5`, `10`, `20`, `30`, `40`, `50`, Readonly||
|[Party_Id](#party_id)|`uniqueidentifier` ||
|[Payment_Account_Id](#payment_account_id)|`uniqueidentifier` ||
|[Start_Balance](#start_balance)|`decimal(0, 0)` ||
|[Income_Amount](#income_amount)|`decimal(0, 0)` ||
|[Expense_Amount](#expense_amount)|`decimal(0, 0)` ||
|[End_Balance](#end_balance)|`decimal(0, 0)` ||
|[Total_Amount_Currency_Id](#total_amount_currency_id)|`uniqueidentifier` ||
|[Payment_Slip_No](#payment_slip_no)|`nvarchar` ||
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` ||
|[Enterprise_Company_Location_Id](#enterprise_company_location_id)|`uniqueidentifier` ||
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
|[Document_Notes](#document_notes)|`nvarchar` ||
|[Document_Id](#document_id)|`uniqueidentifier` ||
|[Payment_Transaction_Id](#payment_transaction_id)|`uniqueidentifier` `PK`||
|[Requires_Allocation](#requires_allocation)|`bit` ||
|[Direction](#direction)|`nvarchar` Allowed: `I`, `R`||
|[Notes](#notes)|`nvarchar` ||
|[Payment_Account_Name](#payment_account_name)|`nvarchar` `ML`||
|[Payment_Account_Currency_Id](#payment_account_currency_id)|`uniqueidentifier` |The currency in which the movements for this payment account will be recorded.|
|[Payment_Account_Code](#payment_account_code)|`nvarchar` ||
|[Payment_Account_Enterprise_Company_Id](#payment_account_enterprise_company_id)|`uniqueidentifier` ||
|[Bank_Account_Id](#bank_account_id)|`uniqueidentifier` |The bank account, which is represented by this payment account.|
|[Payment_Account_Is_Active](#payment_account_is_active)|`bit` |Indicates wheather the payment account is currently used (active).|
|[Payment_Account_Enterprise_Company_Location_Id](#payment_account_enterprise_company_location_id)|`uniqueidentifier` ||
|[Payment_Account_Payment_Type_Id](#payment_account_payment_type_id)|`uniqueidentifier` |Specifies the payment type used to pay, when using this payment account. NULL when the payment type is unknown or unspecified.|
|[Parent_Payment_Slip_Amount_Id](#parent_payment_slip_amount_id)|`uniqueidentifier` |The Payment Slip Amount, which the current payment transaction fulfills . NULL when the current document does not execute any Payment Slip Amount.|

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

### Start_Balance

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Income_Amount

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Expense_Amount

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### End_Balance

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Total_Amount_Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Payment_Slip_No

| Property | Value |
| - | - |
|Type|nvarchar|

### Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Enterprise_Company_Location_Id

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

### Document_Notes

| Property | Value |
| - | - |
|Type|nvarchar|

### Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Payment_Transaction_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Requires_Allocation

| Property | Value |
| - | - |
|Type|bit|

### Direction

| Property | Value |
| - | - |
|Type|nvarchar|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar|

### Payment_Account_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Payment_Account_Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Payment_Account_Code

| Property | Value |
| - | - |
|Type|nvarchar|

### Payment_Account_Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Bank_Account_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Payment_Account_Is_Active

| Property | Value |
| - | - |
|Type|bit|

### Payment_Account_Enterprise_Company_Location_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Payment_Account_Payment_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Parent_Payment_Slip_Amount_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|


