# Query Inv_Store_Order_Lines_Not_Executed_Table_Load_Navigator


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
|[Store_Order_Id](#store_order_id)|`uniqueidentifier` `PK`||
|[Store_Id](#store_id)|`uniqueidentifier` ||
|[Due_Date](#due_date)|`datetime` ||
|[Movement_Type](#movement_type)|`nvarchar` Allowed: `I`, `R`||
|[Planned_Release_Date](#planned_release_date)|`datetime` ||
|[Planned_Completion_Date](#planned_completion_date)|`datetime` ||
|[Driver_Name](#driver_name)|`nvarchar` ||
|[Temp_Transport_Company_Name](#temp_transport_company_name)|`nvarchar` ||
|[Vehicle_Reg_Number](#vehicle_reg_number)|`nvarchar` ||
|[Ordering_Person_Id](#ordering_person_id)|`uniqueidentifier` ||
|[Issued_By_Party_Id](#issued_by_party_id)|`uniqueidentifier` ||
|[Received_By_Party_Id](#received_by_party_id)|`uniqueidentifier` ||
|[Document_Currency_Id](#document_currency_id)|`uniqueidentifier` ||
|[Store_Order_Line_Id](#store_order_line_id)|`uniqueidentifier` `PK`||
|[Parent_Line_Id](#parent_line_id)|`uniqueidentifier` |Id of the line of the parent document, which generated the store order. NULL for user-entered store orders or if not applicable|
|[Line_No](#line_no)|`int` ||
|[Product_Id](#product_id)|`uniqueidentifier` ||
|[Product_Name](#product_name)|`nvarchar` `ML`||
|[Product_Group_Id](#product_group_id)|`uniqueidentifier` ||
|[Product_Variant_Id](#product_variant_id)|`uniqueidentifier` |If specified determines which product variant of the current product in this line is used.|
|[Store_Bin_Id](#store_bin_id)|`uniqueidentifier` ||
|[Serial_Number_Id](#serial_number_id)|`uniqueidentifier` ||
|[Quantity](#quantity)|`decimal(0, 0)` ||
|[Executed_Quantity](#executed_quantity)|`decimal(0, 0)` ||
|[Not_Executed_Quantity](#not_executed_quantity)|`decimal(0, 0)` ||
|[Quantity_Unit_Id](#quantity_unit_id)|`uniqueidentifier` ||
|[Quantity_Base](#quantity_base)|`decimal(0, 0)` Readonly||
|[Not_Executed_Quantity_Base](#not_executed_quantity_base)|`decimal(0, 0)` ||
|[Unit_Cost](#unit_cost)|`decimal(0, 0)` ||
|[Line_Cost](#line_cost)|`decimal(0, 0)` ||
|[Executed_Line_Cost](#executed_line_cost)|`decimal(0, 0)` ||
|[Not_Executed_Line_Cost](#not_executed_line_cost)|`decimal(0, 0)` ||
|[Lot_Number](#lot_number)|`nvarchar` ||
|[Lot_Id](#lot_id)|`uniqueidentifier` ||
|[Purchase_Lot_Number](#purchase_lot_number)|`nvarchar` ||
|[Guarantee_Period_Days](#guarantee_period_days)|`int` ||
|[Sales_Order_Line_Id](#sales_order_line_id)|`uniqueidentifier` ||
|[Transaction_Timestamp](#transaction_timestamp)|`datetime` Readonly||
|[Line_Notes](#line_notes)|`nvarchar` ||
|[Customer_Purchase_Order_No](#customer_purchase_order_no)|`nvarchar` ||
|[Measurement_Units_Id](#measurement_units_id)|`uniqueidentifier` `PK`||
|[Ordered_Standard_Quantity_Base](#ordered_standard_quantity_base)|`decimal(0, 0)` ||
|[Executed_Standard_Quantity_Base](#executed_standard_quantity_base)|`decimal(0, 0)` ||
|[Standard_Quantity_Base](#standard_quantity_base)|`decimal(0, 0)` Readonly|The theoretical quantity in base measurement unit according to the current measurement dimensions of the product. Used to measure the execution. NULL means to take the value from Quantity Base.|
|[Ordered_Quantity](#ordered_quantity)|`decimal(0, 0)` ||
|[Quantity_AMU](#quantity_amu)|`decimal(0, 0)` ||
|[Executed_Quantity_AMU](#executed_quantity_amu)|`decimal(0, 0)` ||
|[Not_Executed_Quantity_AMU](#not_executed_quantity_amu)|`decimal(0, 0)` ||
|[Additional_Measurement_Unit_Id](#additional_measurement_unit_id)|`uniqueidentifier` ||
|[Product_Group_Id_L1_Name](#product_group_id_l1_name)|`nvarchar` `ML`||
|[Product_Group_Id_L2_Name](#product_group_id_l2_name)|`nvarchar` `ML`||
|[Product_Group_Id_L3_Name](#product_group_id_l3_name)|`nvarchar` `ML`||
|[Product_Group_Id_L4_Name](#product_group_id_l4_name)|`nvarchar` `ML`||
|[Product_Group_Id_L5_Name](#product_group_id_l5_name)|`nvarchar` `ML`||
|[Product_Group_Id_L6_Name](#product_group_id_l6_name)|`nvarchar` `ML`||
|[SaleOrder](#saleorder)|`uniqueidentifier` ||
|[Available_Quantity_Base](#available_quantity_base)|`decimal(0, 0)` ||

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

### Store_Order_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Store_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Due_Date

| Property | Value |
| - | - |
|Type|datetime|

### Movement_Type

| Property | Value |
| - | - |
|Type|nvarchar|

### Planned_Release_Date

| Property | Value |
| - | - |
|Type|datetime|

### Planned_Completion_Date

| Property | Value |
| - | - |
|Type|datetime|

### Driver_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Temp_Transport_Company_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Vehicle_Reg_Number

| Property | Value |
| - | - |
|Type|nvarchar|

### Ordering_Person_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Issued_By_Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Received_By_Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Store_Order_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Parent_Line_Id

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

### Product_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Product_Group_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Variant_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Store_Bin_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Serial_Number_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Quantity

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Executed_Quantity

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Not_Executed_Quantity

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Quantity_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Not_Executed_Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Unit_Cost

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Line_Cost

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Executed_Line_Cost

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Not_Executed_Line_Cost

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Lot_Number

| Property | Value |
| - | - |
|Type|nvarchar|

### Lot_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Purchase_Lot_Number

| Property | Value |
| - | - |
|Type|nvarchar|

### Guarantee_Period_Days

| Property | Value |
| - | - |
|Type|int|

### Sales_Order_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Transaction_Timestamp

| Property | Value |
| - | - |
|Type|datetime|

### Line_Notes

| Property | Value |
| - | - |
|Type|nvarchar|

### Customer_Purchase_Order_No

| Property | Value |
| - | - |
|Type|nvarchar|

### Measurement_Units_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Ordered_Standard_Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Executed_Standard_Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Standard_Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Ordered_Quantity

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Quantity_AMU

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Executed_Quantity_AMU

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Not_Executed_Quantity_AMU

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Additional_Measurement_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Group_Id_L1_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Product_Group_Id_L2_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Product_Group_Id_L3_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Product_Group_Id_L4_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Product_Group_Id_L5_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Product_Group_Id_L6_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### SaleOrder

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Available_Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(0, 0)|


