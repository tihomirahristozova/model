# Table Pos_Operators

Represents one operator (person) in one POS location. Entity: Pos_Operators (Introduced in version 19.1)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Pos_Operator_Id|`Guid`|`PK`, Readonly||
|Is_Active|`Boolean`||Indicates whether this operator is active and can be chosen for new records. `Required` `Default(true)` `Filter(multi eq)` |
|Pos_Operator_Code|`String`||Operator code. Unique within the Pos Location. `Required` `Filter(multi eq;like)` `ORD` |
|Starting_Date|`DateTime`||The first date, when the operator has started working for this POS location. `Required` `Filter(multi eq;ge;le)` |
|Termination_Date|`DateTime?`||The date, when the operator has ceased working in this POS location. null means, that the operator is still working or the termination date is still unknown. `Filter(multi eq;ge;le)` |
