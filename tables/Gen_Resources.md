# Table Gen_Resources

Enterprise resources, categorized by groups. Entity: Gen_Resources

# Aggregate Hierarchy

* [Gen_Resource_Groups](Gen_Resource_Groups.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Resource_Id|`Guid`|`PK`, Readonly||
|Resource_Name|`MultilanguageString`||Resource name. Unique within the resource group. `Required` `Filter(eq;like)` |
|Notes|`String`||Notes for this Resource. |
