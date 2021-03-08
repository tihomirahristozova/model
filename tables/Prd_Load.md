# Table Prd_Load

Contains scheduled operations usage of the resources. Entity: Prd_Load

# Aggregate Hierarchy

* [Prd_Work_Order_Item_Operations](Prd_Work_Order_Item_Operations.md)
* [Prd_Work_Order_Items](Prd_Work_Order_Items.md)
* [Prd_Work_Orders](Prd_Work_Orders.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Id|`Guid`|`PK`, Readonly||
|Calendar_Date|`DateTime`||Date of the scheduled load. This is date only. Start_Time and End_Time specify time of day. `Required` `Filter(ge;le)` |
|Priority|`Priority`|Allowed: `1`, `2`, `3`, `4`, `5`|Priority of the allocation. 1=Lowest ... 5=Highest. `Required` `Default(3)` |
|Time_Type|`TimeType`|Allowed: `M`, `R`, `S`, `W`|S=Setup; R=Run; W=Wait; M=Move. `Required` `Default("R")` |
|Usage_End_Time|`DateTime`||The ending time of the planned usage. `Required` `Filter(ge;le)` |
|Usage_Start_Time|`DateTime`||The starting time of the planned usage. `Required` `Filter(ge;le)` |
|Usage_Time_Minutes|`Int32`||Time allocated for the operation in minutes. `Required` `Default(0)` `Filter(ge;le)` |
