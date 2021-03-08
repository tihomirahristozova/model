# Table Cm_Companies

Contains company definitions. Entity: Cm_Companies

# Inheritance

* [Gen_Parties](Gen_Parties.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Company_Id|`Guid`|`PK`, Readonly||
|Branch_Number|`Int32`||Branch number of the company. Companies with equal names and/or registration numbers can be inserted only if their branch numbers are different. `Required` `Default(0)` `Filter(eq)` |
|City|`MultilanguageString`||The city in which the company is registered. `Filter(like)` |
|Creation_Time|`DateTime?`|Readonly|Date and time when the Company was created. `Filter(ge;le)` `ReadOnly` |
|Creation_User|`String`|Readonly|Login name of the user, who created the Company. `Filter(like)` `ReadOnly` |
|GLN|`String`|||
|Is_Active|`Boolean`|||
|Is_VAT_Cash_Reporting_Registered|`Boolean`||When true, specifies that the company uses the special VAT Cash Reporting Mode. `Required` `Default(false)` |
|Is_VAT_Registered|`Boolean`||Determines wheather the company is included in VAT registers. `Required` `Default(false)` |
|Company_Name|`MultilanguageString`||The name of this Company. `Filter(eq;like)` `ORD` |
|Party_Code|`String`|Readonly||
|Creation_Time|`DateTime?`|Readonly||
|Creation_User|`String`|Readonly||
|Party_Name|`MultilanguageString`|||
|Notes|`String`|||
|Party_Type|`PartyType`|Allowed: `C`, `L`, `P`, `S`, `V`||
|Party_Unique_Number|`String`|Readonly||
|Update_Time|`DateTime?`|Readonly||
|Update_User|`String`|Readonly||
|Registration_Number|`String`||Unique, government-assigned registration number. null means unknown. `Filter(eq;like)` `ORD` |
|Registration_Primary_Address|`MultilanguageString`||The primary registration address of the company. `Filter(like)` |
|Registration_Type|`MultilanguageString`||Legal registration type - like LTD., PLC, etc. null means unknown. `Filter(eq)` |
|Registration_VAT_Number|`String`||VAT registration number where applicable. null means that VAT number is not applicable or unknown. `Filter(eq)` `ORD` |
|Responsible_Person_Name|`MultilanguageString`||Primary responsible person of the company. null means unknown. `Filter(like)` |
|Update_Time|`DateTime?`|Readonly|Date and time when the Company was last updated. `Filter(ge;le)` `ReadOnly` |
|Update_User|`String`|Readonly|Login name of the user, who last updated the Company. `Filter(like)` `ReadOnly` |
