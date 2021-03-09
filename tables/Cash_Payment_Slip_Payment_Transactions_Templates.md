# Table Cash_Payment_Slip_Payment_Transactions_Templates

Contains options for generation of payment transactions. Each option set is assigned to specific generation route. Entity: Cash_Payment_Slip_Payment_Transactions_Templates (Introduced in version 19.1)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Id](#id)|`uniqueidentifier` `PK`||
|[Route_Id](#route_id)|`uniqueidentifier` |The route to which the current option set is assigned.|
|[CreateIncomePayments](#createincomepayments)|`bit` |True if the generation creates payment transactions for Payment Slip Amounts with direction Income.|
|[CreateExpensePayments](#createexpensepayments)|`bit` |True if the generation creates payment transactions for Payment Slip Amounts with direction Expense.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Route_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### CreateIncomePayments

| Property | Value |
| - | - |
|Type|bit|

### CreateExpensePayments

| Property | Value |
| - | - |
|Type|bit|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


