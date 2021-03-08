# Table Prj_Task_Types

Represents the different types of tasks, which can be included in the projects. Entity: Prj_Task_Types

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Task_Type_Id|`Guid`|`PK`, Readonly||
|Description|`MultilanguageString`||Multilanguage description of the task type. |
|Display_Order|`Int32`||Display order position of the task. Lowest numbers are shown first (on top). `Required` `Default(1)` |
|Icon|`Byte[]`|`BLOB`|Icon representing the task type. Preferrably 32x32 pixels. |
|Task_Type_Name|`MultilanguageString`||The multilanguage task type name. `Required` `Filter(multi eq;like)` |
