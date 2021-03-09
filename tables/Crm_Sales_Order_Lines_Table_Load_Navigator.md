# Query Crm_Sales_Order_Lines_Table_Load_Navigator


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
|[Release_Time](#release_time)|`datetime` ||
|[Complete_Time](#complete_time)|`datetime` ||
|[Parent_Document_Relationship_Type](#parent_document_relationship_type)|`nvarchar` Allowed: `S`, `N`||
|[Reference_Document_No](#reference_document_no)|`nvarchar` ||
|[User_Status_Id](#user_status_id)|`uniqueidentifier` Readonly||
|[From_Company_Division_Id](#from_company_division_id)|`uniqueidentifier` ||
|[To_Company_Division_Id](#to_company_division_id)|`uniqueidentifier` ||
|[Entity_Name](#entity_name)|`nvarchar` |The entity name of the document header.|
|[Customer_Id](#customer_id)|`uniqueidentifier` ||
|[Ship_To_Customer_Id](#ship_to_customer_id)|`uniqueidentifier` ||
|[Document_Currency_Id](#document_currency_id)|`uniqueidentifier` ||
|[Credit_Limit_Override](#credit_limit_override)|`bit` ||
|[Store_Id](#store_id)|`uniqueidentifier` ||
|[Required_Delivery_Date](#required_delivery_date)|`date` ||
|[Payment_Due_Date](#payment_due_date)|`datetime` ||
|[Payment_Type_Id](#payment_type_id)|`uniqueidentifier` ||
|[Payment_Account_Id](#payment_account_id)|`uniqueidentifier` ||
|[Sales_Order_Id](#sales_order_id)|`uniqueidentifier` `PK`||
|[Ship_To_Party_Contact_Mechanism_Id](#ship_to_party_contact_mechanism_id)|`uniqueidentifier` ||
|[Price_List_Id](#price_list_id)|`uniqueidentifier` ||
|[Sales_Person_Id](#sales_person_id)|`uniqueidentifier` ||
|[Sales_Person_Group_Id](#sales_person_group_id)|`uniqueidentifier` ||
|[Sales_Person_Group_Name](#sales_person_group_name)|`nvarchar` ||
|[Deal_Type_Id](#deal_type_id)|`uniqueidentifier` ||
|[Dealer_Id](#dealer_id)|`uniqueidentifier` ||
|[Deal_Id](#deal_id)|`uniqueidentifier` ||
|[Notes_Sale_Order](#notes_sale_order)|`nvarchar` ||
|[Customer_Purchase_Order_No](#customer_purchase_order_no)|`nvarchar` ||
|[Return_For_Sales_Order_Id](#return_for_sales_order_id)|`uniqueidentifier` ||
|[Return_For_Invoice_Id](#return_for_invoice_id)|`uniqueidentifier` ||
|[Customer_Purchase_Order_Date](#customer_purchase_order_date)|`date` ||
|[End_Customer_Party_Id](#end_customer_party_id)|`uniqueidentifier` |The end customer is the customer of the dealer. It is stored for information purposes only. The end customer may not have customer definition; any party can be used.|
|[From_Date](#from_date)|`date` |When selling a service valid only for a period, denotes the beginning of the period. NULL means that it is unknown or N/A.|
|[To_Date](#to_date)|`date` |When selling a service valid only for a period, denotes the end of the period. NULL means that it is unknown or N/A.|
|[Pos_Location_Id](#pos_location_id)|`uniqueidentifier` |For POS sales, specifies the POS location, in which the sale is performed. NULL when the sales is not a POS sale.|
|[Pos_Terminal_Id](#pos_terminal_id)|`uniqueidentifier` |For POS sales, specifies the POS terminal, on which the sale is entered. NULL when the sales is not a POS sale.|
|[Pos_Operator_Id](#pos_operator_id)|`uniqueidentifier` |For POS sales, specifies the POS operator, who created the sale. NULL when the sale is not a POS sale.|
|[Fiscal_Printer_Pos_Device_Id](#fiscal_printer_pos_device_id)|`uniqueidentifier` |For POS sales, specifies the fiscal printer. NULL when the sales is not a POS sale.|
|[Fiscal_Sales_Number](#fiscal_sales_number)|`nvarchar` Readonly|Unique number of the sale, assigned for fiscal reporting purposes. The format is according to the applicable legislation. NULL means that there is no requirement for fiscal sales number for this document or it is unknown.|
|[Sales_Order_Line_Id](#sales_order_line_id)|`uniqueidentifier` `PK`||
|[Line_No](#line_no)|`int` ||
|[Product_Id](#product_id)|`uniqueidentifier` ||
|[Product_Description](#product_description)|`nvarchar` `ML`||
|[Quantity](#quantity)|`decimal(0, 0)` ||
|[Quantity_Unit_Id](#quantity_unit_id)|`uniqueidentifier` ||
|[Product_Price_Id](#product_price_id)|`uniqueidentifier` ||
|[Unit_Price](#unit_price)|`decimal(0, 0)` ||
|[Line_Discount_Id](#line_discount_id)|`uniqueidentifier` ||
|[Line_Standard_Discount_Percent](#line_standard_discount_percent)|`decimal(0, 0)` ||
|[Line_Custom_Discount_Percent](#line_custom_discount_percent)|`decimal(0, 0)` ||
|[Line_Amount](#line_amount)|`decimal(0, 0)` ||
|[Line_Required_Delivery_Date](#line_required_delivery_date)|`date` ||
|[Line_Store_Id](#line_store_id)|`uniqueidentifier` ||
|[Store_Bin_Id](#store_bin_id)|`uniqueidentifier` ||
|[Lot_Id](#lot_id)|`uniqueidentifier` ||
|[Guarantee_Period_Days](#guarantee_period_days)|`int` ||
|[Line_Deal_Type_Id](#line_deal_type_id)|`uniqueidentifier` ||
|[Product_Code_Id](#product_code_id)|`uniqueidentifier` ||
|[Bonus_Program_Id](#bonus_program_id)|`uniqueidentifier` ||
|[Line_Notes](#line_notes)|`nvarchar` ||
|[Return_For_Sales_Order_Line_Id](#return_for_sales_order_line_id)|`uniqueidentifier` ||
|[Historical_Unit_Cost](#historical_unit_cost)|`decimal(0, 0)` ||
|[Requested_Quantity](#requested_quantity)|`decimal(0, 0)` ||
|[Quantity_Base](#quantity_base)|`decimal(0, 0)` Readonly||
|[Promotional_Package_Id](#promotional_package_id)|`uniqueidentifier` ||
|[Standard_Unit_Price](#standard_unit_price)|`decimal(0, 0)` ||
|[Delivery_Terms_Code](#delivery_terms_code)|`nvarchar` Allowed: `EXW`, `FCA`, `FAS`, `FOB`, `CFR`, `CIF`, `CPT`, `CIP`, `DAP`, `DAT`, `DDP`, `DPU`|Mode of delivery, like CIF, FOB, etc. Used also in Intrastat reporting|
|[Intrastat_Transaction_Nature_Code](#intrastat_transaction_nature_code)|`nvarchar` Allowed: `11`, `12`, `13`, `14`, `19`, `21`, `22`, `23`, `29`, `60`, `70`, `80`, `91`, `99`, `30`, `41`, `42`, `51`, `52`|Transaction nature; used for Intrastat reporting|
|[Intrastat_Transport_Mode_Code](#intrastat_transport_mode_code)|`nvarchar` Allowed: `1`, `2`, `3`, `4`, `5`, `6`, `7`, `8`|Transport mode; used for Intrastat reporting|
|[Intrastat_Transport_Country_Id](#intrastat_transport_country_id)|`uniqueidentifier` |Country of origin of the transport company; used for Intrastat reporting|
|[Persist_Lot](#persist_lot)|`bit` ||
|[Serial_Number_Id](#serial_number_id)|`uniqueidentifier` ||
|[Product_Variant_Id](#product_variant_id)|`uniqueidentifier` ||
|[Parent_Line_No](#parent_line_no)|`int` |The number of the line within the parent document, which the current line executes. NULL when the current line does not execute parent line.|
|[Line_Parent_Document_Id](#line_parent_document_id)|`uniqueidentifier` |The document, which the current line executes. NULL when the current line does not execute another line.|
|[Return_For_Invoice_Line_Id](#return_for_invoice_line_id)|`uniqueidentifier` |When specified, indicates that the current line is a return for products, invoiced with the specified invoice line.|
|[Standard_Quantity_Base](#standard_quantity_base)|`decimal(0, 0)` Readonly|The theoretical quantity in base measurement unit according to the current measurement dimensions for the product. Used to measure the execution. NULL means to convert the value from Quantity using the measurement ratios.|
|[Historical_Data_Json](#historical_data_json)|`nvarchar` |Used only for lines, which are returns. It is a JSON-formatted string, containing data from the original sale.|
|[Line_End_Customer_Party_Id](#line_end_customer_party_id)|`uniqueidentifier` |The end customer is the customer of the dealer. It is stored for information purposes only. The end customer may not have customer definition, just party.|
|[Line_From_Date](#line_from_date)|`date` ||
|[Line_To_Date](#line_to_date)|`date` |When selling a service valid only for a period, denotes the end of the period. NULL means that it is unknown or N/A.|
|[Product_Name_By_Definition](#product_name_by_definition)|`nvarchar` `ML`||
|[Id](#id)|`uniqueidentifier` `PK`||
|[Part_Number](#part_number)|`nvarchar` ||
|[Product_Group_Id](#product_group_id)|`uniqueidentifier` ||
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
|[Minimal_Sales_Quantity_Base](#minimal_sales_quantity_base)|`decimal(0, 0)` ||
|[Short_Name](#short_name)|`nvarchar` `ML`||
|[Allow_Variable_Measurement_Ratios](#allow_variable_measurement_ratios)|`bit` |Allow variable (dynamic) measurement ratios for each transaction. If specified, each store transaction could specify different measurement ratio between the used measurement unit and the base measurement unit.|
|[Cargo_Type_Id](#cargo_type_id)|`uniqueidentifier` |Specifies what type of cargo this product is. Required when generating transportation requisitions. NULL means unspecified.|
|[Area_Id](#area_id)|`uniqueidentifier` ||
|[Customer_Type_Id](#customer_type_id)|`uniqueidentifier` ||
|[Sales_Person_Id_From_Customers](#sales_person_id_from_customers)|`uniqueidentifier` ||
|[Party_Id](#party_id)|`uniqueidentifier` ||
|[Customer_Number](#customer_number)|`nvarchar` ||
|[Party_Name](#party_name)|`nvarchar` `ML`||
|[Party_Type](#party_type)|`nvarchar` Allowed: `C`, `L`, `P`, `S`, `V`||
|[Country_Id](#country_id)|`uniqueidentifier` ||
|[Expiry_Date](#expiry_date)|`datetime` ||
|[Quantity_AMU](#quantity_amu)|`decimal(0, 0)` ||
|[Additional_Measurement_Unit_Id](#additional_measurement_unit_id)|`uniqueidentifier` ||
|[Area_Id_L1_Name](#area_id_l1_name)|`nvarchar` `ML`||
|[Area_Id_L2_Name](#area_id_l2_name)|`nvarchar` `ML`||
|[Area_Id_L3_Name](#area_id_l3_name)|`nvarchar` `ML`||
|[Area_Id_L4_Name](#area_id_l4_name)|`nvarchar` `ML`||
|[Area_Id_L5_Name](#area_id_l5_name)|`nvarchar` `ML`||
|[Area_Id_L6_Name](#area_id_l6_name)|`nvarchar` `ML`||
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
|[Additional_Amount](#additional_amount)|`decimal(0, 0)` ||
|[Add_To_Customer_Amount](#add_to_customer_amount)|`decimal(0, 0)` ||
|[Add_To_Line_Amount](#add_to_line_amount)|`decimal(0, 0)` ||
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

### Customer_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Ship_To_Customer_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Credit_Limit_Override

| Property | Value |
| - | - |
|Type|bit|

### Store_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Required_Delivery_Date

| Property | Value |
| - | - |
|Type|date|

### Payment_Due_Date

| Property | Value |
| - | - |
|Type|datetime|

### Payment_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Payment_Account_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Sales_Order_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Ship_To_Party_Contact_Mechanism_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Price_List_Id

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

### Deal_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Dealer_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Deal_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Notes_Sale_Order

| Property | Value |
| - | - |
|Type|nvarchar|

### Customer_Purchase_Order_No

| Property | Value |
| - | - |
|Type|nvarchar|

### Return_For_Sales_Order_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Return_For_Invoice_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Customer_Purchase_Order_Date

| Property | Value |
| - | - |
|Type|date|

### End_Customer_Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### From_Date

| Property | Value |
| - | - |
|Type|date|

### To_Date

| Property | Value |
| - | - |
|Type|date|

### Pos_Location_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Pos_Terminal_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Pos_Operator_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Fiscal_Printer_Pos_Device_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Fiscal_Sales_Number

| Property | Value |
| - | - |
|Type|nvarchar|

### Sales_Order_Line_Id

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

### Quantity_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Price_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Unit_Price

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Line_Discount_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Line_Standard_Discount_Percent

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Line_Custom_Discount_Percent

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Line_Amount

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Line_Required_Delivery_Date

| Property | Value |
| - | - |
|Type|date|

### Line_Store_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Store_Bin_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Lot_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Guarantee_Period_Days

| Property | Value |
| - | - |
|Type|int|

### Line_Deal_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Code_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Bonus_Program_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Line_Notes

| Property | Value |
| - | - |
|Type|nvarchar|

### Return_For_Sales_Order_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Historical_Unit_Cost

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Requested_Quantity

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Promotional_Package_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Standard_Unit_Price

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Delivery_Terms_Code

| Property | Value |
| - | - |
|Type|nvarchar|

### Intrastat_Transaction_Nature_Code

| Property | Value |
| - | - |
|Type|nvarchar|

### Intrastat_Transport_Mode_Code

| Property | Value |
| - | - |
|Type|nvarchar|

### Intrastat_Transport_Country_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Persist_Lot

| Property | Value |
| - | - |
|Type|bit|

### Serial_Number_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Variant_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Parent_Line_No

| Property | Value |
| - | - |
|Type|int|

### Line_Parent_Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Return_For_Invoice_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Standard_Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Historical_Data_Json

| Property | Value |
| - | - |
|Type|nvarchar|

### Line_End_Customer_Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Line_From_Date

| Property | Value |
| - | - |
|Type|date|

### Line_To_Date

| Property | Value |
| - | - |
|Type|date|

### Product_Name_By_Definition

| Property | Value |
| - | - |
|Type|nvarchar|

### Id

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

### Area_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Customer_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Sales_Person_Id_From_Customers

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Customer_Number

| Property | Value |
| - | - |
|Type|nvarchar|

### Party_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Party_Type

| Property | Value |
| - | - |
|Type|nvarchar|

### Country_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Expiry_Date

| Property | Value |
| - | - |
|Type|datetime|

### Quantity_AMU

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Additional_Measurement_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Area_Id_L1_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Area_Id_L2_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Area_Id_L3_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Area_Id_L4_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Area_Id_L5_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Area_Id_L6_Name

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

### Additional_Amount

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Add_To_Customer_Amount

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Add_To_Line_Amount

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Line_Amount_In_Base_Currency

| Property | Value |
| - | - |
|Type|decimal(0, 0)|


