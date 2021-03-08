# Table Log_Logistic_Unit_Types

Types of logistic units, like EU-PALLET, 40x40 pallet, ISO container, etc. Entity: Log_Logistic_Unit_Types (Introduced in version 21.1.0.77)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Logistic_Unit_Type_Id|`Guid`|`PK`, Readonly||
|Code|`String`||Unique code of the logistic unit type. Used for display and selection purposes. Can contain only EN letters and numbers. `Required` `Filter(multi eq;like)` |
|Name|`MultilanguageString`||Multi-language name of the logistic unit type. `Required` `Filter(eq;like)` |
|Notes|`String`||Notes for this LogisticUnitType. `Filter(like)` |
