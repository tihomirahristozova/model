# Query Prd_Output_Order_Consumption_Lines_Table_Load_Navigator


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
|[Row_Version](#row_version)|`timestamp` ||
|[Line_No](#line_no)|`int` ||
|[Output_Order_Consumption_Line_Id](#output_order_consumption_line_id)|`uniqueidentifier` `PK`||
|[Output_Order_Id](#output_order_id)|`uniqueidentifier` ||
|[Work_Order_Id](#work_order_id)|`uniqueidentifier` ||
|[Work_Order_Item_Id](#work_order_item_id)|`uniqueidentifier` ||
|[Work_Order_Item_Operation_Id](#work_order_item_operation_id)|`uniqueidentifier` ||
|[Operation_Description](#operation_description)|`nvarchar` ||
|[Material_Id](#material_id)|`uniqueidentifier` ||
|[Material_Type](#material_type)|`uniqueidentifier` ||
|[Material_Group](#material_group)|`uniqueidentifier` |The product group, under which the product is categorized.|
|[Material_Name](#material_name)|`nvarchar` `ML`||
|[Production_Id](#production_id)|`uniqueidentifier` ||
|[Production_Name](#production_name)|`nvarchar` `ML`||
|[Consumed_Quantity_For_Setup](#consumed_quantity_for_setup)|`decimal(0, 0)` ||
|[Consumed_Quantity_For_Run](#consumed_quantity_for_run)|`decimal(0, 0)` ||
|[Consumed_Quantity_For_Scrap](#consumed_quantity_for_scrap)|`decimal(0, 0)` ||
|[Quantity_Unit_Id](#quantity_unit_id)|`uniqueidentifier` ||
|[Scrap_Type_Id](#scrap_type_id)|`uniqueidentifier` ||
|[Notes](#notes)|`nvarchar` ||
|[Material_Standard_Cost_Per_Lot](#material_standard_cost_per_lot)|`decimal(0, 0)` ||
|[Material_Standard_Price_Per_Lot](#material_standard_price_per_lot)|`decimal(0, 0)` ||
|[Consumed_Quantity_For_Setup_AMU](#consumed_quantity_for_setup_amu)|`decimal(0, 0)` ||
|[Consumed_Quantity_For_Run_AMU](#consumed_quantity_for_run_amu)|`decimal(0, 0)` ||
|[Consumed_Quantity_For_Scrap_AMU](#consumed_quantity_for_scrap_amu)|`decimal(0, 0)` ||
|[Additional_Measurement_Unit_Id](#additional_measurement_unit_id)|`uniqueidentifier` ||
|[Material_Group_L1_Name](#material_group_l1_name)|`nvarchar` `ML`||
|[Material_Group_L2_Name](#material_group_l2_name)|`nvarchar` `ML`||
|[Material_Group_L3_Name](#material_group_l3_name)|`nvarchar` `ML`||
|[Material_Group_L4_Name](#material_group_l4_name)|`nvarchar` `ML`||
|[Material_Group_L5_Name](#material_group_l5_name)|`nvarchar` `ML`||
|[Material_Group_L6_Name](#material_group_l6_name)|`nvarchar` `ML`||

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

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|

### Line_No

| Property | Value |
| - | - |
|Type|int|

### Output_Order_Consumption_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Output_Order_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Work_Order_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Work_Order_Item_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Work_Order_Item_Operation_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Operation_Description

| Property | Value |
| - | - |
|Type|nvarchar|

### Material_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Material_Type

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Material_Group

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Material_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Production_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Production_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Consumed_Quantity_For_Setup

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Consumed_Quantity_For_Run

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Consumed_Quantity_For_Scrap

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Quantity_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Scrap_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar|

### Material_Standard_Cost_Per_Lot

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Material_Standard_Price_Per_Lot

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Consumed_Quantity_For_Setup_AMU

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Consumed_Quantity_For_Run_AMU

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Consumed_Quantity_For_Scrap_AMU

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Additional_Measurement_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Material_Group_L1_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Material_Group_L2_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Material_Group_L3_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Material_Group_L4_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Material_Group_L5_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Material_Group_L6_Name

| Property | Value |
| - | - |
|Type|nvarchar|


