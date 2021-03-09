# Query Crm_Bonus_Program_Products_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Bonus_Program_Id](#bonus_program_id)|`uniqueidentifier` `PK`||
|[Condition_Min_Quantity](#condition_min_quantity)|`decimal(0, 0)` ||
|[Condition_Max_Quantity](#condition_max_quantity)|`decimal(0, 0)` ||
|[Condition_Min_Amount](#condition_min_amount)|`decimal(0, 0)` ||
|[Condition_Max_Amount](#condition_max_amount)|`decimal(0, 0)` ||
|[Condition_Document_Currency_Id](#condition_document_currency_id)|`uniqueidentifier` ||
|[Condition_From_Date](#condition_from_date)|`datetime` ||
|[Condition_To_Date](#condition_to_date)|`datetime` ||
|[Condition_Target_Group_Id](#condition_target_group_id)|`uniqueidentifier` ||
|[Condition_Customer_Id](#condition_customer_id)|`uniqueidentifier` ||
|[Condition_Customer_Filter_XML](#condition_customer_filter_xml)|`nvarchar` ||
|[Condition_Ship_To_Customer_Id](#condition_ship_to_customer_id)|`uniqueidentifier` ||
|[Condition_Ship_To_Customer_Filter_XML](#condition_ship_to_customer_filter_xml)|`nvarchar` ||
|[Condition_Price_List_Id](#condition_price_list_id)|`uniqueidentifier` ||
|[Active](#active)|`bit` ||
|[Bonus_Action](#bonus_action)|`nvarchar` Allowed: `P`, `D`||
|[Bonus_Product_Id](#bonus_product_id)|`uniqueidentifier` ||
|[Bonus_Product_Quantity](#bonus_product_quantity)|`decimal(0, 0)` ||
|[Bonus_Product_Quantity_Unit_Id](#bonus_product_quantity_unit_id)|`uniqueidentifier` ||
|[Bonus_Product_Quantity_Multiplier_For_Each_Lot_Size](#bonus_product_quantity_multiplier_for_each_lot_size)|`decimal(0, 0)` ||
|[Bonus_Document_Amount_Type_Id](#bonus_document_amount_type_id)|`uniqueidentifier` ||
|[Bonus_Document_Amount_Percent](#bonus_document_amount_percent)|`decimal(0, 0)` ||
|[Bonus_Line_Discount_Percent](#bonus_line_discount_percent)|`decimal(0, 0)` ||
|[Bonus_Program_Name](#bonus_program_name)|`nvarchar` `ML`||
|[Condition_Distribution_Channel_Id](#condition_distribution_channel_id)|`uniqueidentifier` ||
|[Condition_Product_Group_Id](#condition_product_group_id)|`uniqueidentifier` |When not NULL, specifies that the bonus should be applied only to products from the specified product group or its subgroups|
|[Priority](#priority)|`tinyint` Allowed: `0`, `1`, `2`, `3`, `4`||
|[Product_Id](#product_id)|`uniqueidentifier` |The product which is required to exist in the final sales document in order for the bonus program to be applied|
|[Condition_Distribution_Channel_Filter_XML](#condition_distribution_channel_filter_xml)|`nvarchar` ||
|[Bonus_Product_Quantity_AMU](#bonus_product_quantity_amu)|`decimal(0, 0)` ||
|[Additional_Measurement_Unit_Id](#additional_measurement_unit_id)|`uniqueidentifier` ||
|[Condition_Product_Group_Id_L1_Name](#condition_product_group_id_l1_name)|`nvarchar` `ML`||
|[Condition_Product_Group_Id_L2_Name](#condition_product_group_id_l2_name)|`nvarchar` `ML`||
|[Condition_Product_Group_Id_L3_Name](#condition_product_group_id_l3_name)|`nvarchar` `ML`||
|[Condition_Product_Group_Id_L4_Name](#condition_product_group_id_l4_name)|`nvarchar` `ML`||
|[Condition_Product_Group_Id_L5_Name](#condition_product_group_id_l5_name)|`nvarchar` `ML`||
|[Condition_Product_Group_Id_L6_Name](#condition_product_group_id_l6_name)|`nvarchar` `ML`||

## Columns

### Bonus_Program_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Condition_Min_Quantity

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Condition_Max_Quantity

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Condition_Min_Amount

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Condition_Max_Amount

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Condition_Document_Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Condition_From_Date

| Property | Value |
| - | - |
|Type|datetime|

### Condition_To_Date

| Property | Value |
| - | - |
|Type|datetime|

### Condition_Target_Group_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Condition_Customer_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Condition_Customer_Filter_XML

| Property | Value |
| - | - |
|Type|nvarchar|

### Condition_Ship_To_Customer_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Condition_Ship_To_Customer_Filter_XML

| Property | Value |
| - | - |
|Type|nvarchar|

### Condition_Price_List_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Active

| Property | Value |
| - | - |
|Type|bit|

### Bonus_Action

| Property | Value |
| - | - |
|Type|nvarchar|

### Bonus_Product_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Bonus_Product_Quantity

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Bonus_Product_Quantity_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Bonus_Product_Quantity_Multiplier_For_Each_Lot_Size

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Bonus_Document_Amount_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Bonus_Document_Amount_Percent

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Bonus_Line_Discount_Percent

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Bonus_Program_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Condition_Distribution_Channel_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Condition_Product_Group_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Priority

| Property | Value |
| - | - |
|Type|tinyint|

### Product_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Condition_Distribution_Channel_Filter_XML

| Property | Value |
| - | - |
|Type|nvarchar|

### Bonus_Product_Quantity_AMU

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Additional_Measurement_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Condition_Product_Group_Id_L1_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Condition_Product_Group_Id_L2_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Condition_Product_Group_Id_L3_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Condition_Product_Group_Id_L4_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Condition_Product_Group_Id_L5_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Condition_Product_Group_Id_L6_Name

| Property | Value |
| - | - |
|Type|nvarchar|


