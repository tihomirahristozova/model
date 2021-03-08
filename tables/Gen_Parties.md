# Table Gen_Parties

Contains base data for different kind of parties - companies, persons, departments, etc. Entity: Gen_Parties

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Id|`Guid`|`PK`, Readonly|Gets the Id of the party row, related to the domain object |
|GLN|`String`||Global Location Number used by EDI systems. `Filter(multi eq)` `ORD` |
|Is_Active|`Boolean`||Specifies whether the current party is active in the system or not. `Required` `Default(true)` `Filter(eq)` |
|Party_Code|`String`|Readonly|The unique code of the party. `Required` `Filter(eq;like)` `ORD` `ReadOnly` |
|Creation_Time|`DateTime?`|Readonly|Date and time when the Party was created. `Filter(ge;le)` `ReadOnly` |
|Creation_User|`String`|Readonly|Login name of the user, who created the Party. `Filter(like)` `ReadOnly` |
|Party_Name|`MultilanguageString`||The name of the party. `Required` `Filter(eq;like)` `ORD` |
|Notes|`String`||Notes for this Party. |
|Party_Type|`PartyType`|Allowed: `C`, `L`, `P`, `S`, `V`|Type of party. Currently supported are P=Person, C=Company, S=Store, L=Company Location, V=Division. `Required` `Default("P")` `Filter(multi eq)` |
|Party_Unique_Number|`String`|Readonly|Unique number of the party (National number for persons, Registration number for companies). `Filter(eq;like)` `ReadOnly` |
|Update_Time|`DateTime?`|Readonly|Date and time when the Party was last updated. `Filter(ge;le)` `ReadOnly` |
|Update_User|`String`|Readonly|Login name of the user, who last updated the Party. `Filter(like)` `ReadOnly` |
