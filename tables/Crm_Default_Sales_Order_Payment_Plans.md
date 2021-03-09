# Table Crm_Default_Sales_Order_Payment_Plans

Default payment plan for new documents of the specified document type. Entity: Crm_Default_Sales_Order_Payment_Plans

## Owner Tables Hierarchy

* [Gen_Document_Types](Gen_Document_Types.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Default_Sales_Order_Payment_Plan_Id](#default_sales_order_payment_plan_id)|`uniqueidentifier` `PK`||
|[Document_Type_Id](#document_type_id)|`uniqueidentifier` ||
|[Installment_Number](#installment_number)|`int` |Consequtive installment number. Used for identifying different payments generated according this payment plan.|
|[Due_Date_Form_Method](#due_date_form_method)|`nvarchar(3)` Allowed: `EXP`, `INV`, `SLS`, `SDD`, `IDD`|Method to determine the payment due date. SLS = Use sales order date, INV = Use invoice date, EXP = Specify the date explicitly, SDD = Sales order due date, IDD = Invoice due date|
|[Payment_Term_Days](#payment_term_days)|`int` |Payment term in days, which are to be added to form the payment due date. 0 means that the date determined by Due_Date_Form_Method and Explicit_Payment_Due_Date is taken as due date.|
|[Amount_Percent](#amount_percent)|`decimal(7, 6)` |Percent of the sales order amount to be payed.|
|[Remainder](#remainder)|`bit` |Indicates wheather this amount is the remainder of the document. Amount = Total amount of the sales order - explicitly specified amounts in the plan (by Amount_Percent).|
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` |Enterprise company for which the current default installment template is valid. If enterprise company is not set then the installment template is valid for all enterprise companies.|
|[Enterprise_Company_Location_Id](#enterprise_company_location_id)|`uniqueidentifier` |Enterprise company location (within the chosen enterprise company) for which the current default installment template is valid. If enterprise company location is not set then the installment template is valid for all enterprise company locations.|
|[Payment_Account_Id](#payment_account_id)|`uniqueidentifier` |Default payment account for the current installment. NULL means that there is no default account.|
|[Payment_Type_Id](#payment_type_id)|`uniqueidentifier` |Default payment type for the current installment. NULL means that there is no default payment type.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Default_Sales_Order_Payment_Plan_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Type_Id

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

### Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Enterprise_Company_Location_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Payment_Account_Id

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


