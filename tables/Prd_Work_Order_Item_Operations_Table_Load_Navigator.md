# Query Prd_Work_Order_Item_Operations_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
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
|[Document_Id](#document_id)|`uniqueidentifier` ||
|[Work_Order_Id](#work_order_id)|`uniqueidentifier` `PK`||
|[Workgroup_Id](#workgroup_id)|`uniqueidentifier` ||
|[Workgroup_Name](#workgroup_name)|`nvarchar` ||
|[Workgroup_Full_Path](#workgroup_full_path)|`nvarchar` ||
|[Release_Date](#release_date)|`datetime` ||
|[Completion_Date](#completion_date)|`datetime` ||
|[Duration_Hour](#duration_hour)|`decimal(0, 0)` ||
|[Priority](#priority)|`smallint` Allowed: `1`, `2`, `3`, `4`, `5`||
|[Notes](#notes)|`nvarchar` ||
|[Produced_Quantity](#produced_quantity)|`decimal(0, 0)` ||
|[Line_Ord](#line_ord)|`int` ||
|[Product_Id](#product_id)|`uniqueidentifier` ||
|[Product_Name](#product_name)|`nvarchar` `ML`||
|[Product_Group_Id](#product_group_id)|`uniqueidentifier` ||
|[Product_Group_Name](#product_group_name)|`nvarchar` ||
|[Product_Group_Full_Path](#product_group_full_path)|`nvarchar` ||
|[Lot_Size](#lot_size)|`decimal(0, 0)` ||
|[Item_Scheduled_Start_Date_Time](#item_scheduled_start_date_time)|`datetime` ||
|[Item_Scheduled_End_Date_Time](#item_scheduled_end_date_time)|`datetime` ||
|[Id](#id)|`uniqueidentifier` `PK`||
|[Work_Order_Item_Id](#work_order_item_id)|`uniqueidentifier` ||
|[Operation_Id](#operation_id)|`uniqueidentifier` ||
|[Operation_Description](#operation_description)|`nvarchar` ||
|[Workgroup_Resource_Id](#workgroup_resource_id)|`uniqueidentifier` ||
|[Use_Quantity](#use_quantity)|`decimal(0, 0)` ||
|[Operation_Scheduled_Start_Date_Time](#operation_scheduled_start_date_time)|`datetime` ||
|[Operation_Scheduled_End_Date_Time](#operation_scheduled_end_date_time)|`datetime` ||
|[Minimum_Concurrent_Start_Time_Minutes](#minimum_concurrent_start_time_minutes)|`int` ||
|[Setup_Time_Minutes](#setup_time_minutes)|`int` ||
|[Run_Time_Minutes](#run_time_minutes)|`int` ||
|[Wait_Time_Minutes](#wait_time_minutes)|`int` ||
|[Move_Time_Minutes](#move_time_minutes)|`int` ||
|[Scrap_Rate](#scrap_rate)|`decimal(0, 0)` ||
|[Actual_Start_Date_Time](#actual_start_date_time)|`datetime` ||
|[Actual_End_Date_Time](#actual_end_date_time)|`datetime` ||
|[Tooling](#tooling)|`nvarchar` ||
|[Work_Item_Operation_Notes](#work_item_operation_notes)|`nvarchar` ||
|[Operation_Name](#operation_name)|`nvarchar` ||
|[Product_Group_Id_L1_Name](#product_group_id_l1_name)|`nvarchar` `ML`||
|[Product_Group_Id_L2_Name](#product_group_id_l2_name)|`nvarchar` `ML`||
|[Product_Group_Id_L3_Name](#product_group_id_l3_name)|`nvarchar` `ML`||
|[Product_Group_Id_L4_Name](#product_group_id_l4_name)|`nvarchar` `ML`||
|[Product_Group_Id_L5_Name](#product_group_id_l5_name)|`nvarchar` `ML`||
|[Product_Group_Id_L6_Name](#product_group_id_l6_name)|`nvarchar` `ML`||

## Columns

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

### Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Work_Order_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Workgroup_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Workgroup_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Workgroup_Full_Path

| Property | Value |
| - | - |
|Type|nvarchar|

### Release_Date

| Property | Value |
| - | - |
|Type|datetime|

### Completion_Date

| Property | Value |
| - | - |
|Type|datetime|

### Duration_Hour

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Priority

| Property | Value |
| - | - |
|Type|smallint|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar|

### Produced_Quantity

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Line_Ord

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

### Product_Group_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Product_Group_Full_Path

| Property | Value |
| - | - |
|Type|nvarchar|

### Lot_Size

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Item_Scheduled_Start_Date_Time

| Property | Value |
| - | - |
|Type|datetime|

### Item_Scheduled_End_Date_Time

| Property | Value |
| - | - |
|Type|datetime|

### Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Work_Order_Item_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Operation_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Operation_Description

| Property | Value |
| - | - |
|Type|nvarchar|

### Workgroup_Resource_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Use_Quantity

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Operation_Scheduled_Start_Date_Time

| Property | Value |
| - | - |
|Type|datetime|

### Operation_Scheduled_End_Date_Time

| Property | Value |
| - | - |
|Type|datetime|

### Minimum_Concurrent_Start_Time_Minutes

| Property | Value |
| - | - |
|Type|int|

### Setup_Time_Minutes

| Property | Value |
| - | - |
|Type|int|

### Run_Time_Minutes

| Property | Value |
| - | - |
|Type|int|

### Wait_Time_Minutes

| Property | Value |
| - | - |
|Type|int|

### Move_Time_Minutes

| Property | Value |
| - | - |
|Type|int|

### Scrap_Rate

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Actual_Start_Date_Time

| Property | Value |
| - | - |
|Type|datetime|

### Actual_End_Date_Time

| Property | Value |
| - | - |
|Type|datetime|

### Tooling

| Property | Value |
| - | - |
|Type|nvarchar|

### Work_Item_Operation_Notes

| Property | Value |
| - | - |
|Type|nvarchar|

### Operation_Name

| Property | Value |
| - | - |
|Type|nvarchar|

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


