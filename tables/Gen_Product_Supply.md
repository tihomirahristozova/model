# Table Gen_Product_Supply

Contains supply rules, which are used by the procurement planning system. Entity: Gen_Product_Supply

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Product_Supply_Id|`Guid`|`PK`, Readonly||
|Buyer_Name|`String`||The code or name of the person, who is in charge for purchasing the product from external suppliers. It is used to group different products on purchase demand report. null when Procurement_Type is not buy. |
|Is_Active|`Boolean`||True if this product supply is active. `Required` `Default(true)` `Filter(eq)` |
|Is_Default|`Boolean`||Specifies whether this is the default supply rule. The planning system works using *only* the default supply rules. The other rules are for reference and user information. `Required` `Default(true)` `Filter(eq)` |
|Manufacturing_Policy|`ManufacturingPolicy`|Allowed: `ATO`, `MTO`, `MTS`, `ETO`|MTS=Make-To-Stock; MTO=Make-To-Order; ATO=Assemble-To-Order;ETO=Engineer-To-Order. `Required` `Default("MTS")` |
|Order_Lot_Sizing_Method|`OrderLotSizingMethod`|Allowed: `EOQ`, `FOQ`, `LFL`, `LFP`, `ROP`, `ROT`|LFL=Lot for Lot; FOQ=Fixed order quantity; EOQ=Eqonomic Order Quantity; ROP=ReOrder Point; ROT=ReOrder point with Time planning; LFP = Lot For Period;. `Required` `Default("ROP")` |
|Order_Multiple|`Boolean`||True if the order qty should be multiple of lot size when buying or making. `Required` `Default(false)` |
|Order_Period_Planning_Days|`Int32?`||For how many days in the future should be planned - for fixed period replenishment system. null - not yet specified. |
|Order_Period_Start_Date|`DateTime?`||Start date of the first period under fixed period replenishment system. null - not yet specified. |
|Order_Policy|`OrderPolicy`|Allowed: `MRP`, `OPS`, `OPT`, `PRS`|Order policy/replenishment system. OPS=Order Point System; OPT=Order Point System with Time planning; PRS=Periodic Review System/Periods Of Supply; MRP = Material Requirements Planning. `Required` `Default("OPS")` |
|Planning_Annual_Carrying_Cost_Percent|`Decimal?`||The expected carrying cost as percentage of inventory cost. null means unknown. |
|Planning_Horizon_Days|`Int32`||Number of days in the future for which to plan the demand and supply. `Required` `Default(0)` |
|Planning_Lead_Time_Days|`Int32`||The number of days required to supply or manufacture the product. The number is exclusive of the lead-time of lower-level components. `Required` `Default(0)` |
|Planning_Order_Cycle_Days|`Int32?`||Number of days in one period under fixed period replenishment system. null - not yet specified. |
|Planning_Time_Fence_Days|`Int32`||Period in the future inside of which changes to the MPS are carefully evaluated to prevent costly schedule disruption. Demand for the period between DTF and PTF is calculated as the bigger of customer orders and sales forecast. Abbr. - PTF. `Required` `Default(1)` |
|Procurement_Type|`ProcurementType`|Allowed: `B`, `M`, `T`|M=Make; B=Buy; T=Transfer.  Identifies whether the product is produced or externally bought. `Required` `Default("B")` |
|Supply_Schema_Id|`Guid?`||The supply schema to use for the distribution of the product among warehouses. `Filter(multi eq)` |
