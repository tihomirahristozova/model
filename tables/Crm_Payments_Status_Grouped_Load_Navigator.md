# Query Crm_Payments_Status_Grouped_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Ref_Invoice_Apply_Date](#ref_invoice_apply_date)|`datetime` ||
|[Document_Date](#document_date)|`date` ||
|[State](#state)|`smallint` Allowed: `0`, `5`, `10`, `20`, `30`, `40`, `50`, Readonly||
|[User_Status_Id](#user_status_id)|`uniqueidentifier` Readonly||
|[Enterprise_Company_Location_Id](#enterprise_company_location_id)|`uniqueidentifier` ||
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
|[Ref_Document_Type_Id](#ref_document_type_id)|`uniqueidentifier` ||
|[Ref_Document_No](#ref_document_no)|`nvarchar` ||
|[Ref_Document_Date](#ref_document_date)|`datetime` ||
|[Payment_Account_Id](#payment_account_id)|`uniqueidentifier` ||
|[Installment_Number](#installment_number)|`int` ||
|[Ref_Invoice_Document_Type_Id](#ref_invoice_document_type_id)|`uniqueidentifier` ||
|[Ref_Invoice_Document_No](#ref_invoice_document_no)|`nvarchar` ||
|[Ref_Invoice_Document_Date](#ref_invoice_document_date)|`datetime` ||
|[Is_Amount_With_VAT](#is_amount_with_vat)|`bit` ||
|[Location_Party_Id](#location_party_id)|`uniqueidentifier` ||
|[Bill_To](#bill_to)|`nvarchar` Allowed: `C`, `L`||
|[Payment_Type_Id](#payment_type_id)|`uniqueidentifier` ||
|[Payment_Deferment_Days](#payment_deferment_days)|`int` ||
|[Area_Id](#area_id)|`uniqueidentifier` ||
|[Main_Payment_Order](#main_payment_order)|`uniqueidentifier` `PK`||
|[Document_Notes](#document_notes)|`nvarchar` ||
|[Payment_Orders_Count](#payment_orders_count)|`int` ||
|[Responsible_Person_Id](#responsible_person_id)|`uniqueidentifier` ||
|[Responsible_Person_Party_Id](#responsible_person_party_id)|`uniqueidentifier` ||
|[Sales_Person_Id](#sales_person_id)|`uniqueidentifier` `PK`||
|[Sales_Person_Group_Id](#sales_person_group_id)|`uniqueidentifier` ||
|[Customer_Id](#customer_id)|`uniqueidentifier` ||
|[Location_Customer_Id](#location_customer_id)|`uniqueidentifier` ||
|[From_Company_Division_Id](#from_company_division_id)|`uniqueidentifier` ||
|[To_Company_Division_Id](#to_company_division_id)|`uniqueidentifier` ||
|[Grace_Period_Days](#grace_period_days)|`int` ||
|[Due_Start_Date](#due_start_date)|`date` ||
|[Last_Payment_Transaction_Date](#last_payment_transaction_date)|`datetime` |Date of the last payment covering amount from this payment order.|
|[Area_Id_L1_Name](#area_id_l1_name)|`nvarchar` `ML`||
|[Area_Id_L2_Name](#area_id_l2_name)|`nvarchar` `ML`||
|[Area_Id_L3_Name](#area_id_l3_name)|`nvarchar` `ML`||
|[Area_Id_L4_Name](#area_id_l4_name)|`nvarchar` `ML`||
|[Area_Id_L5_Name](#area_id_l5_name)|`nvarchar` `ML`||
|[Area_Id_L6_Name](#area_id_l6_name)|`nvarchar` `ML`||
|[Sales_Person_Group_Id_L1_Name](#sales_person_group_id_l1_name)|`nvarchar` `ML`||
|[Sales_Person_Group_Id_L2_Name](#sales_person_group_id_l2_name)|`nvarchar` `ML`||
|[Sales_Person_Group_Id_L3_Name](#sales_person_group_id_l3_name)|`nvarchar` `ML`||
|[Sales_Person_Group_Id_L4_Name](#sales_person_group_id_l4_name)|`nvarchar` `ML`||
|[Sales_Person_Group_Id_L5_Name](#sales_person_group_id_l5_name)|`nvarchar` `ML`||
|[Sales_Person_Group_Id_L6_Name](#sales_person_group_id_l6_name)|`nvarchar` `ML`||

## Columns

### Ref_Invoice_Apply_Date

| Property | Value |
| - | - |
|Type|datetime|

### Document_Date

| Property | Value |
| - | - |
|Type|date|

### State

| Property | Value |
| - | - |
|Type|smallint|

### User_Status_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Enterprise_Company_Location_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

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

### Location_Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Bill_To

| Property | Value |
| - | - |
|Type|nvarchar|

### Payment_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Payment_Deferment_Days

| Property | Value |
| - | - |
|Type|int|

### Area_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Main_Payment_Order

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Notes

| Property | Value |
| - | - |
|Type|nvarchar|

### Payment_Orders_Count

| Property | Value |
| - | - |
|Type|int|

### Responsible_Person_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Responsible_Person_Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Sales_Person_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Sales_Person_Group_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Customer_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Location_Customer_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### From_Company_Division_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### To_Company_Division_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Grace_Period_Days

| Property | Value |
| - | - |
|Type|int|

### Due_Start_Date

| Property | Value |
| - | - |
|Type|date|

### Last_Payment_Transaction_Date

| Property | Value |
| - | - |
|Type|datetime|

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

### Sales_Person_Group_Id_L1_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Sales_Person_Group_Id_L2_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Sales_Person_Group_Id_L3_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Sales_Person_Group_Id_L4_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Sales_Person_Group_Id_L5_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Sales_Person_Group_Id_L6_Name

| Property | Value |
| - | - |
|Type|nvarchar|


