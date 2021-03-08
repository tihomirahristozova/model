# Table Inv_Requisition_Plan

The current requisition (MRP) plan. The data is deleted and re-created upon each planning. Entity: Inv_Requisition_Plan

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Requisition_Plan_Item_Id|`Guid`|`PK`, Readonly||
|Calendar_Date|`DateTime`||The date for which we are planning. A record is created for each calendar date, on which there are events (orders, executions, planned events, etc.) for the product. Past events are stored on the current date of the planning. `Required` `Filter(ge;le)` |
|Completion_Date|`DateTime?`||The suggested by the program value equals Calendar_Date + Planning_Lead_Time_Days of the default product supply for this store; the completion date of the purchase orders to be generated. |
|Confirm_Action|`Boolean`||True - generate firm planned orders for the current row; false- do not generate;. `Required` `Default(false)` `Filter(eq)` |
|Explanation_Message|`String`||A message that explains why the program has generated the planned orders for this row. |
|Generation_Date|`DateTime`||Indicates the date on which the plan is generated. `Required` `Default(Now)` |
|Release_Date|`DateTime?`||The suggested by the program value equals Calendar_Date; the release date of the purchase orders to be generated. |
