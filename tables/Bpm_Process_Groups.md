# Table Bpm_Process_Groups

Represents a node in the hierarchy of process groups. Entity: Bpm_Process_Groups

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Process_Group_Id|`Guid`|`PK`, Readonly||
|Process_Group_Code|`String`||Group code, unique within the parent group. `Required` `Filter(eq;like)` |
|Process_Group_Name|`MultilanguageString`||Multilanguage process group name. `Required` `Filter(eq;like)` |
|Notes|`String`||Notes for this ProcessGroup. |
