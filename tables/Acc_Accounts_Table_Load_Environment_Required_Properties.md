# Procedure Acc_Accounts_Table_Load_Environment_Required_Properties


## Summary

| Name | Type | Description |
| - | - | --- |
|[Account_Required_Property_Id](#account_required_property_id)|`uniqueidentifier` `PK`||
|[Account_Id](#account_id)|`uniqueidentifier` ||
|[Property_Id](#property_id)|`uniqueidentifier` |A property of type (Entity_Name = Account Voucher Line) for which the user can specify value when entering accounting vouchers|
|[Key_Property](#key_property)|`bit` |Key properties particiate in forming the grouping key, which is the smallest unit of calculation for account balance. Non-key properties simply serve for comment and clarification purposes|
|[Key_Order](#key_order)|`int` |The key order determines in which order the values and descriptions of the properties will form the item (grouping) key and description.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Account_Required_Property_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Account_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Property_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Key_Property

| Property | Value |
| - | - |
|Type|bit|

### Key_Order

| Property | Value |
| - | - |
|Type|int|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


