# Table Cash_Payment_Reasons

Represents reasons for the payments. Contains both system and user-defined reasons. Entity: Cash_Payment_Reasons

## Summary

| Name | Type | Description |
| - | - | --- |
|[Payment_Reason_Id](#payment_reason_id)|`uniqueidentifier` `PK`||
|[Payment_Reason_Name](#payment_reason_name)|`nvarchar(254)` `ML`||
|[Is_System](#is_system)|`bit` Readonly|Specifies whether the payment reason is defined by the system. The system defined records are created by the system and are read-only for the user.|
|[Is_Active](#is_active)|`bit` |Specifies whether the payment reason is active and usable for choosing in new documents.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Payment_Reason_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Payment_Reason_Name

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Is_System

| Property | Value |
| - | - |
|Type|bit|

### Is_Active

| Property | Value |
| - | - |
|Type|bit|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


