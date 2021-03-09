# Table Cash_Payment_Accounts

Payment accounts are cash, bank and other accounts, which are used in payments. Payment accounts are frequently used as analytical dimensions (properties) for general ledger accounts. Entity: Cash_Payment_Accounts

## Summary

| Name | Type | Description |
| - | - | --- |
|[Payment_Account_Name](#payment_account_name)|`nvarchar(50)` `ML`||
|[Currency_Id](#currency_id)|`uniqueidentifier` |The currency in which the movements for this payment account will be recorded.|
|[Payment_Account_Id](#payment_account_id)|`uniqueidentifier` `PK`||
|[Payment_Account_Code](#payment_account_code)|`nvarchar(16)` ||
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` ||
|[Bank_Account_Id](#bank_account_id)|`uniqueidentifier` |The bank account, which is represented by this payment account.|
|[Is_Active](#is_active)|`bit` |Indicates wheather the payment account is currently used (active).|
|[Access_Key_Id](#access_key_id)|`uniqueidentifier` ||
|[Enterprise_Company_Location_Id](#enterprise_company_location_id)|`uniqueidentifier` ||
|[Payment_Type_Id](#payment_type_id)|`uniqueidentifier` |Specifies the payment type used to pay, when using this payment account. NULL when the payment type is unknown or unspecified.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Payment_Account_Name

| Property | Value |
| - | - |
|Type|nvarchar(50)|

### Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Payment_Account_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Payment_Account_Code

| Property | Value |
| - | - |
|Type|nvarchar(16)|

### Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Bank_Account_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Is_Active

| Property | Value |
| - | - |
|Type|bit|

### Access_Key_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Enterprise_Company_Location_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Payment_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


