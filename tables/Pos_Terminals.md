# Table Pos_Terminals

Represents a POS workplace for 1 person, with all the attached devices. (Not to be confused with Payment Terminal, which is specific POS device). Entity: Pos_Terminals (Introduced in version 19.1)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Pos_Terminal_Id|`Guid`|`PK`, Readonly||
|Is_Active|`Boolean`||Represents whether the POS terminal is active and can be chosen from drop-downs for new records. `Required` `Default(true)` `Filter(multi eq)` |
|Pos_Terminal_Code|`String`||Unique (within the location) code of the POS terminal. `Required` `Filter(eq;like)` |
|Pos_Terminal_Name|`MultilanguageString`||The multi-language name of the terminal, like "Cash 1", "Self-checkout 5", etc. `Required` `Filter(multi eq;like)` |
