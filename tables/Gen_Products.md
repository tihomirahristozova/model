# Table Gen_Products

Products are the different items in the enterprise, which can be purchased, stored, sold and depreciated. Entity: Gen_Products

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Id|`Guid`|`PK`, Readonly||
|ABC_Class|`ABCClass`|Allowed: `A `, `B `, `C `|Product importance classification, where A are the most important and C - the least important products. Usually used as user filtering condition when previewing results of the procurement planning process. `Required` `Default("B ")` `Filter(eq)` |
|Active|`Boolean`||True if the product is active, false - not to list in combo boxes for choosing in new documents. `Required` `Default(true)` `Filter(eq)` |
|Allow_Variable_Measurement_Ratios|`Boolean`||Allow variable (dynamic) measurement ratios for each transaction. If specified, each store transaction could specify different measurement ratio between the used measurement unit and the base measurement unit. `Required` `Default(false)` `Filter(eq)` |
|Catalog_Description_Html|`String`||Full HTML description of the product. Usually used for display on product catalogs, web pages, etc. |
|Costing_Method|`CostingMethod?`|Allowed: `AVG`, `EXP`, `BLD`|Specifies the costing method for the product. null means to use the Enterprise Company default. Currently supported methods are: EXP - Explicitly specify lot; AVG - Average cost. |
|Creation_Time|`DateTime?`|Readonly|Date and time when the Product was created. `Filter(ge;le)` `ReadOnly` |
|Creation_User|`String`|Readonly|Login name of the user, who created the Product. `Filter(like)` `ReadOnly` |
|Description|`MultilanguageString`||The description of the product. |
|Expiry_Period_Days|`Int32?`||Total default expiry period for the product (in days) from the date of production to the date of expiry. |
|Flushing_Method|`FlushingMethod`|Allowed: `B`, `F`, `M`|Consumption method for work orders. M=Manual, using Consuption Journals, F=Forward (on release), B=Backward (on finish). `Required` `Default("M")` |
|Guarantee_Period_Days|`Int32?`||Default guarantee period length in days. 0 means no guarantee. Should be non-null for serviced products and null for the others. |
|Is_Featured|`Boolean`||Specifies whether the product should be presented at the title space in promotional materials, web pages, etc. `Required` `Default(false)` `Filter(eq)` |
|Is_Serialized|`Boolean`||True if the parts use/require serial numbers. `Required` `Default(false)` `Filter(eq)` |
|Lots_Issue|`LotsIssue?`|Allowed: `FIFO`, `FEFO`, `LIFO`|Determines the method by which the lots are automatically issued. The method determines the sequence of the lots: in the order of receipt (FIFO), in the order inverse of receipt (LIFO) or in the order of expiration (FEFO). |
|Manufacturing_Policy|`String`||Manufacturing policy controls the procurement planing system actions for this product. Allowed values are MTS=Make-To-Stock; MTO=Make-To-Order; ATO=Assemble-To-Order. `Required` `Default("MTS")` |
|Minimal_Sales_Quantity_Base|`Decimal?`||Minimal base quantity of this product that has to be specified in any sale. |
|Product_Name|`MultilanguageString`||Name of the item. `Required` `Filter(eq;like)` |
|Part_Number|`String`||Unique part number of the product. `Required` `Filter(multi eq;like)` `ORD` |
|Planning_Demand_Time_Fence_Days|`Int32?`||Period in the future, in which changes to the MPS are not accepted due to the high cost of changing. Demand for the period is calculated based entirely on the customer orders. Abbr. - DTF (null = Default of 30 days). |
|Planning_Horizon_Days|`Int32?`||Number of days in the future for which to plan the demand and supply (null = Default of 180 days). |
|Planning_Time_Fence_Days|`Int32?`||Period in the future inside of which changes to the MPS are carefully evaluated to prevent costly schedule disruption. Demand for the period between DTF and PTF is calculated as the bigger of customer orders and sales forecast. Abbr. - PTF. (null = Default of 90 days). |
|Scrap_Rate|`Decimal`||Default scrap rate for the recipe, when this product is used as ingredient. `Required` `Default(0)` |
|Short_Name|`MultilanguageString`||Short name of the product. Used for space-constrained devices, like mobile phones, fiscal printers, etc. `Filter(eq;like)` |
|Show_In_Catalog|`Boolean`||Specifies whether to show the product in catalogs, referring to the product group of the product. false=Do not show; true=Show. `Required` `Default(false)` `Filter(multi eq)` |
|Supply_Schema_Id|`Guid?`||The supply schema to use for the distribution of the product among warehouses. `Filter(multi eq)` |
|Update_Time|`DateTime?`|Readonly|Date and time when the Product was last updated. `Filter(ge;le)` `ReadOnly` |
|Update_User|`String`|Readonly|Login name of the user, who last updated the Product. `Filter(like)` `ReadOnly` |
|Use_Lots|`UseLots`|Allowed: `A`, `N`, `R`|Specifies whether the use of lots for this product in store documents is required or is unallowed or is allowed while not required. `Required` `Default("A")` |
