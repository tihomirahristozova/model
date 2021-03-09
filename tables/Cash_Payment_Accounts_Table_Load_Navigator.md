# Query Cash_Payment_Accounts_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Payment_Account_Id](#payment_account_id)|`uniqueidentifier` `PK`||
|[Payment_Account_Name](#payment_account_name)|`nvarchar` `ML`||
|[Currency_Id](#currency_id)|`uniqueidentifier` |The currency in which the movements for this payment account will be recorded.|
|[Payment_Account_Code](#payment_account_code)|`nvarchar` ||
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` ||
|[Bank_Account_Id](#bank_account_id)|`uniqueidentifier` ||
|[Is_Active](#is_active)|`bit` ||
|[Enterprise_Company_Location_Id](#enterprise_company_location_id)|`uniqueidentifier` ||
|[Payment_Type_Id](#payment_type_id)|`uniqueidentifier` |Specifies the payment type used to pay, when using this payment account. NULL when the payment type is unknown or unspecified.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Payment_Account_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Payment_Account_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Payment_Account_Code

| Property | Value |
| - | - |
|Type|nvarchar|

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


