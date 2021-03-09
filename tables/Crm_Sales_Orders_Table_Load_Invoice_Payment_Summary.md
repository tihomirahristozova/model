# Query Crm_Sales_Orders_Table_Load_Invoice_Payment_Summary


## Summary

| Name | Type | Description |
| - | - | --- |
|[From_Party_Id](#from_party_id)|`uniqueidentifier` ||
|[Document_Type_Id](#document_type_id)|`uniqueidentifier` ||
|[Document_No](#document_no)|`nvarchar` ||
|[Document_Date](#document_date)|`date` ||
|[State](#state)|`smallint` Allowed: `0`, `5`, `10`, `20`, `30`, `40`, `50`, Readonly||
|[To_Party_Id](#to_party_id)|`uniqueidentifier` ||
|[Read_Only](#read_only)|`bit` Readonly||
|[Void](#void)|`bit` Readonly||
|[Master_Document_Id](#master_document_id)|`uniqueidentifier` ||
|[Parent_Document_Id](#parent_document_id)|`uniqueidentifier` ||
|[Adjusted_Document_Id](#adjusted_document_id)|`uniqueidentifier` ||
|[Adjustment_Number](#adjustment_number)|`int` ||
|[Creation_Time](#creation_time)|`datetime` Readonly||
|[Creation_User](#creation_user)|`nvarchar` Readonly||
|[Void_Time](#void_time)|`datetime` Readonly||
|[Void_User](#void_user)|`nvarchar` Readonly||
|[Sales_Order_Id](#sales_order_id)|`uniqueidentifier` `PK`||
|[Customer_Id](#customer_id)|`uniqueidentifier` ||
|[Ship_To_Customer_Id](#ship_to_customer_id)|`uniqueidentifier` ||
|[Bill_To](#bill_to)|`nvarchar` Allowed: `C`, `L`||
|[Collections_Responsible_Employee_Id](#collections_responsible_employee_id)|`uniqueidentifier` ||
|[Store_Id](#store_id)|`uniqueidentifier` ||
|[Sales_Person_Id](#sales_person_id)|`uniqueidentifier` ||
|[Sales_Person_Group_Id](#sales_person_group_id)|`uniqueidentifier` `PK`||
|[Sales_Person_Group_Name](#sales_person_group_name)|`nvarchar` ||
|[Sales_Group_L1](#sales_group_l1)|`nvarchar` ||
|[Sales_Group_L2](#sales_group_l2)|`nvarchar` ||
|[Sales_Group_L3](#sales_group_l3)|`nvarchar` ||
|[Sales_Group_L4](#sales_group_l4)|`nvarchar` ||
|[Sales_Group_L5](#sales_group_l5)|`nvarchar` ||
|[Sales_Group_L6](#sales_group_l6)|`nvarchar` ||
|[Dealer_Id](#dealer_id)|`uniqueidentifier` ||
|[Price_List_Id](#price_list_id)|`uniqueidentifier` ||
|[Ship_To_Party_Contact_Mechanism_Id](#ship_to_party_contact_mechanism_id)|`uniqueidentifier` ||
|[Payment_Type_Id](#payment_type_id)|`uniqueidentifier` ||
|[Payment_Due_Date](#payment_due_date)|`datetime` ||
|[Document_Currency_Id](#document_currency_id)|`uniqueidentifier` ||
|[Document_Id](#document_id)|`uniqueidentifier` ||
|[Sales_Quantity](#sales_quantity)|`decimal(0, 0)` ||
|[Requested_Quantity](#requested_quantity)|`decimal(0, 0)` ||
|[Lines_Total](#lines_total)|`decimal(0, 0)` ||
|[Lines_Count](#lines_count)|`int` ||
|[Amount_To_Pay](#amount_to_pay)|`decimal(0, 0)` ||
|[Invoice_Quantity](#invoice_quantity)|`decimal(0, 0)` ||
|[Invoiced_Amount](#invoiced_amount)|`decimal(0, 0)` ||
|[Invoiced_Lines_Count](#invoiced_lines_count)|`int` ||
|[Invoice_Count](#invoice_count)|`int` ||
|[First_Invoice_Date](#first_invoice_date)|`datetime` ||
|[Last_Invoice_Date](#last_invoice_date)|`datetime` ||
|[Covered_Payment_Order_Amount](#covered_payment_order_amount)|`decimal(0, 0)` ||
|[Left_Payment_Order_Amount](#left_payment_order_amount)|`decimal(0, 0)` ||
|[Payment_Transaction_Count](#payment_transaction_count)|`int` ||
|[First_Payment_Transaction_Date](#first_payment_transaction_date)|`datetime` ||
|[Last_Payment_Transaction_Date](#last_payment_transaction_date)|`datetime` ||
|[Customer_Area_Id](#customer_area_id)|`uniqueidentifier` ||
|[Responsible_Person_Party_Id](#responsible_person_party_id)|`uniqueidentifier` ||
|[End_Customer_Party_Id](#end_customer_party_id)|`uniqueidentifier` |The end customer is the customer of the dealer. It is stored for information purposes only. The end customer may not have customer definition; any party can be used.|
|[User_Status_Id](#user_status_id)|`uniqueidentifier` ||
|[Customer_Type_Id](#customer_type_id)|`uniqueidentifier` ||
|[Customer_Area_Id_L1_Name](#customer_area_id_l1_name)|`nvarchar` `ML`||
|[Customer_Area_Id_L2_Name](#customer_area_id_l2_name)|`nvarchar` `ML`||
|[Customer_Area_Id_L3_Name](#customer_area_id_l3_name)|`nvarchar` `ML`||
|[Customer_Area_Id_L4_Name](#customer_area_id_l4_name)|`nvarchar` `ML`||
|[Customer_Area_Id_L5_Name](#customer_area_id_l5_name)|`nvarchar` `ML`||
|[Customer_Area_Id_L6_Name](#customer_area_id_l6_name)|`nvarchar` `ML`||

## Columns

### From_Party_Id

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

### State

| Property | Value |
| - | - |
|Type|smallint|

### To_Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Read_Only

| Property | Value |
| - | - |
|Type|bit|

### Void

| Property | Value |
| - | - |
|Type|bit|

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

### Sales_Order_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Customer_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Ship_To_Customer_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Bill_To

| Property | Value |
| - | - |
|Type|nvarchar|

### Collections_Responsible_Employee_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Store_Id

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

### Sales_Person_Group_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Sales_Group_L1

| Property | Value |
| - | - |
|Type|nvarchar|

### Sales_Group_L2

| Property | Value |
| - | - |
|Type|nvarchar|

### Sales_Group_L3

| Property | Value |
| - | - |
|Type|nvarchar|

### Sales_Group_L4

| Property | Value |
| - | - |
|Type|nvarchar|

### Sales_Group_L5

| Property | Value |
| - | - |
|Type|nvarchar|

### Sales_Group_L6

| Property | Value |
| - | - |
|Type|nvarchar|

### Dealer_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Price_List_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Ship_To_Party_Contact_Mechanism_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Payment_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Payment_Due_Date

| Property | Value |
| - | - |
|Type|datetime|

### Document_Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Sales_Quantity

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Requested_Quantity

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Lines_Total

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Lines_Count

| Property | Value |
| - | - |
|Type|int|

### Amount_To_Pay

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Invoice_Quantity

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Invoiced_Amount

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Invoiced_Lines_Count

| Property | Value |
| - | - |
|Type|int|

### Invoice_Count

| Property | Value |
| - | - |
|Type|int|

### First_Invoice_Date

| Property | Value |
| - | - |
|Type|datetime|

### Last_Invoice_Date

| Property | Value |
| - | - |
|Type|datetime|

### Covered_Payment_Order_Amount

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Left_Payment_Order_Amount

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Payment_Transaction_Count

| Property | Value |
| - | - |
|Type|int|

### First_Payment_Transaction_Date

| Property | Value |
| - | - |
|Type|datetime|

### Last_Payment_Transaction_Date

| Property | Value |
| - | - |
|Type|datetime|

### Customer_Area_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Responsible_Person_Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### End_Customer_Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### User_Status_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Customer_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Customer_Area_Id_L1_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Customer_Area_Id_L2_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Customer_Area_Id_L3_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Customer_Area_Id_L4_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Customer_Area_Id_L5_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Customer_Area_Id_L6_Name

| Property | Value |
| - | - |
|Type|nvarchar|


