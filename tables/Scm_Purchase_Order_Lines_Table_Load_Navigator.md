# Query Scm_Purchase_Order_Lines_Table_Load_Navigator


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
|[Entity_Name](#entity_name)|`nvarchar` ||
|[Supplier_Id](#supplier_id)|`uniqueidentifier` ||
|[Store_Id](#store_id)|`uniqueidentifier` ||
|[Document_Currency_Id](#document_currency_id)|`uniqueidentifier` ||
|[Purchase_Order_Id](#purchase_order_id)|`uniqueidentifier` `PK`||
|[Planned_Release_Date](#planned_release_date)|`datetime` ||
|[Planned_Delivery_Date](#planned_delivery_date)|`datetime` ||
|[Payment_Due_Date](#payment_due_date)|`datetime` ||
|[Purchase_Price_List_Id](#purchase_price_list_id)|`uniqueidentifier` ||
|[Notes](#notes)|`nvarchar` ||
|[Purchase_Order_Line_Id](#purchase_order_line_id)|`uniqueidentifier` `PK`||
|[Line_No](#line_no)|`int` ||
|[Product_Id](#product_id)|`uniqueidentifier` ||
|[Product_Description](#product_description)|`nvarchar` `ML`||
|[Quantity](#quantity)|`decimal(0, 0)` ||
|[Quantity_Base](#quantity_base)|`decimal(0, 0)` Readonly||
|[Standard_Quantity_Base](#standard_quantity_base)|`decimal(0, 0)` Readonly|The theoretical quantity in base measurement unit according to the current measurement dimensions for the product. Used to measure the execution. NULL means to convert the value from Quantity using the measurement ratios.|
|[Confirmed_Quantity](#confirmed_quantity)|`decimal(0, 0)` ||
|[Confirmed_Quantity_Base](#confirmed_quantity_base)|`decimal(0, 0)` Readonly||
|[Confirmed_Standard_Quantity_Base](#confirmed_standard_quantity_base)|`decimal(0, 0)` Readonly|The theoretical quantity in base measurement unit according to the current measurement dimensions for the product. Used to measure the execution. NULL means to convert the value from Confirmed Quantity using the measurement ratios.|
|[Quantity_Unit_Id](#quantity_unit_id)|`uniqueidentifier` ||
|[Price_Per_Unit](#price_per_unit)|`decimal(0, 0)` ||
|[Confirmed_Price_Per_Unit](#confirmed_price_per_unit)|`decimal(0, 0)` ||
|[Planned_Delivery_Date_Lines](#planned_delivery_date_lines)|`datetime` ||
|[Purchase_Product_Price_Id](#purchase_product_price_id)|`uniqueidentifier` ||
|[Purchase_Order_Line_Notes](#purchase_order_line_notes)|`nvarchar` ||
|[Product_Code_Id](#product_code_id)|`uniqueidentifier` ||
|[Requisition_Line_Id](#requisition_line_id)|`uniqueidentifier` ||
|[Product_Variant_Id](#product_variant_id)|`uniqueidentifier` ||
|[Lot_Id](#lot_id)|`uniqueidentifier` |When not null, indicates that a specific lot is required to be delivered.|
|[Parent_Line_No](#parent_line_no)|`int` ||
|[Parent_Document_Id_Lines](#parent_document_id_lines)|`uniqueidentifier` ||
|[Part_Number](#part_number)|`nvarchar` ||
|[Product_Group_Id](#product_group_id)|`uniqueidentifier` ||
|[Product_Name](#product_name)|`nvarchar` `ML`||
|[Base_Measurement_Category_Id](#base_measurement_category_id)|`uniqueidentifier` ||
|[Measurement_Unit_Id](#measurement_unit_id)|`uniqueidentifier` ||
|[Product_Type_Id](#product_type_id)|`uniqueidentifier` ||
|[Is_Serialized](#is_serialized)|`bit` ||
|[Standard_Price_Per_Lot](#standard_price_per_lot)|`decimal(0, 0)` ||
|[Standard_Cost_Per_Lot](#standard_cost_per_lot)|`decimal(0, 0)` ||
|[Standard_Lot_Size_Base](#standard_lot_size_base)|`decimal(0, 0)` ||
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
|[Show_In_Catalog](#show_in_catalog)|`bit` ||
|[Minimal_Sales_Price_Per_Lot](#minimal_sales_price_per_lot)|`decimal(0, 0)` ||
|[Is_Featured](#is_featured)|`bit` ||
|[Minimal_Sales_Quantity_Base](#minimal_sales_quantity_base)|`decimal(0, 0)` ||
|[Short_Name](#short_name)|`nvarchar` `ML`||
|[Allow_Variable_Measurement_Ratios](#allow_variable_measurement_ratios)|`bit` ||
|[Cargo_Type_Id](#cargo_type_id)|`uniqueidentifier` ||
|[Quantity_AMU](#quantity_amu)|`decimal(0, 0)` ||
|[Confirmed_Quantity_AMU](#confirmed_quantity_amu)|`decimal(0, 0)` ||
|[Additional_Measurement_Unit_Id](#additional_measurement_unit_id)|`uniqueidentifier` ||
|[Product_Group_Id_L1_Name](#product_group_id_l1_name)|`nvarchar` `ML`||
|[Product_Group_Id_L2_Name](#product_group_id_l2_name)|`nvarchar` `ML`||
|[Product_Group_Id_L3_Name](#product_group_id_l3_name)|`nvarchar` `ML`||
|[Product_Group_Id_L4_Name](#product_group_id_l4_name)|`nvarchar` `ML`||
|[Product_Group_Id_L5_Name](#product_group_id_l5_name)|`nvarchar` `ML`||
|[Product_Group_Id_L6_Name](#product_group_id_l6_name)|`nvarchar` `ML`||
|[Line_Amount](#line_amount)|`decimal(0, 0)` ||
|[Line_Amount_In_Base_Currency](#line_amount_in_base_currency)|`decimal(0, 0)` ||

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

### Supplier_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Store_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Purchase_Order_Id

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

### Payment_Due_Date

| Property | Value |
| - | - |
|Type|datetime|

### Purchase_Price_List_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar|

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

### Quantity

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

### Confirmed_Quantity

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Confirmed_Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Confirmed_Standard_Quantity_Base

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

### Planned_Delivery_Date_Lines

| Property | Value |
| - | - |
|Type|datetime|

### Purchase_Product_Price_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Purchase_Order_Line_Notes

| Property | Value |
| - | - |
|Type|nvarchar|

### Product_Code_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Requisition_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Variant_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Lot_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Parent_Line_No

| Property | Value |
| - | - |
|Type|int|

### Parent_Document_Id_Lines

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Part_Number

| Property | Value |
| - | - |
|Type|nvarchar|

### Product_Group_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Name

| Property | Value |
| - | - |
|Type|nvarchar|

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

### Standard_Price_Per_Lot

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Standard_Cost_Per_Lot

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Standard_Lot_Size_Base

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

### Quantity_AMU

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Confirmed_Quantity_AMU

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

### Line_Amount

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Line_Amount_In_Base_Currency

| Property | Value |
| - | - |
|Type|decimal(0, 0)|


