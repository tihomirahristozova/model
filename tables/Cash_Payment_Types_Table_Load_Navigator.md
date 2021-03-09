# Query Cash_Payment_Types_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Payment_Type_Id](#payment_type_id)|`uniqueidentifier` `PK`||
|[Payment_Type_Name](#payment_type_name)|`nvarchar` `ML`||
|[Default_Payment_Account_Id](#default_payment_account_id)|`uniqueidentifier` ||
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` ||
|[System_Type](#system_type)|`nvarchar` Allowed: `CH`, `CD`, `BT`, `TK`, `CK`, `U1`, `U2`, `U3`, `PK`, `IU`, `DG`, `OT`||
|[Payment_Type_Code](#payment_type_code)|`nvarchar` |The payment type unique code|
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
|Type|nvarchar|

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
|Type|nvarchar|

### Payment_Type_Code

| Property | Value |
| - | - |
|Type|nvarchar|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|

### Is_Active

| Property | Value |
| - | - |
|Type|bit|


