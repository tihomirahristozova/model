# Table Sys_User_Business_Rules

Represents user-defined business rule. Entity: Sys_User_Business_Rules

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|User_Business_Rule_Id|`Guid`|`PK`, Readonly||
|User_Business_Rule_Code|`String`||The unique code of the UserBusinessRule. `Required` `Filter(eq;like)` `ORD` |
|Icon|`Byte[]`|`BLOB`|Visual icon of the rule in .PNG format. |
|Is_Active|`Boolean`||Specifies whether the rule is activated. `Required` `Default(false)` `Filter(eq)` |
|Layer|`Layer`|Allowed: `FTE`, `BKE`, `COM`|Specifies in which layers the rule will be available. The available events and actions depend on the chosen layer.  Allowed values: FTE=Front-End, BKE=BackEnd, COM=Common (both). `Required` `Default("BKE")` `Filter(multi eq)` |
|User_Business_Rule_Name|`MultilanguageString`||The name of this UserBusinessRule. `Required` `Filter(like)` |
|Notes|`String`||Notes for this UserBusinessRule. |
|Repository_Name|`String`||The name of the repository, for which this business rule is defined. `Required` `Filter(eq;like)` |
|Script_Language|`ScriptLanguage`|Allowed: `Integrated`, `CSharp`|The programming language used to define the rule actions. `Required` `Default("Integrated")` |
|Script_Text|`String`||The program code used to define the rule actions. |
|User_Startable|`Boolean`||Specifies, that the rule can be manually started by the user. `Default(false)` `Filter(eq)` |
