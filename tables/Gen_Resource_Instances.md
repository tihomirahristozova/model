# Table Gen_Resource_Instances

Represents concrete instances of resources. Entity: Gen_Resource_Instances

# Aggregate Hierarchy

* [Gen_Resources](Gen_Resources.md)
* [Gen_Resource_Groups](Gen_Resource_Groups.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Resource_Instance_Id|`Guid`|`PK`, Readonly||
|Resource_Instance_Code|`String`||Code of the instance, unique within the resource. `Required` `Filter(eq;like)` |
|Resource_Instance_Name|`String`||Multilanguage resource instance name. `Required` `Filter(eq;like)` |
|Notes|`String`||Notes for this ResourceInstance. |
