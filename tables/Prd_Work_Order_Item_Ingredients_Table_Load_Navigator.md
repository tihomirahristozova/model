# Query Prd_Work_Order_Item_Ingredients_Table_Load_Navigator


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
|[Product_Id](#product_id)|`uniqueidentifier` ||
|[Product_Name](#product_name)|`nvarchar` `ML`||
|[Product_Group_Id](#product_group_id)|`uniqueidentifier` ||
|[Product_Group_Name](#product_group_name)|`nvarchar` `ML`||
|[Product_Group_Full_Path](#product_group_full_path)|`nvarchar` ||
|[Lot_Size](#lot_size)|`decimal(0, 0)` ||
|[Scheduled_Start_Date_Time](#scheduled_start_date_time)|`datetime` ||
|[Scheduled_End_Date_Time](#scheduled_end_date_time)|`datetime` ||
|[Item_Lot_Id](#item_lot_id)|`uniqueidentifier` ||
|[Serial_Number_Id](#serial_number_id)|`uniqueidentifier` ||
|[Id](#id)|`uniqueidentifier` `PK`||
|[Work_Order_Item_Id](#work_order_item_id)|`uniqueidentifier` ||
|[Line_Ord](#line_ord)|`int` ||
|[Material_Id](#material_id)|`uniqueidentifier` ||
|[Principal_Recipe_Ingredient_Id](#principal_recipe_ingredient_id)|`uniqueidentifier` ||
|[Ingredient_Name](#ingredient_name)|`nvarchar` `ML`||
|[Ingredient_Group_Id](#ingredient_group_id)|`uniqueidentifier` ||
|[Ingredient_Standard_Cost_Per_Lot](#ingredient_standard_cost_per_lot)|`decimal(0, 0)` ||
|[Ingredient_Standard_Price_Per_Lot](#ingredient_standard_price_per_lot)|`decimal(0, 0)` ||
|[Ingredient_Group_Name](#ingredient_group_name)|`nvarchar` `ML`||
|[Ingredient_Group_Full_Path](#ingredient_group_full_path)|`nvarchar` ||
|[Used_Quantity](#used_quantity)|`decimal(0, 0)` ||
|[Used_Quantity_Base](#used_quantity_base)|`decimal(0, 0)` Readonly||
|[Used_Quantity_Unit_Id](#used_quantity_unit_id)|`uniqueidentifier` ||
|[Used_Standard_Quantity_Base](#used_standard_quantity_base)|`decimal(0, 0)` Readonly|The theoretical quantity in base measurement unit according to the current measurement dimensions of the product. Used to measure the execution. NULL means to take the value from Used Quantity Base.|
|[Store_Id](#store_id)|`uniqueidentifier` ||
|[Work_Order_Item_Ingredients_Notes](#work_order_item_ingredients_notes)|`nvarchar` ||
|[Fixed_Scrap_Quantity](#fixed_scrap_quantity)|`decimal(0, 0)` ||
|[Operation_Id](#operation_id)|`uniqueidentifier` ||
|[Distribute_By](#distribute_by)|`nvarchar` Allowed: `SP`, `MC`, `SC`||
|[Distribute_By_Measurement_Category_Id](#distribute_by_measurement_category_id)|`uniqueidentifier` ||
|[Ingredient_Lot_Id](#ingredient_lot_id)|`uniqueidentifier` ||
|[Product_Code_Id](#product_code_id)|`uniqueidentifier` ||
|[Ingredient_Serial_Number_Id](#ingredient_serial_number_id)|`uniqueidentifier` ||
|[Used_Quantity_AMU](#used_quantity_amu)|`decimal(0, 0)` ||
|[Fixed_Scrap_Quantity_AMU](#fixed_scrap_quantity_amu)|`decimal(0, 0)` ||
|[Additional_Measurement_Unit_Id](#additional_measurement_unit_id)|`uniqueidentifier` ||
|[Product_Group_Id_L1_Name](#product_group_id_l1_name)|`nvarchar` `ML`||
|[Product_Group_Id_L2_Name](#product_group_id_l2_name)|`nvarchar` `ML`||
|[Product_Group_Id_L3_Name](#product_group_id_l3_name)|`nvarchar` `ML`||
|[Product_Group_Id_L4_Name](#product_group_id_l4_name)|`nvarchar` `ML`||
|[Product_Group_Id_L5_Name](#product_group_id_l5_name)|`nvarchar` `ML`||
|[Product_Group_Id_L6_Name](#product_group_id_l6_name)|`nvarchar` `ML`||
|[Ingredient_Group_Id_L1_Name](#ingredient_group_id_l1_name)|`nvarchar` `ML`||
|[Ingredient_Group_Id_L2_Name](#ingredient_group_id_l2_name)|`nvarchar` `ML`||
|[Ingredient_Group_Id_L3_Name](#ingredient_group_id_l3_name)|`nvarchar` `ML`||
|[Ingredient_Group_Id_L4_Name](#ingredient_group_id_l4_name)|`nvarchar` `ML`||
|[Ingredient_Group_Id_L5_Name](#ingredient_group_id_l5_name)|`nvarchar` `ML`||
|[Ingredient_Group_Id_L6_Name](#ingredient_group_id_l6_name)|`nvarchar` `ML`||

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

### Scheduled_Start_Date_Time

| Property | Value |
| - | - |
|Type|datetime|

### Scheduled_End_Date_Time

| Property | Value |
| - | - |
|Type|datetime|

### Item_Lot_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Serial_Number_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Work_Order_Item_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Line_Ord

| Property | Value |
| - | - |
|Type|int|

### Material_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Principal_Recipe_Ingredient_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Ingredient_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Ingredient_Group_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Ingredient_Standard_Cost_Per_Lot

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Ingredient_Standard_Price_Per_Lot

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Ingredient_Group_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Ingredient_Group_Full_Path

| Property | Value |
| - | - |
|Type|nvarchar|

### Used_Quantity

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Used_Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Used_Quantity_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Used_Standard_Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Store_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Work_Order_Item_Ingredients_Notes

| Property | Value |
| - | - |
|Type|nvarchar|

### Fixed_Scrap_Quantity

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Operation_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Distribute_By

| Property | Value |
| - | - |
|Type|nvarchar|

### Distribute_By_Measurement_Category_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Ingredient_Lot_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Code_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Ingredient_Serial_Number_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Used_Quantity_AMU

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Fixed_Scrap_Quantity_AMU

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

### Ingredient_Group_Id_L1_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Ingredient_Group_Id_L2_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Ingredient_Group_Id_L3_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Ingredient_Group_Id_L4_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Ingredient_Group_Id_L5_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Ingredient_Group_Id_L6_Name

| Property | Value |
| - | - |
|Type|nvarchar|


