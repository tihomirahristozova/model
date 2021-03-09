# Query Scm_Purchase_Order_Lines_Not_Received_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Id](#id)|`uniqueidentifier` `PK`||
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
|[Row_Version](#row_version)|`timestamp` ||
|[Purchase_Order_Id](#purchase_order_id)|`uniqueidentifier` `PK`||
|[Supplier_Id](#supplier_id)|`uniqueidentifier` ||
|[Store_Id](#store_id)|`uniqueidentifier` ||
|[Planned_Release_Date](#planned_release_date)|`datetime` ||
|[Planned_Delivery_Date](#planned_delivery_date)|`datetime` ||
|[Document_Currency_Id](#document_currency_id)|`uniqueidentifier` ||
|[Notes](#notes)|`nvarchar` ||
|[Payment_Due_Date](#payment_due_date)|`datetime` ||
|[Invoice_Document_No](#invoice_document_no)|`nvarchar` ||
|[Purchase_Price_List_Id](#purchase_price_list_id)|`uniqueidentifier` ||
|[Payment_Account_Id](#payment_account_id)|`uniqueidentifier` ||
|[Payment_Type_Id](#payment_type_id)|`uniqueidentifier` ||
|[Purchase_Order_Line_Id](#purchase_order_line_id)|`uniqueidentifier` `PK`||
|[Line_No](#line_no)|`int` ||
|[Product_Id](#product_id)|`uniqueidentifier` ||
|[Product_Description](#product_description)|`nvarchar` `ML`||
|[Lot_Id](#lot_id)|`uniqueidentifier` |When not null, indicates that a specific lot is required to be delivered.|
|[Quantity](#quantity)|`decimal(0, 0)` ||
|[Received_Quantity](#received_quantity)|`decimal(0, 0)` ||
|[Not_Received_Quantity](#not_received_quantity)|`decimal(0, 0)` ||
|[Quantity_Base](#quantity_base)|`decimal(0, 0)` Readonly||
|[Standard_Quantity_Base](#standard_quantity_base)|`decimal(0, 0)` Readonly|The theoretical quantity in base measurement unit according to the current measurement dimensions of the product. Used to measure the execution. NULL means to take the value from Quantity Base.|
|[Quantity_Unit_Id](#quantity_unit_id)|`uniqueidentifier` ||
|[Price_Per_Unit](#price_per_unit)|`decimal(0, 0)` ||
|[Confirmed_Price_Per_Unit](#confirmed_price_per_unit)|`decimal(0, 0)` ||
|[Purchase_Product_Price_Id](#purchase_product_price_id)|`uniqueidentifier` ||
|[Product_Code_Id](#product_code_id)|`uniqueidentifier` ||
|[Purchase_Order_Line_Notes](#purchase_order_line_notes)|`nvarchar` ||
|[Purchase_Order_Line_Planned_Delivery_Date](#purchase_order_line_planned_delivery_date)|`datetime` ||
|[Requisition_Line_Id](#requisition_line_id)|`uniqueidentifier` ||
|[Finished](#finished)|`bit` ||
|[Serial_Number_Id](#serial_number_id)|`uniqueidentifier` ||
|[Quantity_AMU](#quantity_amu)|`decimal(0, 0)` ||
|[Received_Quantity_AMU](#received_quantity_amu)|`decimal(0, 0)` ||
|[Additional_Measurement_Unit_Id](#additional_measurement_unit_id)|`uniqueidentifier` ||

## Columns

### Id

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

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|

### Purchase_Order_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Supplier_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Store_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Planned_Release_Date

| Property | Value |
| - | - |
|Type|datetime|

### Planned_Delivery_Date

| Property | Value |
| - | - |
|Type|datetime|

### Document_Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar|

### Payment_Due_Date

| Property | Value |
| - | - |
|Type|datetime|

### Invoice_Document_No

| Property | Value |
| - | - |
|Type|nvarchar|

### Purchase_Price_List_Id

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

### Purchase_Order_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Line_No

| Property | Value |
| - | - |
|Type|int|

### Product_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Description

| Property | Value |
| - | - |
|Type|nvarchar|

### Lot_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Quantity

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Received_Quantity

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Not_Received_Quantity

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Standard_Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Quantity_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Price_Per_Unit

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Confirmed_Price_Per_Unit

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Purchase_Product_Price_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Code_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Purchase_Order_Line_Notes

| Property | Value |
| - | - |
|Type|nvarchar|

### Purchase_Order_Line_Planned_Delivery_Date

| Property | Value |
| - | - |
|Type|datetime|

### Requisition_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Finished

| Property | Value |
| - | - |
|Type|bit|

### Serial_Number_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Quantity_AMU

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Received_Quantity_AMU

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Additional_Measurement_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|


