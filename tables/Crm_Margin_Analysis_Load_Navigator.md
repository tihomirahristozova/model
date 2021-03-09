# Query Crm_Margin_Analysis_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` |When not NULL, specifies that the product is specific to a given enterprise company and may be used only in documents from this enterprise company.|
|[Enterprise_Company_Location_Id](#enterprise_company_location_id)|`uniqueidentifier` ||
|[Document_Type_Id](#document_type_id)|`uniqueidentifier` ||
|[Responsible_Person_Id](#responsible_person_id)|`uniqueidentifier` ||
|[Sales_Order_Currency_Directory_Id](#sales_order_currency_directory_id)|`uniqueidentifier` ||
|[Responsible_Person_Party_Id](#responsible_person_party_id)|`uniqueidentifier` ||
|[Document_No](#document_no)|`nvarchar` ||
|[Document_Date](#document_date)|`date` ||
|[Sales_Order_Id](#sales_order_id)|`uniqueidentifier` ||
|[Bonus_Program_Id](#bonus_program_id)|`uniqueidentifier` ||
|[Unit_Price](#unit_price)|`decimal(0, 0)` ||
|[Customer_Id](#customer_id)|`uniqueidentifier` ||
|[Ship_To_Customer_Id](#ship_to_customer_id)|`uniqueidentifier` ||
|[Sales_Order_Person_Id](#sales_order_person_id)|`uniqueidentifier` ||
|[Store_Id](#store_id)|`uniqueidentifier` ||
|[Sales_Order_Date](#sales_order_date)|`date` ||
|[Issue_Date](#issue_date)|`date` ||
|[Product_Id](#product_id)|`uniqueidentifier` ||
|[Product_Name](#product_name)|`nvarchar` `ML`||
|[Product_Part_Number](#product_part_number)|`nvarchar` ||
|[Customer_Sales_Person_Id](#customer_sales_person_id)|`uniqueidentifier` ||
|[Id](#id)|`uniqueidentifier` `PK`||
|[Product_Group_Id](#product_group_id)|`uniqueidentifier` ||
|[Base_Measurement_Category_Id](#base_measurement_category_id)|`uniqueidentifier` ||
|[Measurement_Unit_Id](#measurement_unit_id)|`uniqueidentifier` ||
|[Product_Type_Id](#product_type_id)|`uniqueidentifier` ||
|[Is_Serialized](#is_serialized)|`bit` ||
|[Standard_Cost_Per_Lot](#standard_cost_per_lot)|`decimal(0, 0)` ||
|[Planning_Demand_Time_Fence_Days](#planning_demand_time_fence_days)|`int` ||
|[Planning_Time_Fence_Days](#planning_time_fence_days)|`int` ||
|[Planning_Horizon_Days](#planning_horizon_days)|`int` ||
|[Flushing_Method](#flushing_method)|`nvarchar` Allowed: `B`, `F`, `M`||
|[Manufacturing_Policy](#manufacturing_policy)|`nvarchar` ||
|[ABC_Class](#abc_class)|`nvarchar` Allowed: `A `, `B `, `C `||
|[Supply_Schema_Id](#supply_schema_id)|`uniqueidentifier` ||
|[Scrap_Rate](#scrap_rate)|`decimal(0, 0)` ||
|[Description](#description)|`nvarchar` `ML`||
|[Costing_Method](#costing_method)|`nvarchar` Allowed: `AVG`, `EXP`, `BLD`||
|[Costing_Currency_Id](#costing_currency_id)|`uniqueidentifier` ||
|[Active](#active)|`bit` ||
|[Guarantee_Period_Days](#guarantee_period_days)|`int` ||
|[Creation_Time](#creation_time)|`datetime` Readonly||
|[Creation_User](#creation_user)|`nvarchar` Readonly||
|[Update_Time](#update_time)|`datetime` Readonly||
|[Update_User](#update_user)|`nvarchar` Readonly||
|[Purchase_Measurement_Unit_Id](#purchase_measurement_unit_id)|`uniqueidentifier` ||
|[Valuation_Group_Id](#valuation_group_id)|`uniqueidentifier` ||
|[Origin_Country_Id](#origin_country_id)|`uniqueidentifier` ||
|[Intrastat_Commodity_Code_Id](#intrastat_commodity_code_id)|`uniqueidentifier` ||
|[Intrastat_Supplementary_Unit_Id](#intrastat_supplementary_unit_id)|`uniqueidentifier` ||
|[Use_Lots](#use_lots)|`nvarchar` Allowed: `A`, `N`, `R`||
|[Lots_Issue](#lots_issue)|`nvarchar` Allowed: `FIFO`, `FEFO`, `LIFO`||
|[Expiry_Period_Days](#expiry_period_days)|`int` ||
|[Product_Enterprise_Company_Id](#product_enterprise_company_id)|`uniqueidentifier` ||
|[Show_In_Catalog](#show_in_catalog)|`bit` ||
|[Minimal_Sales_Price_Per_Lot](#minimal_sales_price_per_lot)|`decimal(0, 0)` ||
|[Is_Featured](#is_featured)|`bit` ||
|[Minimal_Sales_Quantity_Base](#minimal_sales_quantity_base)|`decimal(0, 0)` |Minimal base quantity of this product that has to be specified in any sale.|
|[Short_Name](#short_name)|`nvarchar` `ML`||
|[Allow_Variable_Measurement_Ratios](#allow_variable_measurement_ratios)|`bit` |Allow variable (dynamic) measurement ratios for each transaction. If specified, each store transaction could specify different measurement ratio between the used measurement unit and the base measurement unit.|
|[Cargo_Type_Id](#cargo_type_id)|`uniqueidentifier` |Specifies what type of cargo this product is. Required when generating transportation requisitions. NULL means unspecified.|
|[Standard_Price_Per_Lot](#standard_price_per_lot)|`decimal(0, 0)` ||
|[Standard_Lot_Size_Base](#standard_lot_size_base)|`decimal(0, 0)` ||
|[Product_Variant_Id](#product_variant_id)|`uniqueidentifier` ||
|[Lot_Id](#lot_id)|`uniqueidentifier` ||
|[Amount](#amount)|`decimal(0, 0)` ||
|[Standard_Price_Amount](#standard_price_amount)|`decimal(0, 0)` ||
|[Sales_Order_Currency_Id](#sales_order_currency_id)|`uniqueidentifier` ||
|[Quantity_Base](#quantity_base)|`decimal(0, 0)` ||
|[Document_Cost](#document_cost)|`decimal(0, 0)` ||
|[Transaction_Currency_Id](#transaction_currency_id)|`uniqueidentifier` ||
|[Product_Cost](#product_cost)|`decimal(0, 0)` ||
|[Product_Costing_Currency_Id](#product_costing_currency_id)|`uniqueidentifier` ||
|[Store_Cost](#store_cost)|`decimal(0, 0)` ||
|[Store_Currency_Id](#store_currency_id)|`uniqueidentifier` ||
|[Base_Cost](#base_cost)|`decimal(0, 0)` ||
|[Base_Currency_Id](#base_currency_id)|`uniqueidentifier` ||
|[Sales_Person_Group_Id](#sales_person_group_id)|`uniqueidentifier` ||
|[Sales_Person_Group_Name](#sales_person_group_name)|`nvarchar` ||
|[Customer_Area_Id](#customer_area_id)|`uniqueidentifier` ||
|[Customer_Type_Id](#customer_type_id)|`uniqueidentifier` ||
|[Party_Id](#party_id)|`uniqueidentifier` ||
|[Promotional_Package_Id](#promotional_package_id)|`uniqueidentifier` ||
|[From_Company_Division_Id](#from_company_division_id)|`uniqueidentifier` ||
|[To_Company_Division_Id](#to_company_division_id)|`uniqueidentifier` ||
|[Customer_Purchase_Order_No](#customer_purchase_order_no)|`nvarchar` ||
|[Quantity_Base_AMU](#quantity_base_amu)|`decimal(0, 0)` ||
|[Additional_Measurement_Unit_Id](#additional_measurement_unit_id)|`uniqueidentifier` ||
|[Customer_Area_Id_L1_Name](#customer_area_id_l1_name)|`nvarchar` `ML`||
|[Customer_Area_Id_L2_Name](#customer_area_id_l2_name)|`nvarchar` `ML`||
|[Customer_Area_Id_L3_Name](#customer_area_id_l3_name)|`nvarchar` `ML`||
|[Customer_Area_Id_L4_Name](#customer_area_id_l4_name)|`nvarchar` `ML`||
|[Customer_Area_Id_L5_Name](#customer_area_id_l5_name)|`nvarchar` `ML`||
|[Customer_Area_Id_L6_Name](#customer_area_id_l6_name)|`nvarchar` `ML`||
|[Sales_Person_Group_Id_L1_Name](#sales_person_group_id_l1_name)|`nvarchar` `ML`||
|[Sales_Person_Group_Id_L2_Name](#sales_person_group_id_l2_name)|`nvarchar` `ML`||
|[Sales_Person_Group_Id_L3_Name](#sales_person_group_id_l3_name)|`nvarchar` `ML`||
|[Sales_Person_Group_Id_L4_Name](#sales_person_group_id_l4_name)|`nvarchar` `ML`||
|[Sales_Person_Group_Id_L5_Name](#sales_person_group_id_l5_name)|`nvarchar` `ML`||
|[Sales_Person_Group_Id_L6_Name](#sales_person_group_id_l6_name)|`nvarchar` `ML`||
|[Product_Group_Id_L1_Name](#product_group_id_l1_name)|`nvarchar` `ML`||
|[Product_Group_Id_L2_Name](#product_group_id_l2_name)|`nvarchar` `ML`||
|[Product_Group_Id_L3_Name](#product_group_id_l3_name)|`nvarchar` `ML`||
|[Product_Group_Id_L4_Name](#product_group_id_l4_name)|`nvarchar` `ML`||
|[Product_Group_Id_L5_Name](#product_group_id_l5_name)|`nvarchar` `ML`||
|[Product_Group_Id_L6_Name](#product_group_id_l6_name)|`nvarchar` `ML`||
|[Amount_In_Base_Currency](#amount_in_base_currency)|`decimal(0, 0)` ||

## Columns

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

### Responsible_Person_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Sales_Order_Currency_Directory_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Responsible_Person_Party_Id

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

### Sales_Order_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Bonus_Program_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Unit_Price

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Customer_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Ship_To_Customer_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Sales_Order_Person_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Store_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Sales_Order_Date

| Property | Value |
| - | - |
|Type|date|

### Issue_Date

| Property | Value |
| - | - |
|Type|date|

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

### Customer_Sales_Person_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Group_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Base_Measurement_Category_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Measurement_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Is_Serialized

| Property | Value |
| - | - |
|Type|bit|

### Standard_Cost_Per_Lot

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Planning_Demand_Time_Fence_Days

| Property | Value |
| - | - |
|Type|int|

### Planning_Time_Fence_Days

| Property | Value |
| - | - |
|Type|int|

### Planning_Horizon_Days

| Property | Value |
| - | - |
|Type|int|

### Flushing_Method

| Property | Value |
| - | - |
|Type|nvarchar|

### Manufacturing_Policy

| Property | Value |
| - | - |
|Type|nvarchar|

### ABC_Class

| Property | Value |
| - | - |
|Type|nvarchar|

### Supply_Schema_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Scrap_Rate

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Description

| Property | Value |
| - | - |
|Type|nvarchar|

### Costing_Method

| Property | Value |
| - | - |
|Type|nvarchar|

### Costing_Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Active

| Property | Value |
| - | - |
|Type|bit|

### Guarantee_Period_Days

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

### Update_Time

| Property | Value |
| - | - |
|Type|datetime|

### Update_User

| Property | Value |
| - | - |
|Type|nvarchar|

### Purchase_Measurement_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Valuation_Group_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Origin_Country_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Intrastat_Commodity_Code_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Intrastat_Supplementary_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Use_Lots

| Property | Value |
| - | - |
|Type|nvarchar|

### Lots_Issue

| Property | Value |
| - | - |
|Type|nvarchar|

### Expiry_Period_Days

| Property | Value |
| - | - |
|Type|int|

### Product_Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Show_In_Catalog

| Property | Value |
| - | - |
|Type|bit|

### Minimal_Sales_Price_Per_Lot

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Is_Featured

| Property | Value |
| - | - |
|Type|bit|

### Minimal_Sales_Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Short_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Allow_Variable_Measurement_Ratios

| Property | Value |
| - | - |
|Type|bit|

### Cargo_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Standard_Price_Per_Lot

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Standard_Lot_Size_Base

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Product_Variant_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Lot_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Amount

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Standard_Price_Amount

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Sales_Order_Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Document_Cost

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Transaction_Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Cost

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Product_Costing_Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Store_Cost

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Store_Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Base_Cost

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Base_Currency_Id

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

### Customer_Area_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Customer_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Promotional_Package_Id

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

### Customer_Purchase_Order_No

| Property | Value |
| - | - |
|Type|nvarchar|

### Quantity_Base_AMU

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Additional_Measurement_Unit_Id

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

### Sales_Person_Group_Id_L1_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Sales_Person_Group_Id_L2_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Sales_Person_Group_Id_L3_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Sales_Person_Group_Id_L4_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Sales_Person_Group_Id_L5_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Sales_Person_Group_Id_L6_Name

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

### Amount_In_Base_Currency

| Property | Value |
| - | - |
|Type|decimal(0, 0)|


