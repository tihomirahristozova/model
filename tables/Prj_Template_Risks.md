# Table Prj_Template_Risks

Contains project risks, which will be copied to projects, based on the template. Entity: Prj_Template_Risks

# Aggregate Hierarchy

* [Prj_Templates](Prj_Templates.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Project_Template_Risk_Id|`Guid`|`PK`, Readonly||
|Description|`String`||The description of this TemplateRisk. |
|Impact_Percent|`Decimal`||The impact of the risk to the project, expressed as percentage of the total project value. `Required` `Default(0)` |
|Probability_Percent|`Decimal`||The probability of the risk occurring. `Required` `Default(0)` |
|Risk_Name|`String`||The name of the risk. `Required` |
