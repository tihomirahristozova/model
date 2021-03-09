# Table Crm_Sales_Order_Payment_Plans

Payment plan of a sales order. Entity: Crm_Sales_Order_Payment_Plans

## Owner Tables Hierarchy

* [Crm_Sales_Orders](Crm_Sales_Orders.md)
* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Sales_Order_Payment_Plan_Id](#sales_order_payment_plan_id)|`uniqueidentifier` `PK`|Unique identification of the payment plan|
|[Sales_Order_Id](#sales_order_id)|`uniqueidentifier` ||
|[Installment_Number](#installment_number)|`int` |Consequtive installment number. Used for identifying different payments generated according this payment plan.|
|[Due_Date_Form_Method](#due_date_form_method)|`nvarchar(3)` Allowed: `EXP`, `INV`, `SLS`, `SDD`, `IDD`|Method to determine the payment due date. SLS = Use sales order date, INV = Use invoice date, EXP = Specify the date explicitly, SDD = Sales order due date, IDD = Invoice due date|
|[Explicit_Payment_Due_Date](#explicit_payment_due_date)|`datetime` |Explicitly specified payment due date. Must be filled if and only if Due_Date_Form_Method = 'EXP'|
|[Payment_Term_Days](#payment_term_days)|`int` |Payment term in days, which are to be added to form the payment due date. 0 means that the date determined by Due_Date_Form_Method and Explicit_Payment_Due_Date is taken as due date.|
|[Amount_Percent](#amount_percent)|`decimal(7, 6)` |Percent of the sales order amount to be payed.|
|[Remainder](#remainder)|`bit` |Indicates wheather this amount is the remainder of the document. Amount = Total amount of the sales order - explicitly specified amounts in the plan (by Amount_Percent or Amount).|
|[Amount](#amount)|`decimal(14, 2)` |Amount to be payed.|
|[Notes](#notes)|`nvarchar(254)` ||
|[Explicit_Payment_Due_Start_Date](#explicit_payment_due_start_date)|`date` |Explicitly specified date on which the payment becomes executable. Can be specified only when date formation method is 'Set explicit date'.|
|[Payment_Start_Days](#payment_start_days)|`int` |Number of days until the payment becomes executable. The days are counted, starting with the date, specified by due date formation method.|
|[Payment_Type_Id](#payment_type_id)|`uniqueidentifier` |Specifies the expected payment type. NULL means that there is no expected payment type. For POS implementations, this can be used to denote the payment type which actually occurred.|
|[Payment_Account_Id](#payment_account_id)|`uniqueidentifier` |Specifies the payment account towards which the payment is expected. NULL means that there is no expectation for payment account. For POS implementations, this can be used to denote the payment account in which the payment actually occurred.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Sales_Order_Payment_Plan_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Sales_Order_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Installment_Number

| Property | Value |
| - | - |
|Type|int|

### Due_Date_Form_Method

| Property | Value |
| - | - |
|Type|nvarchar(3)|

### Explicit_Payment_Due_Date

| Property | Value |
| - | - |
|Type|datetime|

### Payment_Term_Days

| Property | Value |
| - | - |
|Type|int|

### Amount_Percent

| Property | Value |
| - | - |
|Type|decimal(7, 6)|

### Remainder

| Property | Value |
| - | - |
|Type|bit|

### Amount

| Property | Value |
| - | - |
|Type|decimal(14, 2)|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Explicit_Payment_Due_Start_Date

| Property | Value |
| - | - |
|Type|date|

### Payment_Start_Days

| Property | Value |
| - | - |
|Type|int|

### Payment_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Payment_Account_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


