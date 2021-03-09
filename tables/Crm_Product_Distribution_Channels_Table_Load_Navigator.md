# Query Crm_Product_Distribution_Channels_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Product_Distribution_Channel_Id](#product_distribution_channel_id)|`uniqueidentifier` `PK`||
|[Product_Id](#product_id)|`uniqueidentifier` ||
|[Distribution_Channel_Id](#distribution_channel_id)|`uniqueidentifier` ||
|[From_Date](#from_date)|`date` ||
|[To_Date](#to_date)|`date` ||
|[Is_Active](#is_active)|`bit` ||
|[Minimal_Sales_Price_Per_Lot](#minimal_sales_price_per_lot)|`decimal(0, 0)` |Minimal allowed price for sales of this product through this channel. The price is for one standard lot and in the costing currency of the product. The minimum is enforced upon planning and/or releasing a document. NULL means that there is no minimal sales price enforcement.|
|[Minimal_Sales_Quantity_Base](#minimal_sales_quantity_base)|`decimal(0, 0)` |Minimal base quantity of the current product that has to be specified in any sale for this distribution channel.|
|[Id](#id)|`uniqueidentifier` `PK`|Unique id of the item|
|[Part_Number](#part_number)|`nvarchar` |Unique part number of the item|
|[Product_Group_Id](#product_group_id)|`uniqueidentifier` |Id of the containing group|
|[Product_Name](#product_name)|`nvarchar` `ML`|Name of the item|
|[Base_Measurement_Category_Id](#base_measurement_category_id)|`uniqueidentifier` ||
|[Measurement_Unit_Id](#measurement_unit_id)|`uniqueidentifier` |Measurement category used to calculate inventory and demand|
|[Product_Type_Id](#product_type_id)|`uniqueidentifier` |The type of the product. This also defines whether the product is stocked. NULL=no specific product type and the product is stocked|
|[Is_Serialized](#is_serialized)|`bit` |1 if the parts use/require serial numbers|
|[Standard_Price_Per_Lot](#standard_price_per_lot)|`decimal(0, 0)` |Standard sales price (used if no special price is defined) for one standard lot of the product in the currency, specified by Costing_Currency_Id|
|[Standard_Cost_Per_Lot](#standard_cost_per_lot)|`decimal(0, 0)` |Standard cost for one standard lot of the product in the currency, specified by Costing_Currency_Id|
|[Standard_Lot_Size_Base](#standard_lot_size_base)|`decimal(0, 0)` |The size of a standard lot, expressed in the base measurement unit of the product. Used for Standard_Cost and Standard_Price|
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
|[Costing_Currency_Id](#costing_currency_id)|`uniqueidentifier` |Specifies the currency to use for cost calculations for the product. When NULL, the base currency for the enterprise company should be used|
|[Active](#active)|`bit` |1 if the product is active, 0 - not to list in combo boxes for choosing in new documents|
|[Guarantee_Period_Days](#guarantee_period_days)|`int` |Default guarantee period length in days. 0 means no guarantee. Should be non-NULL for serviced products and NULL for the others|
|[Creation_Time](#creation_time)|`datetime` Readonly||
|[Creation_User](#creation_user)|`nvarchar` Readonly||
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
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` |When not NULL, specifies that the product is specific to a given enterprise company and may be used only in documents from this enterprise company.|
|[Show_In_Catalog](#show_in_catalog)|`bit` |Specifies whether to show the product in catalogs, referring to the product group of the product. 0=Do not show; 1=Show.|
|[Product_Minimal_Sales_Price_Per_Lot](#product_minimal_sales_price_per_lot)|`decimal(0, 0)` |Minimal allowed price for sales of this product. The price is for one standard lot and in the costing currency of the product. The minimum is enforced upon planning and/or releasing a document. NULL means that there is no minimal sales price enforcement.|
|[Is_Featured](#is_featured)|`bit` ||
|[Product_Minimal_Sales_Quantity_Base](#product_minimal_sales_quantity_base)|`decimal(0, 0)` |Minimal base quantity of this product that has to be specified in any sale.|
|[Short_Name](#short_name)|`nvarchar` `ML`||
|[Allow_Variable_Measurement_Ratios](#allow_variable_measurement_ratios)|`bit` |Allow variable (dynamic) measurement ratios for each transaction. If specified, each store transaction could specify different measurement ratio between the used measurement unit and the base measurement unit.|
|[Cargo_Type_Id](#cargo_type_id)|`uniqueidentifier` |Specifies what type of cargo this product is. Required when generating transportation requisitions. NULL means unspecified.|
|[Product_Group_Id_L1_Name](#product_group_id_l1_name)|`nvarchar` `ML`||
|[Product_Group_Id_L2_Name](#product_group_id_l2_name)|`nvarchar` `ML`||
|[Product_Group_Id_L3_Name](#product_group_id_l3_name)|`nvarchar` `ML`||
|[Product_Group_Id_L4_Name](#product_group_id_l4_name)|`nvarchar` `ML`||
|[Product_Group_Id_L5_Name](#product_group_id_l5_name)|`nvarchar` `ML`||
|[Product_Group_Id_L6_Name](#product_group_id_l6_name)|`nvarchar` `ML`||

## Columns

### Product_Distribution_Channel_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Distribution_Channel_Id

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

### Is_Active

| Property | Value |
| - | - |
|Type|bit|

### Minimal_Sales_Price_Per_Lot

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Minimal_Sales_Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

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

### Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Show_In_Catalog

| Property | Value |
| - | - |
|Type|bit|

### Product_Minimal_Sales_Price_Per_Lot

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Is_Featured

| Property | Value |
| - | - |
|Type|bit|

### Product_Minimal_Sales_Quantity_Base

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


