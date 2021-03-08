# Table Prj_Project_Risks

Contains risks, associated to projects. Entity: Prj_Project_Risks

# Aggregate Hierarchy

* [Prj_Projects](Prj_Projects.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Project_Risk_Id|`Guid`|`PK`, Readonly||
|Create_Date|`DateTime`||The creation date of the project risk. `Required` `Default(Now)` `Filter(eq)` |
|Description|`String`||The description of this ProjectRisk. `Filter(like)` |
|Impact_Percent|`Decimal`||The impact of the risk to the project, expressed as percentage of the total project value. `Required` `Default(0)` |
|Probability_Percent|`Decimal`||The probability of the risk occurring. `Required` `Default(0)` |
|Resolution_Strategy|`String`||The strategy chosen to handle the risk. `Filter(eq)` |
|Resolved|`Boolean`||True if the risk is resolved. `Required` `Default(false)` `Filter(eq)` |
|Resolve_Date|`DateTime?`||The date on which the risk is resolved. `Filter(eq)` |
|Risk_Name|`String`||The short name of the risk. `Required` `Filter(multi eq)` |
