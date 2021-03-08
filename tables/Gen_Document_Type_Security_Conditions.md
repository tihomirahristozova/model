# Table Gen_Document_Type_Security_Conditions

Provides rules to conditionally secure new documents. Entity: Gen_Document_Type_Security_Conditions

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Document_Type_Security_Condition_Id|`Guid`|`PK`, Readonly||
|Condition_Filter_Xml|`DataAccessFilter`||Specifies the documents, for which the current rule is applicable. The XML filter is compared against new documents and the rule is applicable when they match. `Required` |
|Description|`String`||The description of this DocumentTypeSecurityCondition. `Required` `Filter(eq;like)` |
|Priority|`Priority`|Allowed: `1`, `2`, `3`, `4`, `5`|Priority of the rule against other rules, which are also applicable. Only the highest priority rule is selected. `Required` `Default(3)` `Filter(ge;le)` |
