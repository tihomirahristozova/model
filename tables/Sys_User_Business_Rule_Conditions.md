# Table Sys_User_Business_Rule_Conditions

Represents one condition for the execution of a business rule. Entity: Sys_User_Business_Rule_Conditions

# Aggregate Hierarchy

* [Sys_User_Business_Rules](Sys_User_Business_Rules.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|User_Business_Rule_Condition_Id|`Guid`|`PK`, Readonly||
|Attribute_Name|`String`||The attribute, which will be tested. `Required` |
|Comparison_Type|`ComparisonType`|Allowed: `Equals`, `Greater_Than`, `Less_Than`, `Like`, `IsNull`, `Not_Equals`|How to compare the attribute and the value of the condition - e.g. Attribute-Comparison-Value. `Required` `Default("Equals")` |
|Condition_No|`Int32`||Unique consecutive number of the condition within the business rule. `Required` |
|Notes|`String`||Notes for this UserBusinessRuleCondition. `Introduced in version 20.1` |
|Value|`String`||The value against which the data attribute will be tested. |
