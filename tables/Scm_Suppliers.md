# Table Scm_Suppliers

Contains supplier conditions (contracts). Entity: Scm_Suppliers

## Owner Tables Hierarchy

* [Gen_Parties](Gen_Parties.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Supplier_Id](#supplier_id)|`uniqueidentifier` `PK`||
|[Party_Id](#party_id)|`uniqueidentifier` ||
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` ||
|[From_Date](#from_date)|`datetime` |The date on which this party became a supplier or the date, when the supplier contract was signed.|
|[Thru_Date](#thru_date)|`datetime` |The date (inclusive) on which this party ceased to be a supplier.|
|[Supplier_Number](#supplier_number)|`nvarchar(16)` |The unique supplier number.|
|[Default_Currency_Id](#default_currency_id)|`uniqueidentifier` |The default currency for purchases from this supplier. NULL means there is no default|
|[Default_Payment_Term_Days](#default_payment_term_days)|`int` |Default payment term in days, starting from the date of receiving the invoice|
|[Default_Delivery_Term_Days](#default_delivery_term_days)|`int` |Default term in days for goods delivery, starting at the day of sending the purchase order|
|[Default_Purchase_Price_List_Id](#default_purchase_price_list_id)|`uniqueidentifier` |The default purchase price list, which shall be used for new purchase documents for this supplier.|
|[Creation_Time](#creation_time)|`datetime` Readonly||
|[Creation_User](#creation_user)|`nvarchar(64)` Readonly||
|[Update_Time](#update_time)|`datetime` Readonly||
|[Update_User](#update_user)|`nvarchar(64)` Readonly||
|[Default_Payment_Type_Id](#default_payment_type_id)|`uniqueidentifier` |When not null, specifies the default payment type which should be used for new purchase document for this supplier.|
|[Default_Payment_Account_Id](#default_payment_account_id)|`uniqueidentifier` |When not null, specifies the default payment account which should be used for new purchase document for this supplier.|
|[Supplier_Type_Id](#supplier_type_id)|`uniqueidentifier` |When not null, specifies the type of this supplier. The type is primarily used for security access differentiation of the supplier records.|
|[Default_Payment_Start_Days](#default_payment_start_days)|`int` |Default number of days until the payment becomes executable. 0 means that the payment is executable at all times.|
|[Is_Active](#is_active)|`bit` |Indicates whether the current supplier is active.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Supplier_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### From_Date

| Property | Value |
| - | - |
|Type|datetime|

### Thru_Date

| Property | Value |
| - | - |
|Type|datetime|

### Supplier_Number

| Property | Value |
| - | - |
|Type|nvarchar(16)|

### Default_Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Default_Payment_Term_Days

| Property | Value |
| - | - |
|Type|int|

### Default_Delivery_Term_Days

| Property | Value |
| - | - |
|Type|int|

### Default_Purchase_Price_List_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Creation_Time

| Property | Value |
| - | - |
|Type|datetime|

### Creation_User

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### Update_Time

| Property | Value |
| - | - |
|Type|datetime|

### Update_User

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### Default_Payment_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Default_Payment_Account_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Supplier_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Default_Payment_Start_Days

| Property | Value |
| - | - |
|Type|int|

### Is_Active

| Property | Value |
| - | - |
|Type|bit|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


