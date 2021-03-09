# Query Inv_Movements_Chronology_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[From_Party_Id](#from_party_id)|`uniqueidentifier` ||
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` ||
|[Enterprise_Company_Location_Id](#enterprise_company_location_id)|`uniqueidentifier` ||
|[Document_Type_Id](#document_type_id)|`uniqueidentifier` ||
|[Document_No](#document_no)|`nvarchar` ||
|[Document_Date](#document_date)|`date` ||
|[State](#state)|`smallint` Allowed: `0`, `5`, `10`, `20`, `30`, `40`, `50`, Readonly||
|[To_Party_Id](#to_party_id)|`uniqueidentifier` ||
|[Read_Only](#read_only)|`bit` Readonly||
|[Notes](#notes)|`nvarchar` ||
|[Void](#void)|`bit` Readonly||
|[Master_Document_Id](#master_document_id)|`uniqueidentifier` ||
|[Parent_Document_Id](#parent_document_id)|`uniqueidentifier` ||
|[Adjusted_Document_Id](#adjusted_document_id)|`uniqueidentifier` ||
|[Adjustment_Number](#adjustment_number)|`int` Readonly||
|[Creation_Time](#creation_time)|`datetime` Readonly||
|[Creation_User](#creation_user)|`nvarchar` Readonly||
|[Void_Time](#void_time)|`datetime` Readonly||
|[Void_User](#void_user)|`nvarchar` Readonly||
|[Base_Currency_Id](#base_currency_id)|`uniqueidentifier` ||
|[Transaction_Id](#transaction_id)|`uniqueidentifier` `PK`||
|[Document_Id](#document_id)|`uniqueidentifier` ||
|[Store_Id](#store_id)|`uniqueidentifier` ||
|[Movement_Type](#movement_type)|`nvarchar` Allowed: `I`, `R`||
|[Cost_Source](#cost_source)|`nvarchar` Allowed: `S`, `D`, Readonly||
|[Document_Currency_Id](#document_currency_id)|`uniqueidentifier` ||
|[Store_Currency_Id](#store_currency_id)|`uniqueidentifier` ||
|[Transaction_Line_Id](#transaction_line_id)|`uniqueidentifier` `PK`||
|[Line_No](#line_no)|`int` ||
|[Product_Id](#product_id)|`uniqueidentifier` ||
|[Product_Name](#product_name)|`nvarchar` `ML`||
|[Product_Part_Number](#product_part_number)|`nvarchar` ||
|[Costing_Currency_Id](#costing_currency_id)|`uniqueidentifier` ||
|[Product_Group_Id](#product_group_id)|`uniqueidentifier` |The product group, under which the product is categorized.|
|[ABC_Class](#abc_class)|`nvarchar` Allowed: `A `, `B `, `C `|Product importance classification, where A are the most important and C - the least important products. Usually used as user filtering condition when previewing results of the procurement planning process.|
|[Description](#description)|`nvarchar` `ML`|The description of the product|
|[Original_Product_Id](#original_product_id)|`uniqueidentifier` ||
|[Lot_Id](#lot_id)|`uniqueidentifier` ||
|[Store_Bin_Id](#store_bin_id)|`uniqueidentifier` ||
|[Serial_Number_Id](#serial_number_id)|`uniqueidentifier` ||
|[Product_Variant_Id](#product_variant_id)|`uniqueidentifier` |If specified determines which product variant of the current product in this line is used.|
|[Base_Measurement_Unit_Id](#base_measurement_unit_id)|`uniqueidentifier` ||
|[Finished](#finished)|`bit` ||
|[Guarantee_Period_Days](#guarantee_period_days)|`int` ||
|[Product_Code_Id](#product_code_id)|`uniqueidentifier` ||
|[Transaction_Lines_Notes](#transaction_lines_notes)|`nvarchar` ||
|[Transaction_Timestamp](#transaction_timestamp)|`datetime` ||
|[Parent_Store_Order_Line_Id](#parent_store_order_line_id)|`uniqueidentifier` ||
|[Type](#type)|`nvarchar` Allowed: `MV`, `SV`||
|[Start_Quantity_Base](#start_quantity_base)|`decimal(0, 0)` ||
|[Receipt_Quantity_Base](#receipt_quantity_base)|`decimal(0, 0)` ||
|[Issue_Quantity_Base](#issue_quantity_base)|`decimal(0, 0)` ||
|[End_Quantity_Base](#end_quantity_base)|`decimal(0, 0)` ||
|[Start_Product_Cost](#start_product_cost)|`decimal(0, 0)` ||
|[Receipt_Product_Cost](#receipt_product_cost)|`decimal(0, 0)` ||
|[Issue_Product_Cost](#issue_product_cost)|`decimal(0, 0)` ||
|[End_Product_Cost](#end_product_cost)|`decimal(0, 0)` ||
|[Start_Store_Cost](#start_store_cost)|`decimal(0, 0)` ||
|[Receipt_Store_Cost](#receipt_store_cost)|`decimal(0, 0)` ||
|[Issue_Store_Cost](#issue_store_cost)|`decimal(0, 0)` ||
|[End_Store_Cost](#end_store_cost)|`decimal(0, 0)` ||
|[Start_Base_Cost](#start_base_cost)|`decimal(0, 0)` ||
|[Receipt_Base_Cost](#receipt_base_cost)|`decimal(0, 0)` ||
|[Issue_Base_Cost](#issue_base_cost)|`decimal(0, 0)` ||
|[End_Base_Cost](#end_base_cost)|`decimal(0, 0)` ||
|[Start_Adjusted_Product_Cost](#start_adjusted_product_cost)|`decimal(0, 0)` ||
|[Receipt_Adjusted_Product_Cost](#receipt_adjusted_product_cost)|`decimal(0, 0)` ||
|[Issue_Adjusted_Product_Cost](#issue_adjusted_product_cost)|`decimal(0, 0)` ||
|[End_Adjusted_Product_Cost](#end_adjusted_product_cost)|`decimal(0, 0)` ||
|[Start_Adjusted_Store_Cost](#start_adjusted_store_cost)|`decimal(0, 0)` ||
|[Receipt_Adjusted_Store_Cost](#receipt_adjusted_store_cost)|`decimal(0, 0)` ||
|[Issue_Adjusted_Store_Cost](#issue_adjusted_store_cost)|`decimal(0, 0)` ||
|[End_Adjusted_Store_Cost](#end_adjusted_store_cost)|`decimal(0, 0)` ||
|[Start_Adjusted_Base_Cost](#start_adjusted_base_cost)|`decimal(0, 0)` ||
|[Receipt_Adjusted_Base_Cost](#receipt_adjusted_base_cost)|`decimal(0, 0)` ||
|[Issue_Adjusted_Base_Cost](#issue_adjusted_base_cost)|`decimal(0, 0)` ||
|[End_Adjusted_Base_Cost](#end_adjusted_base_cost)|`decimal(0, 0)` ||
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

### Enterprise_Company_Location_Id

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

### Notes

| Property | Value |
| - | - |
|Type|nvarchar|

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

### Base_Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Transaction_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Store_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Movement_Type

| Property | Value |
| - | - |
|Type|nvarchar|

### Cost_Source

| Property | Value |
| - | - |
|Type|nvarchar|

### Document_Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Store_Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Transaction_Line_Id

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

### Product_Part_Number

| Property | Value |
| - | - |
|Type|nvarchar|

### Costing_Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Group_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### ABC_Class

| Property | Value |
| - | - |
|Type|nvarchar|

### Description

| Property | Value |
| - | - |
|Type|nvarchar|

### Original_Product_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Lot_Id

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

### Product_Variant_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Base_Measurement_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Finished

| Property | Value |
| - | - |
|Type|bit|

### Guarantee_Period_Days

| Property | Value |
| - | - |
|Type|int|

### Product_Code_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Transaction_Lines_Notes

| Property | Value |
| - | - |
|Type|nvarchar|

### Transaction_Timestamp

| Property | Value |
| - | - |
|Type|datetime|

### Parent_Store_Order_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Type

| Property | Value |
| - | - |
|Type|nvarchar|

### Start_Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Receipt_Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Issue_Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### End_Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Start_Product_Cost

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Receipt_Product_Cost

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Issue_Product_Cost

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### End_Product_Cost

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Start_Store_Cost

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Receipt_Store_Cost

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Issue_Store_Cost

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### End_Store_Cost

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Start_Base_Cost

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Receipt_Base_Cost

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Issue_Base_Cost

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### End_Base_Cost

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Start_Adjusted_Product_Cost

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Receipt_Adjusted_Product_Cost

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Issue_Adjusted_Product_Cost

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### End_Adjusted_Product_Cost

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Start_Adjusted_Store_Cost

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Receipt_Adjusted_Store_Cost

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Issue_Adjusted_Store_Cost

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### End_Adjusted_Store_Cost

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Start_Adjusted_Base_Cost

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Receipt_Adjusted_Base_Cost

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Issue_Adjusted_Base_Cost

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### End_Adjusted_Base_Cost

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

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


