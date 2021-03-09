# Query Inv_Projected_Availability_By_Lots_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` `PK`||
|[Store_Id](#store_id)|`uniqueidentifier` `PK`|Unique store Id|
|[Product_Id](#product_id)|`uniqueidentifier` |The product to which the lot is bound|
|[Lot_Id](#lot_id)|`uniqueidentifier` `PK`||
|[Document_Date](#document_date)|`datetime` ||
|[Planned_Quantity_Base](#planned_quantity_base)|`decimal(0, 0)` ||
|[Planned_Quantity_Base_To_Date](#planned_quantity_base_to_date)|`decimal(0, 0)` ||
|[On_Hand_Quantity_Base](#on_hand_quantity_base)|`decimal(0, 0)` ||
|[Projected_Available_Balance_Base](#projected_available_balance_base)|`decimal(0, 0)` ||
|[Available_To_Promise_For_Date_Base](#available_to_promise_for_date_base)|`decimal(0, 0)` ||
|[Company_Id](#company_id)|`uniqueidentifier` |Contains the base company data on which this enterprise company is based.|
|[Base_Currency_Id](#base_currency_id)|`uniqueidentifier` |The base currency for summary reporting for this company.|
|[Default_Language](#default_language)|`nvarchar` Allowed: `bg`, `en`|The default language for multi-language names in the definitions (like Customer_Name, Product_Name, ...).|
|[Default_Costing_Method](#default_costing_method)|`nvarchar` Allowed: `AVG`, `EXP`, `BLD`|Default method for cost evaluation (if not specified in the product). Currently supported: EXP - Explicit lot specifying; AVG - Average cost|
|[Exchange_Difference_Debit_Account_Id](#exchange_difference_debit_account_id)|`uniqueidentifier` |Account for balancing accounting vouchers with debit difference due to currency exchanges|
|[Exchange_Difference_Credit_Account_Id](#exchange_difference_credit_account_id)|`uniqueidentifier` |Account for balancing accounting vouchers with credit difference due to currency exchanges|
|[Advance_Product_Id](#advance_product_id)|`uniqueidentifier` |Product that is used for handling advances in trade documents.|
|[VAT_Document_Amount_Type_Id](#vat_document_amount_type_id)|`uniqueidentifier` |The document amount that is used to determine the amount of the VAT entries when they are generated.|
|[Edit_Period_Start_Date](#edit_period_start_date)|`datetime` |Start date of the priod when the documents can be edited|
|[Default_Customer_Credit_Limit_Base](#default_customer_credit_limit_base)|`decimal(0, 0)` ||
|[BI_Start_Date](#bi_start_date)|`datetime` ||
|[UI_Base_Color](#ui_base_color)|`int` |When not NULL, specifies the background color to use for visualization of the UI when the current enterprise company is selected. The color is in RGBA color format.|
|[Is_Active](#is_active)|`bit` |Indicates whether the current Enterprise company  is active.|
|[Print_Images_Retention_Months](#print_images_retention_months)|`int` |A period of months for which the printed images of the documents will be kept.|
|[Party_Id](#party_id)|`uniqueidentifier` |The party of the store. Each store is a party and is stored based on a party definition.|
|[Parent_Store_Id](#parent_store_id)|`uniqueidentifier` |Obsolete. Not used. (Hierarchy of the stores is now represented by the Store Groups entity).|
|[Store_Code](#store_code)|`nvarchar` ||
|[Store_Name](#store_name)|`nvarchar` `ML`|Name of the store|
|[Responsible_Party_Id](#responsible_party_id)|`uniqueidentifier` |Primary responsible party (usually employee) for the stock in the store.|
|[Number_Of_Dimensions](#number_of_dimensions)|`int` |Number of dimensions in the coordinate system of the storage bins. 0 means single-bin store. Currently, this is only stored for information and is not used for automatical generation of store bins, as it was intended.|
|[Default_Store_Bin_Id](#default_store_bin_id)|`uniqueidentifier` |To be used when store bin is unknown|
|[Default_Supply_Store_Id](#default_supply_store_id)|`uniqueidentifier` |The store from which goods are usually supplied to this store|
|[Unmanaged](#unmanaged)|`bit` |If 0 the system will expect the user to process the store transactions. If 1 the system will auto-generate them|
|[Schema_XML](#schema_xml)|`nvarchar` |Obsolete. Not used.|
|[Currency_Id](#currency_id)|`uniqueidentifier` |The currency for the warehouse cost calculations. When NULL, the base currency for the enterprise company will be used|
|[Store_Creation_Time](#store_creation_time)|`datetime` Readonly||
|[Creation_User](#creation_user)|`nvarchar` Readonly||
|[Store_Update_Time](#store_update_time)|`datetime` Readonly||
|[Update_User](#update_user)|`nvarchar` Readonly||
|[Enterprise_Company_Location_Id](#enterprise_company_location_id)|`uniqueidentifier` ||
|[Store_Group_Id](#store_group_id)|`uniqueidentifier` |The store group, to which this store belongs.|
|[Warehouse_Id](#warehouse_id)|`uniqueidentifier` |Specifies, the warehouse, which manages the warehouse operations for the store. NULL for stores, which do not have managed operations.|
|[Part_Number](#part_number)|`nvarchar` |Unique part number of the product|
|[Product_Group_Id](#product_group_id)|`uniqueidentifier` |The product group, under which the product is categorized.|
|[Product_Name](#product_name)|`nvarchar` `ML`|Name of the item|
|[Base_Measurement_Category_Id](#base_measurement_category_id)|`uniqueidentifier` |The base measurement category for quantities of this product.|
|[Measurement_Unit_Id](#measurement_unit_id)|`uniqueidentifier` |Default measurement unit, when creating new documents with this product.|
|[Product_Type_Id](#product_type_id)|`uniqueidentifier` |The type of the product. This also defines whether the product is stocked. NULL=no specific product type and the product is stocked|
|[Is_Serialized](#is_serialized)|`bit` |1 if the parts use/require serial numbers|
|[Standard_Price_Per_Lot](#standard_price_per_lot)|`decimal(0, 0)` |Standard sales price (used if no special price is defined) for one standard lot of the product in the currency, specified by Costing_Currency_Id|
|[Standard_Cost_Per_Lot](#standard_cost_per_lot)|`decimal(0, 0)` |Standard cost for one standard lot of the product in the currency, specified by Costing_Currency_Id|
|[Standard_Lot_Size_Base](#standard_lot_size_base)|`decimal(0, 0)` |The size of a standard lot, expressed in the base measurement unit of the product. Used for Standard_Cost and Standard_Price|
|[Planning_Demand_Time_Fence_Days](#planning_demand_time_fence_days)|`int` |Period in the future, in which changes to the MPS are not accepted due to the high cost of changing. Demand for the period is calculated based entirely on the customer orders. Abbr. - DTF (NULL = Default of 30 days)|
|[Planning_Time_Fence_Days](#planning_time_fence_days)|`int` |Period in the future inside of which changes to the MPS are carefully evaluated to prevent costly schedule disruption. Demand for the period between DTF and PTF is calculated as the bigger of customer orders and sales forecast. Abbr. - PTF. (NULL = Default of 90 days)|
|[Planning_Horizon_Days](#planning_horizon_days)|`int` |Number of days in the future for which to plan the demand and supply (NULL = Default of 180 days)|
|[Flushing_Method](#flushing_method)|`nvarchar` Allowed: `B`, `F`, `M`|Consumption method for work orders. M=Manual, using Consuption Journals, F=Forward (on release), B=Backward (on finish)|
|[Manufacturing_Policy](#manufacturing_policy)|`nvarchar` |Manufacturing policy controls the procurement planing system actions for this product. Allowed values are MTS=Make-To-Stock; MTO=Make-To-Order; ATO=Assemble-To-Order|
|[ABC_Class](#abc_class)|`nvarchar` Allowed: `A `, `B `, `C `|Product importance classification, where A are the most important and C - the least important products. Usually used as user filtering condition when previewing results of the procurement planning process.|
|[Supply_Schema_Id](#supply_schema_id)|`uniqueidentifier` |The supply schema to use for the distribution of the product among warehouses|
|[Scrap_Rate](#scrap_rate)|`decimal(0, 0)` |Default scrap rate for the recipe, when this product is used as ingredient|
|[Description](#description)|`nvarchar` `ML`|The description of the product|
|[Costing_Method](#costing_method)|`nvarchar` Allowed: `AVG`, `EXP`, `BLD`|Specifies the costing method for the product. NULL means to use the Enterprise Company default. Currently supported methods are: EXP - Explicitly specify lot; AVG - Average cost|
|[Costing_Currency_Id](#costing_currency_id)|`uniqueidentifier` |Specifies the currency to use for cost calculations for the product. When NULL, the base currency for the enterprise company should be used|
|[Product_Active](#product_active)|`bit` |1 if the product is active, 0 - not to list in combo boxes for choosing in new documents|
|[Guarantee_Period_Days](#guarantee_period_days)|`int` |Default guarantee period length in days. 0 means no guarantee. Should be non-NULL for serviced products and NULL for the others|
|[Product_Creation_Time](#product_creation_time)|`datetime` Readonly||
|[Product_Creation_User](#product_creation_user)|`nvarchar` Readonly||
|[Product_Update_Time](#product_update_time)|`datetime` Readonly||
|[Product_Update_User](#product_update_user)|`nvarchar` Readonly||
|[Purchase_Measurement_Unit_Id](#purchase_measurement_unit_id)|`uniqueidentifier` |Default measurement unit to use, when creating new purchase documents with this product.|
|[Valuation_Group_Id](#valuation_group_id)|`uniqueidentifier` |Valuation group of the product. Used in reconciliations when compensating pluses and minuses. Equal plus and minus amounts within a valuation group are allowed to be compensated with each other for zero net fiscal effect.|
|[Origin_Country_Id](#origin_country_id)|`uniqueidentifier` |Country from which the product originates (in which the product is produced/cultivated ...). Primarily used for Intrastat reporting.|
|[Intrastat_Commodity_Code_Id](#intrastat_commodity_code_id)|`uniqueidentifier` ||
|[Intrastat_Supplementary_Unit_Id](#intrastat_supplementary_unit_id)|`uniqueidentifier` ||
|[Use_Lots](#use_lots)|`nvarchar` Allowed: `A`, `N`, `R`|Specifies whether the use of lots for this product in store documents is required or is unallowed or is allowed while not required.|
|[Lots_Issue](#lots_issue)|`nvarchar` Allowed: `FIFO`, `FEFO`, `LIFO`|Determines the method by which the lots are automatically issued. The method determines the sequence of the lots: in the order of receipt (FIFO), in the order inverse of receipt (LIFO) or in the order of expiration (FEFO).|
|[Expiry_Period_Days](#expiry_period_days)|`int` |Total default expiry period for the product (in days) from the date of production to the date of expiry|
|[Show_In_Catalog](#show_in_catalog)|`bit` |Specifies whether to show the product in catalogs, referring to the product group of the product. 0=Do not show; 1=Show.|
|[Minimal_Sales_Price_Per_Lot](#minimal_sales_price_per_lot)|`decimal(0, 0)` |Minimal allowed price for sales of this product. The price is for one standard lot and in the costing currency of the product. The minimum is enforced upon planning and/or releasing a document. NULL means that there is no minimal sales price enforcement.|
|[Is_Featured](#is_featured)|`bit` ||
|[Minimal_Sales_Quantity_Base](#minimal_sales_quantity_base)|`decimal(0, 0)` |Minimal base quantity of this product that has to be specified in any sale.|
|[Short_Name](#short_name)|`nvarchar` `ML`||
|[Allow_Variable_Measurement_Ratios](#allow_variable_measurement_ratios)|`bit` |Allow variable (dynamic) measurement ratios for each transaction. If specified, each store transaction could specify different measurement ratio between the used measurement unit and the base measurement unit.|
|[Cargo_Type_Id](#cargo_type_id)|`uniqueidentifier` |Specifies what type of cargo this product is. Required when generating transportation requisitions. NULL means unspecified.|
|[Lot_Number](#lot_number)|`nvarchar` ||
|[Receipt_Store_Transaction_Id](#receipt_store_transaction_id)|`uniqueidentifier` |The store receipt transaction, which created the lot. NULL if the lot is manually created|
|[Production_Batch_Id](#production_batch_id)|`uniqueidentifier` |Non-NULL if the production batch is known. Production batches are automatically created for internal production, but can also be used for specifying production batches for purchased goods|
|[Status](#status)|`int` Allowed: `0`, `-1`, `-2`, `-3`|Status of the warehouse lot. Minus statuses describe blocked conditions.
-3 blocked for document (sales or service order)
-2 blocked for party
-1 blocked for inspection
0 free to use|
|[Blocked_For_Party_Id](#blocked_for_party_id)|`uniqueidentifier` |Non-NULL when the warehouse lot is blocked specifically for some party|
|[Blocked_For_Document_Id](#blocked_for_document_id)|`uniqueidentifier` |If non-null, contains the document for which the lot is blocked|
|[Expiry_Date](#expiry_date)|`datetime` ||
|[License_No](#license_no)|`nvarchar` |The license number for this lot. Null when license number is N/A or unknown.|
|[Lot_Description](#lot_description)|`nvarchar` `ML`||
|[Purchase_Lot_Number](#purchase_lot_number)|`nvarchar` |Identification of the purchase lost with which the products from this store lot are received. E.g. the document number of the Receiving order.|
|[Receipt_Date](#receipt_date)|`date` Readonly|The date of the first receipt of products in this lot.|
|[Certificate_Document_Id](#certificate_document_id)|`uniqueidentifier` ||
|[Excise_Measuring_Transaction_Id](#excise_measuring_transaction_id)|`uniqueidentifier` |When the lot was created in an excise controlled environment, specifies the measuring transaction which was used to create the lot.|
|[Product_Group_Id_L1_Name](#product_group_id_l1_name)|`nvarchar` `ML`||
|[Product_Group_Id_L2_Name](#product_group_id_l2_name)|`nvarchar` `ML`||
|[Product_Group_Id_L3_Name](#product_group_id_l3_name)|`nvarchar` `ML`||
|[Product_Group_Id_L4_Name](#product_group_id_l4_name)|`nvarchar` `ML`||
|[Product_Group_Id_L5_Name](#product_group_id_l5_name)|`nvarchar` `ML`||
|[Product_Group_Id_L6_Name](#product_group_id_l6_name)|`nvarchar` `ML`||
|[Store_Group_Id_L1_Name](#store_group_id_l1_name)|`nvarchar` `ML`||
|[Store_Group_Id_L2_Name](#store_group_id_l2_name)|`nvarchar` `ML`||
|[Store_Group_Id_L3_Name](#store_group_id_l3_name)|`nvarchar` `ML`||
|[Store_Group_Id_L4_Name](#store_group_id_l4_name)|`nvarchar` `ML`||
|[Store_Group_Id_L5_Name](#store_group_id_l5_name)|`nvarchar` `ML`||
|[Store_Group_Id_L6_Name](#store_group_id_l6_name)|`nvarchar` `ML`||

## Columns

### Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Store_Id

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

### Document_Date

| Property | Value |
| - | - |
|Type|datetime|

### Planned_Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Planned_Quantity_Base_To_Date

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### On_Hand_Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Projected_Available_Balance_Base

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Available_To_Promise_For_Date_Base

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Base_Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Default_Language

| Property | Value |
| - | - |
|Type|nvarchar|

### Default_Costing_Method

| Property | Value |
| - | - |
|Type|nvarchar|

### Exchange_Difference_Debit_Account_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Exchange_Difference_Credit_Account_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Advance_Product_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### VAT_Document_Amount_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Edit_Period_Start_Date

| Property | Value |
| - | - |
|Type|datetime|

### Default_Customer_Credit_Limit_Base

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### BI_Start_Date

| Property | Value |
| - | - |
|Type|datetime|

### UI_Base_Color

| Property | Value |
| - | - |
|Type|int|

### Is_Active

| Property | Value |
| - | - |
|Type|bit|

### Print_Images_Retention_Months

| Property | Value |
| - | - |
|Type|int|

### Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Parent_Store_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Store_Code

| Property | Value |
| - | - |
|Type|nvarchar|

### Store_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Responsible_Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Number_Of_Dimensions

| Property | Value |
| - | - |
|Type|int|

### Default_Store_Bin_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Default_Supply_Store_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Unmanaged

| Property | Value |
| - | - |
|Type|bit|

### Schema_XML

| Property | Value |
| - | - |
|Type|nvarchar|

### Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Store_Creation_Time

| Property | Value |
| - | - |
|Type|datetime|

### Creation_User

| Property | Value |
| - | - |
|Type|nvarchar|

### Store_Update_Time

| Property | Value |
| - | - |
|Type|datetime|

### Update_User

| Property | Value |
| - | - |
|Type|nvarchar|

### Enterprise_Company_Location_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Store_Group_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Warehouse_Id

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

### Product_Active

| Property | Value |
| - | - |
|Type|bit|

### Guarantee_Period_Days

| Property | Value |
| - | - |
|Type|int|

### Product_Creation_Time

| Property | Value |
| - | - |
|Type|datetime|

### Product_Creation_User

| Property | Value |
| - | - |
|Type|nvarchar|

### Product_Update_Time

| Property | Value |
| - | - |
|Type|datetime|

### Product_Update_User

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

### Status

| Property | Value |
| - | - |
|Type|int|

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

### Lot_Description

| Property | Value |
| - | - |
|Type|nvarchar|

### Purchase_Lot_Number

| Property | Value |
| - | - |
|Type|nvarchar|

### Receipt_Date

| Property | Value |
| - | - |
|Type|date|

### Certificate_Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Excise_Measuring_Transaction_Id

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

### Store_Group_Id_L1_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Store_Group_Id_L2_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Store_Group_Id_L3_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Store_Group_Id_L4_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Store_Group_Id_L5_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Store_Group_Id_L6_Name

| Property | Value |
| - | - |
|Type|nvarchar|


