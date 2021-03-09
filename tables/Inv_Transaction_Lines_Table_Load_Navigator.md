# Query Inv_Transaction_Lines_Table_Load_Navigator


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
|[Parent_Store_Order_Id](#parent_store_order_id)|`uniqueidentifier` |The parent (generating) store order. Deprecated, use the Parent Document reference.|
|[Is_Scrap](#is_scrap)|`bit` ||
|[Scrap_Type_Id](#scrap_type_id)|`uniqueidentifier` ||
|[Store_Id](#store_id)|`uniqueidentifier` ||
|[Issuing_Person_Id](#issuing_person_id)|`uniqueidentifier` ||
|[Receiving_Person_Id](#receiving_person_id)|`uniqueidentifier` ||
|[Movement_Type](#movement_type)|`nvarchar` Allowed: `I`, `R`||
|[Document_Currency_Id](#document_currency_id)|`uniqueidentifier` |The currency in which the document amounts are recorded.|
|[Cost_Source](#cost_source)|`nvarchar` Allowed: `S`, `D`, Readonly||
|[IsValid](#isvalid)|`bit` |Managed by the system and used only for integrity purposes. Do not use.|
|[Is_Single_Execution](#is_single_execution)|`bit` Readonly|Specifies whether the document is a single execution of its order document.|
|[Is_Released](#is_released)|`bit` Readonly|True if the document is not void and its state is released or greater|
|[Transaction_Line_Id](#transaction_line_id)|`uniqueidentifier` `PK`||
|[Transaction_Id](#transaction_id)|`uniqueidentifier` |The transaction to which the transaction line belongs.|
|[Line_No](#line_no)|`int` ||
|[Parent_Store_Order_Line_Id](#parent_store_order_line_id)|`uniqueidentifier` ||
|[Store_Bin_Id](#store_bin_id)|`uniqueidentifier` ||
|[Original_Product_Id](#original_product_id)|`uniqueidentifier` ||
|[Product_Id](#product_id)|`uniqueidentifier` ||
|[Lot_Id](#lot_id)|`uniqueidentifier` |If non-null, contains the specific lot to use for the movement|
|[Serial_Number_Id](#serial_number_id)|`uniqueidentifier` |Item serial number for serialized items. NULL for non-serialized items|
|[Quantity](#quantity)|`decimal(0, 0)` ||
|[Quantity_Unit_Id](#quantity_unit_id)|`uniqueidentifier` ||
|[Quantity_Base](#quantity_base)|`decimal(0, 0)` Readonly||
|[Notes](#notes)|`nvarchar` ||
|[Temp_Order_No](#temp_order_no)|`nvarchar` |Obsolete. Not used.|
|[Finished](#finished)|`bit` ||
|[Unit_Cost](#unit_cost)|`decimal(0, 0)` ||
|[Line_Cost](#line_cost)|`decimal(0, 0)` ||
|[Line_Document_Cost](#line_document_cost)|`decimal(0, 0)` Readonly||
|[Line_Product_Cost](#line_product_cost)|`decimal(0, 0)` Readonly||
|[Line_Store_Cost](#line_store_cost)|`decimal(0, 0)` Readonly||
|[Line_Base_Cost](#line_base_cost)|`decimal(0, 0)` Readonly||
|[Guarantee_Period_Days](#guarantee_period_days)|`int` ||
|[Parent_Line_Id](#parent_line_id)|`uniqueidentifier` |Used, when transaction lines are generated directly from other entities (different from Store Order). Denotes the Id of the parent document line, which generated the transaction line.|
|[Product_Code_Id](#product_code_id)|`uniqueidentifier` ||
|[Transaction_Timestamp](#transaction_timestamp)|`datetime` ||
|[Allow_Over_Execution](#allow_over_execution)|`bit` |When true, specifies, that we explicitly allow over-execution. Over-execution is when the quantity in all execution lines exceed the quantity in the parent store order line.|
|[Product_Variant_Id](#product_variant_id)|`uniqueidentifier` |If specified determines which product variant of the current product in this line is used.|
|[Parent_Line_No](#parent_line_no)|`int` |The number of the line within the parent document, which the current line executes. NULL when the current line does not execute line.|
|[Inv_Transaction_Line_Parent_Document_Id](#inv_transaction_line_parent_document_id)|`uniqueidentifier` |The document, which the current line executes. NULL when the current line does not execute another line.|
|[Standard_Quantity_Base](#standard_quantity_base)|`decimal(0, 0)` Readonly|The theoretical quantity in base measurement unit according to the current measurement dimensions of the product. Used to measure the execution. NULL means to take the value from Quantity Base.|
|[Lot_Number](#lot_number)|`nvarchar` ||
|[Receipt_Store_Transaction_Id](#receipt_store_transaction_id)|`uniqueidentifier` |The store receipt transaction, which created the lot. NULL if the lot is manually created|
|[Production_Batch_Id](#production_batch_id)|`uniqueidentifier` |Non-NULL if the production batch is known. Production batches are automatically created for internal production, but can also be used for specifying production batches for purchased goods|
|[Blocked_For_Party_Id](#blocked_for_party_id)|`uniqueidentifier` |Non-NULL when the warehouse lot is blocked specifically for some party|
|[Blocked_For_Document_Id](#blocked_for_document_id)|`uniqueidentifier` |If non-null, contains the document for which the lot is blocked|
|[Expiry_Date](#expiry_date)|`datetime` ||
|[License_No](#license_no)|`nvarchar` |The license number for this lot. Null when license number is N/A or unknown.|
|[Purchase_Lot_Number](#purchase_lot_number)|`nvarchar` |Identification of the purchase lost with which the products from this store lot are received. E.g. the document number of the Receiving order.|
|[Part_Number](#part_number)|`nvarchar` |Unique part number of the item|
|[Product_Group_Id](#product_group_id)|`uniqueidentifier` ||
|[Product_Name](#product_name)|`nvarchar` `ML`||
|[Base_Measurement_Category_Id](#base_measurement_category_id)|`uniqueidentifier` ||
|[Measurement_Unit_Id](#measurement_unit_id)|`uniqueidentifier` |Measurement category used to calculate inventory and demand|
|[Product_Type_Id](#product_type_id)|`uniqueidentifier` ||
|[Is_Serialized](#is_serialized)|`bit` |1 if the parts use/require serial numbers|
|[Standard_Price_Per_Lot](#standard_price_per_lot)|`decimal(0, 0)` ||
|[Standard_Cost_Per_Lot](#standard_cost_per_lot)|`decimal(0, 0)` |Standard cost for one standard lot of the product in the currency, specified by Costing_Currency_Id|
|[Standard_Lot_Size_Base](#standard_lot_size_base)|`decimal(0, 0)` ||
|[Planning_Demand_Time_Fence_Days](#planning_demand_time_fence_days)|`int` |Period in the future, in which changes to the MPS are not accepted due to the high cost of changing. Demand for the period is calculated based entirely on the customer orders. Abbr. - DTF (NULL = Default of 30 days)|
|[Planning_Time_Fence_Days](#planning_time_fence_days)|`int` |Period in the future inside of which changes to the MPS are carefully evaluated to prevent costly schedule disruption. Demand for the period between DTF and PTF is calculated as the bigger of customer orders and sales forecast. Abbr. - PTF. (NULL = Default of 90 days)|
|[Planning_Horizon_Days](#planning_horizon_days)|`int` |Number of days in the future for which to plan the demand and supply (NULL = Default of 180 days)|
|[Flushing_Method](#flushing_method)|`nvarchar` Allowed: `B`, `F`, `M`|Consumption method for work orders. M=Manual, using Consuption Journals, F=Forward (on release), B=Backward (on finish)|
|[Manufacturing_Policy](#manufacturing_policy)|`nvarchar` |MTS=Make-To-Stock; MTO=Make-To-Order; ATO=Assemble-To-Order|
|[ABC_Class](#abc_class)|`nvarchar` Allowed: `A `, `B `, `C `|Importance classification. A=Most important, AA, B, BB,  C, CC=Least important|
|[Supply_Schema_Id](#supply_schema_id)|`uniqueidentifier` |The supply schema to use for the distribution of the product among warehouses|
|[Scrap_Rate](#scrap_rate)|`decimal(0, 0)` |Default scrap rate for the recipe, when this product is used as ingredient|
|[Description](#description)|`nvarchar` `ML`|The description of the product|
|[Costing_Method](#costing_method)|`nvarchar` Allowed: `AVG`, `EXP`, `BLD`|Specifies the costing method for the product. NULL means to use the Enterprise Company default. Currently supported methods are: EXP - Explicitly specify lot; AVG - Average cost|
|[Active](#active)|`bit` |1 if the product is active, 0 - not to list in combo boxes for choosing in new documents|
|[Update_Time](#update_time)|`datetime` Readonly||
|[Update_User](#update_user)|`nvarchar` Readonly||
|[Purchase_Measurement_Unit_Id](#purchase_measurement_unit_id)|`uniqueidentifier` ||
|[Valuation_Group_Id](#valuation_group_id)|`uniqueidentifier` ||
|[Origin_Country_Id](#origin_country_id)|`uniqueidentifier` |Country from which the product originates (in which the product is produced/cultivated ...)|
|[Intrastat_Commodity_Code_Id](#intrastat_commodity_code_id)|`uniqueidentifier` |Product code from the Intrastat Combined nomenclature. Used when creating Intrastat declarations.|
|[Intrastat_Supplementary_Unit_Id](#intrastat_supplementary_unit_id)|`uniqueidentifier` |Additional measurement unit from the Intrastat Combined nomenclature. Used when creating Intrastat declarations.|
|[Use_Lots](#use_lots)|`nvarchar` Allowed: `A`, `N`, `R`|Specifies whether the use of lots for this product in store documents is required or is unallowed or is allowed while not required.|
|[Lots_Issue](#lots_issue)|`nvarchar` Allowed: `FIFO`, `FEFO`, `LIFO`|Determines the method by which the lots are automatically issued. The method determines the sequence of the lots: in the order of receipt (FIFO), in the order inverse of receipt (LIFO) or in the order of expiration (FEFO).|
|[Expiry_Period_Days](#expiry_period_days)|`int` |Total default expiry period for the product (in days) from the date of production to the date of expiry|
|[Product_Enterprise_Company_Id](#product_enterprise_company_id)|`uniqueidentifier` |When not NULL, specifies that the product is specific to a given enterprise company and may be used only in documents from this enterprise company.|
|[Show_In_Catalog](#show_in_catalog)|`bit` |Specifies whether to show the product in catalogs, referring to the product group of the product. 0=Do not show; 1=Show.|
|[Minimal_Sales_Price_Per_Lot](#minimal_sales_price_per_lot)|`decimal(0, 0)` |Minimal allowed price for sales of this product. The price is for one standard lot and in the costing currency of the product. The minimum is enforced upon planning and/or releasing a document. NULL means that there is no minimal sales price enforcement.|
|[Is_Featured](#is_featured)|`bit` ||
|[Minimal_Sales_Quantity_Base](#minimal_sales_quantity_base)|`decimal(0, 0)` |Minimal base quantity of this product that has to be specified in any sale.|
|[Short_Name](#short_name)|`nvarchar` `ML`||
|[Allow_Variable_Measurement_Ratios](#allow_variable_measurement_ratios)|`bit` |Allow variable (dynamic) measurement ratios for each transaction. If specified, each store transaction could specify different measurement ratio between the used measurement unit and the base measurement unit.|
|[Cargo_Type_Id](#cargo_type_id)|`uniqueidentifier` |Specifies what type of cargo this product is. Required when generating transportation requisitions. NULL means unspecified.|
|[Costing_Currency_Id](#costing_currency_id)|`uniqueidentifier` ||
|[Base_Measurement_Unit_Id](#base_measurement_unit_id)|`uniqueidentifier` ||
|[Product_Group_Full_Path](#product_group_full_path)|`nvarchar` ||
|[PG_L1_Name](#pg_l1_name)|`nvarchar` `ML`||
|[PG_L2_Name](#pg_l2_name)|`nvarchar` `ML`||
|[PG_L3_Name](#pg_l3_name)|`nvarchar` `ML`||
|[PG_L4_Name](#pg_l4_name)|`nvarchar` `ML`||
|[PG_L5_Name](#pg_l5_name)|`nvarchar` `ML`||
|[PG_L6_Name](#pg_l6_name)|`nvarchar` `ML`||
|[Cost_Correction_Amount](#cost_correction_amount)|`decimal(0, 0)` ||
|[Product_Cost_Adjustment](#product_cost_adjustment)|`decimal(0, 0)` ||
|[Store_Cost_Adjustment](#store_cost_adjustment)|`decimal(0, 0)` ||
|[Base_Cost_Adjustment](#base_cost_adjustment)|`decimal(0, 0)` ||
|[Adjusted_Document_Cost](#adjusted_document_cost)|`decimal(0, 0)` ||
|[Adjusted_Base_Cost](#adjusted_base_cost)|`decimal(0, 0)` ||
|[Adjusted_Product_Cost](#adjusted_product_cost)|`decimal(0, 0)` ||
|[Adjusted_Store_Cost](#adjusted_store_cost)|`decimal(0, 0)` ||
|[Quantity_AMU](#quantity_amu)|`decimal(0, 0)` ||
|[Additional_Measurement_Unit_Id](#additional_measurement_unit_id)|`uniqueidentifier` ||
|[Product_Group_Id_L1_Name](#product_group_id_l1_name)|`nvarchar` `ML`||
|[Product_Group_Id_L2_Name](#product_group_id_l2_name)|`nvarchar` `ML`||
|[Product_Group_Id_L3_Name](#product_group_id_l3_name)|`nvarchar` `ML`||
|[Product_Group_Id_L4_Name](#product_group_id_l4_name)|`nvarchar` `ML`||
|[Product_Group_Id_L5_Name](#product_group_id_l5_name)|`nvarchar` `ML`||
|[Product_Group_Id_L6_Name](#product_group_id_l6_name)|`nvarchar` `ML`||
|[Customer_Purchase_Order_No](#customer_purchase_order_no)|`nvarchar` ||

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

### Parent_Store_Order_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Is_Scrap

| Property | Value |
| - | - |
|Type|bit|

### Scrap_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Store_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Issuing_Person_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Receiving_Person_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Movement_Type

| Property | Value |
| - | - |
|Type|nvarchar|

### Document_Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Cost_Source

| Property | Value |
| - | - |
|Type|nvarchar|

### IsValid

| Property | Value |
| - | - |
|Type|bit|

### Is_Single_Execution

| Property | Value |
| - | - |
|Type|bit|

### Is_Released

| Property | Value |
| - | - |
|Type|bit|

### Transaction_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Transaction_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Line_No

| Property | Value |
| - | - |
|Type|int|

### Parent_Store_Order_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Store_Bin_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Original_Product_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Lot_Id

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

### Quantity_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar|

### Temp_Order_No

| Property | Value |
| - | - |
|Type|nvarchar|

### Finished

| Property | Value |
| - | - |
|Type|bit|

### Unit_Cost

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Line_Cost

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Line_Document_Cost

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Line_Product_Cost

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Line_Store_Cost

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Line_Base_Cost

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Guarantee_Period_Days

| Property | Value |
| - | - |
|Type|int|

### Parent_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Code_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Transaction_Timestamp

| Property | Value |
| - | - |
|Type|datetime|

### Allow_Over_Execution

| Property | Value |
| - | - |
|Type|bit|

### Product_Variant_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Parent_Line_No

| Property | Value |
| - | - |
|Type|int|

### Inv_Transaction_Line_Parent_Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Standard_Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Lot_Number

| Property | Value |
| - | - |
|Type|nvarchar|

### Receipt_Store_Transaction_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Production_Batch_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Blocked_For_Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Blocked_For_Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Expiry_Date

| Property | Value |
| - | - |
|Type|datetime|

### License_No

| Property | Value |
| - | - |
|Type|nvarchar|

### Purchase_Lot_Number

| Property | Value |
| - | - |
|Type|nvarchar|

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

### Costing_Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Base_Measurement_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Group_Full_Path

| Property | Value |
| - | - |
|Type|nvarchar|

### PG_L1_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### PG_L2_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### PG_L3_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### PG_L4_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### PG_L5_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### PG_L6_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Cost_Correction_Amount

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Product_Cost_Adjustment

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Store_Cost_Adjustment

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Base_Cost_Adjustment

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Adjusted_Document_Cost

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Adjusted_Base_Cost

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Adjusted_Product_Cost

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Adjusted_Store_Cost

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Quantity_AMU

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

### Customer_Purchase_Order_No

| Property | Value |
| - | - |
|Type|nvarchar|


