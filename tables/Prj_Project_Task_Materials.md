# Table Prj_Project_Task_Materials

Contains the materials, which are required for a project task. Entity: Prj_Project_Task_Materials

# Aggregate Hierarchy

* [Prj_Project_Tasks](Prj_Project_Tasks.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Project_Task_Material_Id|`Guid`|`PK`, Readonly||
|Line_Number|`Int32`||Line number within the task, increased in steps of 10. Used for sorting purposes. `Required` `Default(0)` |
|Quantity_Base|`Decimal`|Readonly|The equivalence of Quantity in the base measurement unit of the Material. `Required` `Default(0)` `ReadOnly` |
