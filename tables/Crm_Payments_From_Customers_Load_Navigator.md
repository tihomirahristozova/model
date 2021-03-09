# Query Crm_Payments_From_Customers_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Customer_Id](#customer_id)|`uniqueidentifier` ||
|[Location_Customer_Id](#location_customer_id)|`uniqueidentifier` ||
|[Sales_Person_Id](#sales_person_id)|`uniqueidentifier` `PK`||
|[Sales_Person_Group_Id](#sales_person_group_id)|`uniqueidentifier` ||
|[From_Party_Id](#from_party_id)|`uniqueidentifier` ||
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` ||
|[Document_Type_Id](#document_type_id)|`uniqueidentifier` ||
|[Document_No](#document_no)|`nvarchar` ||
|[Document_Date](#document_date)|`date` ||
|[Reference_Date](#reference_date)|`datetime` ||
|[State](#state)|`smallint` Allowed: `0`, `5`, `10`, `20`, `30`, `40`, `50`, Readonly||
|[Void](#void)|`bit` Readonly||
|[To_Party_Id](#to_party_id)|`uniqueidentifier` ||
|[Currency_Directory_Id](#currency_directory_id)|`uniqueidentifier` ||
|[Master_Document_Id](#master_document_id)|`uniqueidentifier` ||
|[Parent_Document_Id](#parent_document_id)|`uniqueidentifier` ||
|[Adjusted_Document_Id](#adjusted_document_id)|`uniqueidentifier` Readonly||
|[Adjustment_Number](#adjustment_number)|`int` Readonly||
|[Creation_Time](#creation_time)|`datetime` Readonly||
|[Creation_User](#creation_user)|`nvarchar` Readonly||
|[Void_Time](#void_time)|`datetime` Readonly||
|[Void_User](#void_user)|`nvarchar` Readonly||
|[Adjustment_Time](#adjustment_time)|`datetime` Readonly||
|[Adjustment_User](#adjustment_user)|`nvarchar` Readonly||
|[Read_Only](#read_only)|`bit` Readonly||
|[Document_Notes](#document_notes)|`nvarchar` ||
|[Document_Version](#document_version)|`int` Readonly||
|[Responsible_Person_Id](#responsible_person_id)|`uniqueidentifier` ||
|[Void_Reason](#void_reason)|`nvarchar` Readonly||
|[Reverse_Of_Document_Id](#reverse_of_document_id)|`uniqueidentifier` Readonly||
|[Enterprise_Company_Location_Id](#enterprise_company_location_id)|`uniqueidentifier` ||
|[Planning_Only](#planning_only)|`bit` Readonly||
|[Prime_Cause_Document_Id](#prime_cause_document_id)|`uniqueidentifier` ||
|[Release_Time](#release_time)|`datetime` Readonly||
|[Complete_Time](#complete_time)|`datetime` Readonly||
|[Parent_Document_Relationship_Type](#parent_document_relationship_type)|`nvarchar` Allowed: `S`, `N`, Readonly||
|[Reference_Document_No](#reference_document_no)|`nvarchar` ||
|[User_Status_Id](#user_status_id)|`uniqueidentifier` Readonly||
|[From_Company_Division_Id](#from_company_division_id)|`uniqueidentifier` ||
|[To_Company_Division_Id](#to_company_division_id)|`uniqueidentifier` ||
|[Entity_Name](#entity_name)|`nvarchar` ||
|[Document_Id](#document_id)|`uniqueidentifier` ||
|[Payment_Transaction_Notes](#payment_transaction_notes)|`nvarchar` ||
|[Payment_Account_Id](#payment_account_id)|`uniqueidentifier` ||
|[Total_Amount](#total_amount)|`decimal(0, 0)` ||
|[Total_Amount_Currency_Id](#total_amount_currency_id)|`uniqueidentifier` ||
|[Payment_Slip_Id](#payment_slip_id)|`uniqueidentifier` ||
|[Payment_Slip_No](#payment_slip_no)|`nvarchar` ||
|[Requires_Allocation](#requires_allocation)|`bit` ||
|[Direction](#direction)|`nvarchar` Allowed: `I`, `R`||
|[Payment_Reason_Id](#payment_reason_id)|`uniqueidentifier` ||
|[Is_Single_Execution](#is_single_execution)|`bit` Readonly||
|[Is_Released](#is_released)|`bit` Readonly||
|[Payment_Type_Id](#payment_type_id)|`uniqueidentifier` |When not NULL specifies the payment type for the sales order|
|[Fiscal_Printer_Pos_Device_Id](#fiscal_printer_pos_device_id)|`uniqueidentifier` |When not NULL, contains the actual fiscal printer on which the fiscal note is printed.|
|[Parent_Payment_Slip_Amount_Id](#parent_payment_slip_amount_id)|`uniqueidentifier` |The Payment Slip Amount, which the current payment transaction fulfills . NULL when the current document does not execute any Payment Slip Amount.|
|[Pos_Location_Id](#pos_location_id)|`uniqueidentifier` |For POS Sales Order payments. Specifies the POS Location, in which the payment is performed. Null when the payment transaction is not created for a POS Sale Order.|
|[Pos_Operator_Id](#pos_operator_id)|`uniqueidentifier` |For POS Sales Order payments. Specifies the POS Operator, who created the payment order. Null when the payment transaction is not created for a POS Sale Order.|
|[Original_Payment_Transaction_Id](#original_payment_transaction_id)|`uniqueidentifier` ||
|[Reversal_Reason](#reversal_reason)|`nvarchar` Allowed: `OPE`, `TBR`, `REF`||
|[Payment_Transaction_Line_Id](#payment_transaction_line_id)|`uniqueidentifier` `PK`||
|[Payment_Transaction_Id](#payment_transaction_id)|`uniqueidentifier` ||
|[Amount](#amount)|`decimal(0, 0)` ||
|[Covered_Order_Amount](#covered_order_amount)|`decimal(0, 0)` ||
|[Payment_Order_Id](#payment_order_id)|`uniqueidentifier` ||
|[Payment_Transaction_Line_Notes](#payment_transaction_line_notes)|`nvarchar` ||
|[Allow_Overpayment](#allow_overpayment)|`bit` ||
|[Ref_Document_Id](#ref_document_id)|`uniqueidentifier` ||
|[Ref_Document_Type_Id](#ref_document_type_id)|`uniqueidentifier` ||
|[Ref_Document_No](#ref_document_no)|`nvarchar` ||
|[Ref_Document_Date](#ref_document_date)|`datetime` ||
|[Party_Id](#party_id)|`uniqueidentifier` ||
|[Due_Date](#due_date)|`datetime` ||
|[Payment_Order_Total_Amount](#payment_order_total_amount)|`decimal(0, 0)` ||
|[Payment_Order_Total_Amount_Currency_Id](#payment_order_total_amount_currency_id)|`uniqueidentifier` ||
|[Notes](#notes)|`nvarchar` ||
|[Payment_Order_Payment_Account_Id](#payment_order_payment_account_id)|`uniqueidentifier` ||
|[Installment_Number](#installment_number)|`int` ||
|[Ref_Invoice_Document_Id](#ref_invoice_document_id)|`uniqueidentifier` ||
|[Ref_Invoice_Document_Type_Id](#ref_invoice_document_type_id)|`uniqueidentifier` ||
|[Ref_Invoice_Document_No](#ref_invoice_document_no)|`nvarchar` ||
|[Ref_Invoice_Document_Date](#ref_invoice_document_date)|`datetime` ||
|[Invoice_Amount](#invoice_amount)|`decimal(0, 0)` ||
|[Invoice_Amount_Currency_Id](#invoice_amount_currency_id)|`uniqueidentifier` ||
|[Is_Amount_With_VAT](#is_amount_with_vat)|`bit` ||
|[Location_Party_Id](#location_party_id)|`uniqueidentifier` ||
|[Bill_To](#bill_to)|`nvarchar` Allowed: `C`, `L`||
|[Ref_Invoice_Apply_Date](#ref_invoice_apply_date)|`datetime` ||
|[Allow_Close_Not_Paid](#allow_close_not_paid)|`bit` ||
|[Due_Start_Date](#due_start_date)|`date` ||
|[Payment_Order_Is_Single_Execution](#payment_order_is_single_execution)|`bit` Readonly||
|[Payment_Order_Is_Released](#payment_order_is_released)|`bit` Readonly||
|[Payment_Order_Fiscal_Printer_Pos_Device_Id](#payment_order_fiscal_printer_pos_device_id)|`uniqueidentifier` |When not NULL, contains suggested fiscal printer for printing fiscal notes upon payment.|
|[Area_Id](#area_id)|`uniqueidentifier` ||
|[Payment_Order_Responsible_Person_Id](#payment_order_responsible_person_id)|`uniqueidentifier` ||
|[Payment_Account_Name](#payment_account_name)|`nvarchar` `ML`||
|[Payment_Account_Currency_Id](#payment_account_currency_id)|`uniqueidentifier` ||
|[Payment_Account_Code](#payment_account_code)|`nvarchar` ||
|[Payment_Account_Enterprise_Company_Id](#payment_account_enterprise_company_id)|`uniqueidentifier` ||
|[Bank_Account_Id](#bank_account_id)|`uniqueidentifier` ||
|[Payment_Account_Is_Active](#payment_account_is_active)|`bit` ||
|[Payment_Account_Enterprise_Company_Location_Id](#payment_account_enterprise_company_location_id)|`uniqueidentifier` ||
|[Payment_Account_Payment_Type_Id](#payment_account_payment_type_id)|`uniqueidentifier` ||
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

### Customer_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Location_Customer_Id

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

### From_Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

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

### Document_Date

| Property | Value |
| - | - |
|Type|date|

### Reference_Date

| Property | Value |
| - | - |
|Type|datetime|

### State

| Property | Value |
| - | - |
|Type|smallint|

### Void

| Property | Value |
| - | - |
|Type|bit|

### To_Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Currency_Directory_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Master_Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Parent_Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Adjusted_Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Adjustment_Number

| Property | Value |
| - | - |
|Type|int|

### Creation_Time

| Property | Value |
| - | - |
|Type|datetime|

### Creation_User

| Property | Value |
| - | - |
|Type|nvarchar|

### Void_Time

| Property | Value |
| - | - |
|Type|datetime|

### Void_User

| Property | Value |
| - | - |
|Type|nvarchar|

### Adjustment_Time

| Property | Value |
| - | - |
|Type|datetime|

### Adjustment_User

| Property | Value |
| - | - |
|Type|nvarchar|

### Read_Only

| Property | Value |
| - | - |
|Type|bit|

### Document_Notes

| Property | Value |
| - | - |
|Type|nvarchar|

### Document_Version

| Property | Value |
| - | - |
|Type|int|

### Responsible_Person_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Void_Reason

| Property | Value |
| - | - |
|Type|nvarchar|

### Reverse_Of_Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Enterprise_Company_Location_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Planning_Only

| Property | Value |
| - | - |
|Type|bit|

### Prime_Cause_Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Release_Time

| Property | Value |
| - | - |
|Type|datetime|

### Complete_Time

| Property | Value |
| - | - |
|Type|datetime|

### Parent_Document_Relationship_Type

| Property | Value |
| - | - |
|Type|nvarchar|

### Reference_Document_No

| Property | Value |
| - | - |
|Type|nvarchar|

### User_Status_Id

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

### Entity_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Payment_Transaction_Notes

| Property | Value |
| - | - |
|Type|nvarchar|

### Payment_Account_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Total_Amount

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Total_Amount_Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Payment_Slip_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Payment_Slip_No

| Property | Value |
| - | - |
|Type|nvarchar|

### Requires_Allocation

| Property | Value |
| - | - |
|Type|bit|

### Direction

| Property | Value |
| - | - |
|Type|nvarchar|

### Payment_Reason_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Is_Single_Execution

| Property | Value |
| - | - |
|Type|bit|

### Is_Released

| Property | Value |
| - | - |
|Type|bit|

### Payment_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Fiscal_Printer_Pos_Device_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Parent_Payment_Slip_Amount_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Pos_Location_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Pos_Operator_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Original_Payment_Transaction_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Reversal_Reason

| Property | Value |
| - | - |
|Type|nvarchar|

### Payment_Transaction_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Payment_Transaction_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Amount

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Covered_Order_Amount

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Payment_Order_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Payment_Transaction_Line_Notes

| Property | Value |
| - | - |
|Type|nvarchar|

### Allow_Overpayment

| Property | Value |
| - | - |
|Type|bit|

### Ref_Document_Id

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

### Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Due_Date

| Property | Value |
| - | - |
|Type|datetime|

### Payment_Order_Total_Amount

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Payment_Order_Total_Amount_Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar|

### Payment_Order_Payment_Account_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Installment_Number

| Property | Value |
| - | - |
|Type|int|

### Ref_Invoice_Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

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

### Invoice_Amount

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Invoice_Amount_Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

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

### Ref_Invoice_Apply_Date

| Property | Value |
| - | - |
|Type|datetime|

### Allow_Close_Not_Paid

| Property | Value |
| - | - |
|Type|bit|

### Due_Start_Date

| Property | Value |
| - | - |
|Type|date|

### Payment_Order_Is_Single_Execution

| Property | Value |
| - | - |
|Type|bit|

### Payment_Order_Is_Released

| Property | Value |
| - | - |
|Type|bit|

### Payment_Order_Fiscal_Printer_Pos_Device_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Area_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Payment_Order_Responsible_Person_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Payment_Account_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Payment_Account_Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Payment_Account_Code

| Property | Value |
| - | - |
|Type|nvarchar|

### Payment_Account_Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Bank_Account_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Payment_Account_Is_Active

| Property | Value |
| - | - |
|Type|bit|

### Payment_Account_Enterprise_Company_Location_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Payment_Account_Payment_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

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


