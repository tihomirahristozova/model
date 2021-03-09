# Query Crm_Invoices_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Document_Id](#document_id)|`uniqueidentifier` `PK`||
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
|[Adjusted_Document_Id](#adjusted_document_id)|`uniqueidentifier` ||
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
|[Entity_Name](#entity_name)|`nvarchar` |The entity name of the document header.|
|[Customer_Type_Id](#customer_type_id)|`uniqueidentifier` ||
|[Invoice_Id](#invoice_id)|`uniqueidentifier` `PK`||
|[Customer_Id](#customer_id)|`uniqueidentifier` ||
|[Notes](#notes)|`nvarchar` ||
|[Document_Currency_Id](#document_currency_id)|`uniqueidentifier` ||
|[Payment_Type_Id](#payment_type_id)|`uniqueidentifier` ||
|[Payment_Type_Description](#payment_type_description)|`nvarchar` `ML`||
|[Payment_Account_Id](#payment_account_id)|`uniqueidentifier` ||
|[Payment_Due_Date](#payment_due_date)|`datetime` ||
|[Credit_Note_Original_Invoice_Id](#credit_note_original_invoice_id)|`uniqueidentifier` ||
|[Credit_Note_Description](#credit_note_description)|`nvarchar` ||
|[Delivery_Date](#delivery_date)|`datetime` ||
|[Deal_Type_Id](#deal_type_id)|`uniqueidentifier` ||
|[Apply_Date](#apply_date)|`date` ||
|[VAT_Notes](#vat_notes)|`nvarchar` ||
|[IsValid](#isvalid)|`bit` ||
|[Automatic_Order_Linking](#automatic_order_linking)|`bit` ||
|[Delivery_Terms_Code](#delivery_terms_code)|`nvarchar` Allowed: `EXW`, `FCA`, `FAS`, `FOB`, `CFR`, `CIF`, `CPT`, `CIP`, `DAP`, `DAT`, `DDP`, `DPU`||
|[Intrastat_Transaction_Nature_Code](#intrastat_transaction_nature_code)|`nvarchar` Allowed: `11`, `12`, `13`, `14`, `19`, `21`, `22`, `23`, `29`, `60`, `70`, `80`, `91`, `99`, `30`, `41`, `42`, `51`, `52`||
|[Intrastat_Transport_Mode_Code](#intrastat_transport_mode_code)|`nvarchar` Allowed: `1`, `2`, `3`, `4`, `5`, `6`, `7`, `8`||
|[Intrastat_Transport_Country_Id](#intrastat_transport_country_id)|`uniqueidentifier` ||
|[VAT_Cash_Reporting_Mode](#vat_cash_reporting_mode)|`bit` ||
|[Payment_Due_Start_Date](#payment_due_start_date)|`datetime` ||
|[Is_Single_Execution](#is_single_execution)|`bit` Readonly||
|[Is_Released](#is_released)|`bit` Readonly||
|[Lines_Total](#lines_total)|`decimal(0, 0)` ||
|[Amount_To_Pay](#amount_to_pay)|`decimal(0, 0)` ||
|[Credit_Notes_Amount](#credit_notes_amount)|`decimal(0, 0)` ||
|[Customer_Purchase_Order_No](#customer_purchase_order_no)|`nvarchar` ||
|[Invoice_Delivery_Date](#invoice_delivery_date)|`datetime` ||
|[Lines_Total_In_Base_Currency](#lines_total_in_base_currency)|`decimal(0, 0)` ||

## Columns

### Document_Id

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

### Customer_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Invoice_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Customer_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar|

### Document_Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Payment_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Payment_Type_Description

| Property | Value |
| - | - |
|Type|nvarchar|

### Payment_Account_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Payment_Due_Date

| Property | Value |
| - | - |
|Type|datetime|

### Credit_Note_Original_Invoice_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Credit_Note_Description

| Property | Value |
| - | - |
|Type|nvarchar|

### Delivery_Date

| Property | Value |
| - | - |
|Type|datetime|

### Deal_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Apply_Date

| Property | Value |
| - | - |
|Type|date|

### VAT_Notes

| Property | Value |
| - | - |
|Type|nvarchar|

### IsValid

| Property | Value |
| - | - |
|Type|bit|

### Automatic_Order_Linking

| Property | Value |
| - | - |
|Type|bit|

### Delivery_Terms_Code

| Property | Value |
| - | - |
|Type|nvarchar|

### Intrastat_Transaction_Nature_Code

| Property | Value |
| - | - |
|Type|nvarchar|

### Intrastat_Transport_Mode_Code

| Property | Value |
| - | - |
|Type|nvarchar|

### Intrastat_Transport_Country_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### VAT_Cash_Reporting_Mode

| Property | Value |
| - | - |
|Type|bit|

### Payment_Due_Start_Date

| Property | Value |
| - | - |
|Type|datetime|

### Is_Single_Execution

| Property | Value |
| - | - |
|Type|bit|

### Is_Released

| Property | Value |
| - | - |
|Type|bit|

### Lines_Total

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Amount_To_Pay

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Credit_Notes_Amount

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Customer_Purchase_Order_No

| Property | Value |
| - | - |
|Type|nvarchar|

### Invoice_Delivery_Date

| Property | Value |
| - | - |
|Type|datetime|

### Lines_Total_In_Base_Currency

| Property | Value |
| - | - |
|Type|decimal(0, 0)|


