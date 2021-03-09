# Table Cash_Payment_Types

Describes the way of payment. For example: in cash, by bank transfer, with credit card, etc. Entity: Cash_Payment_Types

## Summary

| Name | Type | Description |
| - | - | --- |
|[Payment_Type_Id](#payment_type_id)|`uniqueidentifier` `PK`||
|[Payment_Type_Name](#payment_type_name)|`nvarchar(254)` `ML`||
|[Default_Payment_Account_Id](#default_payment_account_id)|`uniqueidentifier` |When not NULL specifies the default payment account to use associated with this payment type|
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` ||
|[System_Type](#system_type)|`nvarchar(2)` Allowed: `CH`, `CD`, `BT`, `TK`, `CK`, `U1`, `U2`, `U3`, `PK`, `IU`, `DG`, `OT`|Not NULL only when this is one of the system payment types. CS=Cash; CD=By Card; BT=Bank Transfer|
|[Payment_Type_Code](#payment_type_code)|`nvarchar(16)` |The payment type unique code|
|[Row_Version](#row_version)|`timestamp` ||
|[Is_Active](#is_active)|`bit` |Indicates wheather the payment type is active and usable for choosing in new documents.|

## Columns

### Payment_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Payment_Type_Name

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Default_Payment_Account_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### System_Type

| Property | Value |
| - | - |
|Type|nvarchar(2)|

### Payment_Type_Code

| Property | Value |
| - | - |
|Type|nvarchar(16)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|

### Is_Active

| Property | Value |
| - | - |
|Type|bit|


