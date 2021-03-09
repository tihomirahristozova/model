# Query Cash_Payments_Status_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Document_Date](#document_date)|`date` ||
|[State](#state)|`smallint` Allowed: `0`, `5`, `10`, `20`, `30`, `40`, `50`, Readonly||
|[Party_Id](#party_id)|`uniqueidentifier` ||
|[Party_Code](#party_code)|`nvarchar` Readonly||
|[Direction](#direction)|`nvarchar` Allowed: `I`, `R`||
|[Total_Amount](#total_amount)|`decimal(0, 0)` ||
|[Covered_Amount](#covered_amount)|`decimal(0, 0)` ||
|[Remaining_Amount](#remaining_amount)|`decimal(0, 0)` ||
|[Total_Amount_Currency_Id](#total_amount_currency_id)|`uniqueidentifier` ||
|[Due_Date](#due_date)|`datetime` ||
|[Overdue_Days](#overdue_days)|`int` ||
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` ||
|[Document_Type_Id](#document_type_id)|`uniqueidentifier` ||
|[Document_No](#document_no)|`nvarchar` ||
|[Ref_Document_Type_Id](#ref_document_type_id)|`uniqueidentifier` ||
|[Ref_Document_No](#ref_document_no)|`nvarchar` ||
|[Ref_Document_Date](#ref_document_date)|`datetime` ||
|[Payment_Order_Id](#payment_order_id)|`uniqueidentifier` `PK`||
|[Payment_Account_Id](#payment_account_id)|`uniqueidentifier` ||
|[Installment_Number](#installment_number)|`int` ||
|[Ref_Invoice_Document_Type_Id](#ref_invoice_document_type_id)|`uniqueidentifier` ||
|[Ref_Invoice_Document_No](#ref_invoice_document_no)|`nvarchar` ||
|[Ref_Invoice_Document_Date](#ref_invoice_document_date)|`datetime` ||
|[Is_Amount_With_VAT](#is_amount_with_vat)|`bit` ||
|[Payment_Deferment_Days](#payment_deferment_days)|`int` ||
|[Area_Id](#area_id)|`uniqueidentifier` ||
|[Location_Party_Id](#location_party_id)|`uniqueidentifier` ||
|[Due_Start_Date](#due_start_date)|`date` |The date at which the payment becomes executable. NULL means the payment is executable at all times.|
|[Area_Id_L1_Name](#area_id_l1_name)|`nvarchar` `ML`||
|[Area_Id_L2_Name](#area_id_l2_name)|`nvarchar` `ML`||
|[Area_Id_L3_Name](#area_id_l3_name)|`nvarchar` `ML`||
|[Area_Id_L4_Name](#area_id_l4_name)|`nvarchar` `ML`||
|[Area_Id_L5_Name](#area_id_l5_name)|`nvarchar` `ML`||
|[Area_Id_L6_Name](#area_id_l6_name)|`nvarchar` `ML`||

## Columns

### Document_Date

| Property | Value |
| - | - |
|Type|date|

### State

| Property | Value |
| - | - |
|Type|smallint|

### Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Party_Code

| Property | Value |
| - | - |
|Type|nvarchar|

### Direction

| Property | Value |
| - | - |
|Type|nvarchar|

### Total_Amount

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Covered_Amount

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Remaining_Amount

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Total_Amount_Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Due_Date

| Property | Value |
| - | - |
|Type|datetime|

### Overdue_Days

| Property | Value |
| - | - |
|Type|int|

### Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_No

| Property | Value |
| - | - |
|Type|nvarchar|

### Ref_Document_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Ref_Document_No

| Property | Value |
| - | - |
|Type|nvarchar|

### Ref_Document_Date

| Property | Value |
| - | - |
|Type|datetime|

### Payment_Order_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Payment_Account_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Installment_Number

| Property | Value |
| - | - |
|Type|int|

### Ref_Invoice_Document_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Ref_Invoice_Document_No

| Property | Value |
| - | - |
|Type|nvarchar|

### Ref_Invoice_Document_Date

| Property | Value |
| - | - |
|Type|datetime|

### Is_Amount_With_VAT

| Property | Value |
| - | - |
|Type|bit|

### Payment_Deferment_Days

| Property | Value |
| - | - |
|Type|int|

### Area_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Location_Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Due_Start_Date

| Property | Value |
| - | - |
|Type|date|

### Area_Id_L1_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Area_Id_L2_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Area_Id_L3_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Area_Id_L4_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Area_Id_L5_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Area_Id_L6_Name

| Property | Value |
| - | - |
|Type|nvarchar|


