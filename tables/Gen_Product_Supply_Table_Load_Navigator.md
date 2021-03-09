# Query Gen_Product_Supply_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Product_Supply_Id](#product_supply_id)|`uniqueidentifier` `PK`||
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` ||
|[Product_Id](#product_id)|`uniqueidentifier` ||
|[Product_Group_Id](#product_group_id)|`uniqueidentifier` ||
|[Supply_Schema_Id](#supply_schema_id)|`uniqueidentifier` ||
|[Procurement_Type](#procurement_type)|`nvarchar` Allowed: `B`, `M`, `T`||
|[Generate_Document_Type_Id](#generate_document_type_id)|`uniqueidentifier` ||
|[Standard_Cost_Per_Lot](#standard_cost_per_lot)|`decimal(0, 0)` ||
|[Planning_Lead_Time_Days](#planning_lead_time_days)|`int` ||
|[Planning_Time_Fence_Days](#planning_time_fence_days)|`int` ||
|[Planning_Safety_Stock_Quantity_Base](#planning_safety_stock_quantity_base)|`decimal(0, 0)` ||
|[Planning_Horizon_Days](#planning_horizon_days)|`int` ||
|[Planning_Maximum_Inventory_Quantity_Base](#planning_maximum_inventory_quantity_base)|`decimal(0, 0)` ||
|[Planning_Annual_Usage_Quantity_Base](#planning_annual_usage_quantity_base)|`decimal(0, 0)` ||
|[Planning_Annual_Carrying_Cost_Percent](#planning_annual_carrying_cost_percent)|`decimal(0, 0)` ||
|[Planning_Order_Cycle_Days](#planning_order_cycle_days)|`int` ||
|[Planning_Order_Cost_Base_Currency](#planning_order_cost_base_currency)|`decimal(0, 0)` ||
|[Order_Policy](#order_policy)|`nvarchar` Allowed: `MRP`, `OPS`, `OPT`, `PRS`||
|[Order_Point_Quantity_Base](#order_point_quantity_base)|`decimal(0, 0)` ||
|[Fixed_Order_Quantity_Base](#fixed_order_quantity_base)|`decimal(0, 0)` ||
|[Order_Minimum](#order_minimum)|`decimal(0, 0)` ||
|[Order_Maximum](#order_maximum)|`decimal(0, 0)` ||
|[Order_Lot_Sizing_Method](#order_lot_sizing_method)|`nvarchar` Allowed: `EOQ`, `FOQ`, `LFL`, `LFP`, `ROP`, `ROT`||
|[Order_Multiple](#order_multiple)|`bit` ||
|[Order_Lot_Size_Quantity_Base](#order_lot_size_quantity_base)|`decimal(0, 0)` ||
|[Order_Period_Start_Date](#order_period_start_date)|`datetime` ||
|[Order_Period_Planning_Days](#order_period_planning_days)|`int` ||
|[Manufacturing_Policy](#manufacturing_policy)|`nvarchar` Allowed: `ATO`, `MTO`, `MTS`, `ETO`||
|[Preferred_Supplier_Id](#preferred_supplier_id)|`uniqueidentifier` ||
|[Buyer_Name](#buyer_name)|`nvarchar` ||
|[Store_Id](#store_id)|`uniqueidentifier` ||
|[Default_Store_Bin_Id](#default_store_bin_id)|`uniqueidentifier` ||
|[From_Store_Id](#from_store_id)|`uniqueidentifier` ||
|[Is_Default](#is_default)|`bit` ||
|[Is_Active](#is_active)|`bit` ||
|[Product_Name](#product_name)|`nvarchar` `ML`||
|[Planning_Safety_Stock_Quantity_Base_AMU](#planning_safety_stock_quantity_base_amu)|`decimal(0, 0)` ||
|[Planning_Maximum_Inventory_Quantity_Base_AMU](#planning_maximum_inventory_quantity_base_amu)|`decimal(0, 0)` ||
|[Planning_Annual_Usage_Quantity_Base_AMU](#planning_annual_usage_quantity_base_amu)|`decimal(0, 0)` ||
|[Order_Point_Quantity_Base_AMU](#order_point_quantity_base_amu)|`decimal(0, 0)` ||
|[Fixed_Order_Quantity_Base_AMU](#fixed_order_quantity_base_amu)|`decimal(0, 0)` ||
|[Order_Minimum_AMU](#order_minimum_amu)|`decimal(0, 0)` ||
|[Order_Maximum_AMU](#order_maximum_amu)|`decimal(0, 0)` ||
|[Order_Lot_Size_Quantity_Base_AMU](#order_lot_size_quantity_base_amu)|`decimal(0, 0)` ||
|[Additional_Measurement_Unit_Id](#additional_measurement_unit_id)|`uniqueidentifier` ||
|[Product_Group_Id_L1_Name](#product_group_id_l1_name)|`nvarchar` `ML`||
|[Product_Group_Id_L2_Name](#product_group_id_l2_name)|`nvarchar` `ML`||
|[Product_Group_Id_L3_Name](#product_group_id_l3_name)|`nvarchar` `ML`||
|[Product_Group_Id_L4_Name](#product_group_id_l4_name)|`nvarchar` `ML`||
|[Product_Group_Id_L5_Name](#product_group_id_l5_name)|`nvarchar` `ML`||
|[Product_Group_Id_L6_Name](#product_group_id_l6_name)|`nvarchar` `ML`||

## Columns

### Product_Supply_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Group_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Supply_Schema_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Procurement_Type

| Property | Value |
| - | - |
|Type|nvarchar|

### Generate_Document_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Standard_Cost_Per_Lot

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Planning_Lead_Time_Days

| Property | Value |
| - | - |
|Type|int|

### Planning_Time_Fence_Days

| Property | Value |
| - | - |
|Type|int|

### Planning_Safety_Stock_Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Planning_Horizon_Days

| Property | Value |
| - | - |
|Type|int|

### Planning_Maximum_Inventory_Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Planning_Annual_Usage_Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Planning_Annual_Carrying_Cost_Percent

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Planning_Order_Cycle_Days

| Property | Value |
| - | - |
|Type|int|

### Planning_Order_Cost_Base_Currency

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Order_Policy

| Property | Value |
| - | - |
|Type|nvarchar|

### Order_Point_Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Fixed_Order_Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Order_Minimum

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Order_Maximum

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Order_Lot_Sizing_Method

| Property | Value |
| - | - |
|Type|nvarchar|

### Order_Multiple

| Property | Value |
| - | - |
|Type|bit|

### Order_Lot_Size_Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Order_Period_Start_Date

| Property | Value |
| - | - |
|Type|datetime|

### Order_Period_Planning_Days

| Property | Value |
| - | - |
|Type|int|

### Manufacturing_Policy

| Property | Value |
| - | - |
|Type|nvarchar|

### Preferred_Supplier_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Buyer_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Store_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Default_Store_Bin_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### From_Store_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Is_Default

| Property | Value |
| - | - |
|Type|bit|

### Is_Active

| Property | Value |
| - | - |
|Type|bit|

### Product_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Planning_Safety_Stock_Quantity_Base_AMU

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Planning_Maximum_Inventory_Quantity_Base_AMU

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Planning_Annual_Usage_Quantity_Base_AMU

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Order_Point_Quantity_Base_AMU

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Fixed_Order_Quantity_Base_AMU

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Order_Minimum_AMU

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Order_Maximum_AMU

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Order_Lot_Size_Quantity_Base_AMU

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


