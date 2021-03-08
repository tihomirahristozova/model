# Table Prd_Work_Order_Items

The different items that are produced with a work order. Entity: Prd_Work_Order_Items

# Aggregate Hierarchy

* [Prd_Work_Orders](Prd_Work_Orders.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Id|`Guid`|`PK`, Readonly||
|Completion_Date|`DateTime?`||The date, when the item should be completed. null means that there is no constraint for completion date. |
|Line_Ord|`Int32`||The order of the line within the work order. `Required` `Filter(eq;like)` |
|Notes|`String`||Notes for this WorkOrderItem. |
|Parent_Line_Id|`Guid?`||If not null contains the Id of the line of the parent document, that created the current row. `Filter(multi eq)` |
|Parent_Line_No|`Int32?`||The number of the line within the parent document, which the current line executes. null when the current line does not execute another line. `Filter(eq)` |
|Priority|`Priority`|Allowed: `1`, `2`, `3`, `4`, `5`|Priority of the production of the item. Initially inherits the priority of the work order. 1=Lowest ... 5=Highest. `Required` `Default(3)` |
|Release_Date|`DateTime?`||The date, when the item is released to production. null means that still there is no plan when the item will be released to production. |
|Scheduled_End_Date_Time|`DateTime?`||Date and time when the production of this item is scheduled to end. |
|Scheduled_Start_Date_Time|`DateTime?`||Date and time when the production of this item is scheduled to begin. |
