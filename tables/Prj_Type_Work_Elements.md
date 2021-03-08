# Table Prj_Type_Work_Elements

The work elements of the work breakdown structure of each project type. Entity: Prj_Type_Work_Elements

# Aggregate Hierarchy

* [Prj_Types](Prj_Types.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Project_Type_Work_Element_Id|`Guid`|`PK`, Readonly||
|Full_Path|`String`|Readonly|The full path of the node in the format of dot-delimited, dot-terminated codes of the parents. `Filter(eq;like)` `ReadOnly` |
|Notes|`String`||Notes for this TypeWorkElement. |
|Parent_Full_Path|`String`||The full path of the parent work element in this project type. null when this is root element. `Filter(eq;like)` |
|Work_Element_Code|`String`||The code of the work element, unique among the sibling elements within the parent work element. `Required` `Filter(eq)` |
|Work_Element_Name|`String`||The name of the work element, unique among the sibling elements within the parent work element. `Required` `Filter(eq)` |
