# Table Prd_Work_Order_Item_Operations

The operations that are performed to produce the product. Entity: Prd_Work_Order_Item_Operations

# Aggregate Hierarchy

* [Prd_Work_Order_Items](Prd_Work_Order_Items.md)
* [Prd_Work_Orders](Prd_Work_Orders.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Id|`Guid`|`PK`, Readonly||
|Actual_End_Date_Time|`DateTime?`||The date/time when the operation has completed. null means that the operation is not completed. |
|Actual_Start_Date_Time|`DateTime?`||The date/time when the operation has started. null means that the has not started yet. |
|Line_Ord|`Int32`||Order of the line within the work order routing. `Required` `Filter(eq;like)` |
|Minimum_Concurrent_Start_Time_Minutes|`Int32?`||How many minutes after the start of this operation can the next operation start. null means that the next operation should wait this operation to finish before starting. |
|Move_Time_Minutes|`Int32`||Time to move the lot to the next operation in minutes. `Required` `Default(0)` |
|Notes|`String`||Notes for this WorkOrderItemOperation. |
|Operation_Description|`String`||The short description of the operation. |
|Run_Time_Minutes|`Int32`||Time for production of one lot of the produced item in minutes. `Required` `Default(0)` |
|Scheduled_End_Date_Time|`DateTime?`||The date/time when the operation is scheduled to complete. null means that there is still no plan when the operation will finish (for new orders only). |
|Scheduled_Start_Date_Time|`DateTime?`||The date/time when the operation is planned to start. null means that there is still no plan when to start the operaion (only for new work orders). |
|Scrap_Rate|`Decimal`||Projected scrap rate of the operation. `Required` `Default(0)` |
|Setup_Time_Minutes|`Int32`||Time needed to setup the equipment in minutes. `Required` `Default(0)` |
|Tooling|`String`||The tools needed for the routing step. |
|Wait_Time_Minutes|`Int32`||Wait time (drying, cooling, etc.) after the operation in minutes. `Required` `Default(0)` |
