# Query Crm_Default_Sales_Order_Payment_Plans_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Default_Sales_Order_Payment_Plan_Id](#default_sales_order_payment_plan_id)|`uniqueidentifier` `PK`||
|[Document_Type_Id](#document_type_id)|`uniqueidentifier` ||
|[Installment_Number](#installment_number)|`int` ||
|[Due_Date_Form_Method](#due_date_form_method)|`nvarchar` Allowed: `EXP`, `INV`, `SLS`, `SDD`, `IDD`||
|[Payment_Term_Days](#payment_term_days)|`int` ||
|[Amount_Percent](#amount_percent)|`decimal(0, 0)` ||
|[Remainder](#remainder)|`bit` ||
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
|Type|nvarchar|

### Payment_Term_Days

| Property | Value |
| - | - |
|Type|int|

### Amount_Percent

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

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


