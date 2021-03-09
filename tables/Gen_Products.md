# Table Gen_Products

Products are the different items in the enterprise, which can be purchased, stored, sold and depreciated. Entity: Gen_Products

## Summary

| Name | Type | Description |
| - | - | --- |
|[Id](#id)|`uniqueidentifier` `PK`|Unique id of the item|
|[Part_Number](#part_number)|`nvarchar(32)` |Unique part number of the product|
|[Product_Group_Id](#product_group_id)|`uniqueidentifier` |The product group, under which the product is categorized.|
|[Product_Name](#product_name)|`nvarchar(254)` `ML`|Name of the item|
|[Short_Name](#short_name)|`nvarchar(128)` `ML`|Short name of the product. Used for space-constrained devices, like mobile phones, fiscal printers, etc.|
|[Description](#description)|`nvarchar(2147483647)` `ML`|The description of the product|
|[Base_Measurement_Category_Id](#base_measurement_category_id)|`uniqueidentifier` |The base measurement category for quantities of this product.|
|[Measurement_Unit_Id](#measurement_unit_id)|`uniqueidentifier` |Default measurement unit, when creating new documents with this product.|
|[Product_Type_Id](#product_type_id)|`uniqueidentifier` |The type of the product. This also defines whether the product is stocked. NULL=no specific product type and the product is stocked|
|[Is_Serialized](#is_serialized)|`bit` |1 if the parts use/require serial numbers|
|[Is_Featured](#is_featured)|`bit` ||
|[Standard_Price_Per_Lot](#standard_price_per_lot)|`decimal(18, 4)` |Standard sales price (used if no special price is defined) for one standard lot of the product in the currency, specified by Costing_Currency_Id|
|[Standard_Cost_Per_Lot](#standard_cost_per_lot)|`decimal(18, 4)` |Standard cost for one standard lot of the product in the currency, specified by Costing_Currency_Id|
|[Standard_Lot_Size_Base](#standard_lot_size_base)|`decimal(18, 3)` |The size of a standard lot, expressed in the base measurement unit of the product. Used for Standard_Cost and Standard_Price|
|[Minimal_Sales_Price_Per_Lot](#minimal_sales_price_per_lot)|`decimal(18, 4)` |Minimal allowed price for sales of this product. The price is for one standard lot and in the costing currency of the product. The minimum is enforced upon planning and/or releasing a document. NULL means that there is no minimal sales price enforcement.|
|[Minimal_Sales_Quantity_Base](#minimal_sales_quantity_base)|`decimal(18, 3)` |Minimal base quantity of this product that has to be specified in any sale.|
|[Show_In_Catalog](#show_in_catalog)|`bit` |Specifies whether to show the product in catalogs, referring to the product group of the product. 0=Do not show; 1=Show.|
|[Catalog_Description_Html](#catalog_description_html)|`nvarchar(2147483647)` |Full HTML description of the product. Usually used for display on product catalogs, web pages, etc.|
|[Planning_Demand_Time_Fence_Days](#planning_demand_time_fence_days)|`int` |Period in the future, in which changes to the MPS are not accepted due to the high cost of changing. Demand for the period is calculated based entirely on the customer orders. Abbr. - DTF (NULL = Default of 30 days)|
|[Planning_Time_Fence_Days](#planning_time_fence_days)|`int` |Period in the future inside of which changes to the MPS are carefully evaluated to prevent costly schedule disruption. Demand for the period between DTF and PTF is calculated as the bigger of customer orders and sales forecast. Abbr. - PTF. (NULL = Default of 90 days)|
|[Planning_Horizon_Days](#planning_horizon_days)|`int` |Number of days in the future for which to plan the demand and supply (NULL = Default of 180 days)|
|[Flushing_Method](#flushing_method)|`nvarchar(1)` Allowed: `B`, `F`, `M`|Consumption method for work orders. M=Manual, using Consuption Journals, F=Forward (on release), B=Backward (on finish)|
|[Manufacturing_Policy](#manufacturing_policy)|`nvarchar(3)` |Manufacturing policy controls the procurement planing system actions for this product. Allowed values are MTS=Make-To-Stock; MTO=Make-To-Order; ATO=Assemble-To-Order|
|[ABC_Class](#abc_class)|`nvarchar(2)` Allowed: `A `, `B `, `C `|Product importance classification, where A are the most important and C - the least important products. Usually used as user filtering condition when previewing results of the procurement planning process.|
|[Supply_Schema_Id](#supply_schema_id)|`uniqueidentifier` |The supply schema to use for the distribution of the product among warehouses|
|[Scrap_Rate](#scrap_rate)|`decimal(7, 6)` |Default scrap rate for the recipe, when this product is used as ingredient|
|[Costing_Method](#costing_method)|`nvarchar(4)` Allowed: `AVG`, `EXP`, `BLD`|Specifies the costing method for the product. NULL means to use the Enterprise Company default. Currently supported methods are: EXP - Explicitly specify lot; AVG - Average cost|
|[Costing_Currency_Id](#costing_currency_id)|`uniqueidentifier` |Specifies the currency to use for cost calculations for the product. When NULL, the base currency for the enterprise company should be used|
|[Active](#active)|`bit` |1 if the product is active, 0 - not to list in combo boxes for choosing in new documents|
|[Guarantee_Period_Days](#guarantee_period_days)|`int` |Default guarantee period length in days. 0 means no guarantee. Should be non-NULL for serviced products and NULL for the others|
|[Creation_Time](#creation_time)|`datetime` Readonly||
|[Creation_User](#creation_user)|`nvarchar(64)` Readonly||
|[Update_Time](#update_time)|`datetime` Readonly||
|[Update_User](#update_user)|`nvarchar(64)` Readonly||
|[Purchase_Measurement_Unit_Id](#purchase_measurement_unit_id)|`uniqueidentifier` |Default measurement unit to use, when creating new purchase documents with this product.|
|[Valuation_Group_Id](#valuation_group_id)|`uniqueidentifier` |Valuation group of the product. Used in reconciliations when compensating pluses and minuses. Equal plus and minus amounts within a valuation group are allowed to be compensated with each other for zero net fiscal effect.|
|[Origin_Country_Id](#origin_country_id)|`uniqueidentifier` |Country from which the product originates (in which the product is produced/cultivated ...). Primarily used for Intrastat reporting.|
|[Intrastat_Commodity_Code_Id](#intrastat_commodity_code_id)|`uniqueidentifier` ||
|[Intrastat_Supplementary_Unit_Id](#intrastat_supplementary_unit_id)|`uniqueidentifier` ||
|[Use_Lots](#use_lots)|`nvarchar(1)` Allowed: `A`, `N`, `R`|Specifies whether the use of lots for this product in store documents is required or is unallowed or is allowed while not required.|
|[Lots_Issue](#lots_issue)|`nvarchar(4)` Allowed: `FIFO`, `FEFO`, `LIFO`|Determines the method by which the lots are automatically issued. The method determines the sequence of the lots: in the order of receipt (FIFO), in the order inverse of receipt (LIFO) or in the order of expiration (FEFO).|
|[Expiry_Period_Days](#expiry_period_days)|`int` |Total default expiry period for the product (in days) from the date of production to the date of expiry|
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` |When not NULL, specifies that the product is specific to a given enterprise company and may be used only in documents from this enterprise company.|
|[Allow_Variable_Measurement_Ratios](#allow_variable_measurement_ratios)|`bit` |Allow variable (dynamic) measurement ratios for each transaction. If specified, each store transaction could specify different measurement ratio between the used measurement unit and the base measurement unit.|
|[Row_Version](#row_version)|`timestamp` ||
|[Cargo_Type_Id](#cargo_type_id)|`uniqueidentifier` |Specifies what type of cargo this product is. Required when generating transportation requisitions. NULL means unspecified.|

## Columns

### Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Part_Number

| Property | Value |
| - | - |
|Type|nvarchar(32)|

### Product_Group_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Name

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Short_Name

| Property | Value |
| - | - |
|Type|nvarchar(128)|

### Description

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

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

### Is_Featured

| Property | Value |
| - | - |
|Type|bit|

### Standard_Price_Per_Lot

| Property | Value |
| - | - |
|Type|decimal(18, 4)|

### Standard_Cost_Per_Lot

| Property | Value |
| - | - |
|Type|decimal(18, 4)|

### Standard_Lot_Size_Base

| Property | Value |
| - | - |
|Type|decimal(18, 3)|

### Minimal_Sales_Price_Per_Lot

| Property | Value |
| - | - |
|Type|decimal(18, 4)|

### Minimal_Sales_Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(18, 3)|

### Show_In_Catalog

| Property | Value |
| - | - |
|Type|bit|

### Catalog_Description_Html

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

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
|Type|nvarchar(1)|

### Manufacturing_Policy

| Property | Value |
| - | - |
|Type|nvarchar(3)|

### ABC_Class

| Property | Value |
| - | - |
|Type|nvarchar(2)|

### Supply_Schema_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Scrap_Rate

| Property | Value |
| - | - |
|Type|decimal(7, 6)|

### Costing_Method

| Property | Value |
| - | - |
|Type|nvarchar(4)|

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
|Type|nvarchar(64)|

### Update_Time

| Property | Value |
| - | - |
|Type|datetime|

### Update_User

| Property | Value |
| - | - |
|Type|nvarchar(64)|

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
|Type|nvarchar(1)|

### Lots_Issue

| Property | Value |
| - | - |
|Type|nvarchar(4)|

### Expiry_Period_Days

| Property | Value |
| - | - |
|Type|int|

### Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Allow_Variable_Measurement_Ratios

| Property | Value |
| - | - |
|Type|bit|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|

### Cargo_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|


