# Table Prj_Type_Roles

Contains the roles of the participants of each project type. Entity: Prj_Type_Roles

# Aggregate Hierarchy

* [Prj_Types](Prj_Types.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Project_Type_Role_Id|`Guid`|`PK`, Readonly||
|Description|`String`||Description of the participant role. |
|Role_Name|`String`||The name of the participant role. `Required` `Filter(multi eq;like)` |
