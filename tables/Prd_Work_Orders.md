# Table Prd_Work_Orders

Scheduled and released production orders. Each order can contain the production of many items. Entity: Prd_Work_Orders

# Inheritance

* [Gen_Documents](Gen_Documents.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Id|`Guid`|`PK`, Readonly||
|Adjustment_Number|`Int32`|Readonly||
|Adjustment_Time|`DateTime?`|Readonly||
|Adjustment_User|`String`|Readonly||
|Complete_Time|`DateTime?`|Readonly||
|Completion_Date|`DateTime?`||Scheduled date of completion. Specifies the date when the workorder was completed. null means that the order is not yet completed. |
|Creation_Time|`DateTime`|Readonly||
|Creation_User|`String`|Readonly||
|Document_Date|`DateTime`|||
|Document_No|`String`|||
|Notes|`String`|||
|Document_Version|`Int32`|Readonly||
|Due_Date|`DateTime?`||The final due date, when the production should be ready. |
|Duration_Hour|`Decimal`||The duration of all operations in the protocol either planned (for planned orders) or actual (for completed orders). `Required` `Default(0)` |
|Entity_Name|`String`|Readonly||
|Is_Released|`Boolean`|Readonly|True if the document is not void and its state is released or greater. `Required` `Default(false)` `Filter(eq)` `ReadOnly` |
|Is_Single_Execution|`Boolean`|Readonly|Specifies whether the document is a single execution of its order document. `Required` `Default(false)` `Filter(eq)` `ReadOnly` |
|Notes|`String`||User notes for the production order. |
|Parent_Document_Relationship_Type|`ParentDocumentRelationshipType?`|Allowed: `S`, `N`, Readonly||
|Planning_Only|`Boolean`|Readonly||
|Priority|`Priority`|Allowed: `1`, `2`, `3`, `4`, `5`|Priority of the work order. Higher priority orders might seize resources from lower priority orders. 1=Lowest priority ... 5=Highest. `Required` `Default(3)` `Filter(ge;le)` |
|Read_Only|`Boolean`|Readonly||
|Reference_Date|`DateTime?`|||
|Reference_Document_No|`String`|||
|Release_Date|`DateTime?`||Scheduled release date. Specifies the date when the order is planned/released to production. null means that still there is no plan for releasing the order. |
|Release_Time|`DateTime?`|Readonly||
|State|`DocumentState`|Allowed: `0`, `5`, `10`, `20`, `30`, `40`, `50`, Readonly||
|Void|`Boolean`|Readonly||
|Void_Reason|`String`|Readonly||
|Void_Time|`DateTime?`|Readonly||
|Void_User|`String`|Readonly||
