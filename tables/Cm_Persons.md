# Table Cm_Persons

Personal records. Requires related party record. Entity: Cm_Persons

# Inheritance

* [Gen_Parties](Gen_Parties.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Person_Id|`Guid`|`PK`, Readonly||
|Birth_Date|`DateTime?`||Birth date. null means unknown. `Filter(ge;le)` |
|City|`MultilanguageString`||City from the legal registration address for the person. `Filter(like)` |
|Creation_Time|`DateTime?`|Readonly|Date and time when the Person was created. `Filter(ge;le)` `ReadOnly` |
|Creation_User|`String`|Readonly|Login name of the user, who created the Person. `Filter(like)` `ReadOnly` |
|First_Name|`MultilanguageString`||First name of the person. `Filter(eq;like)` |
|Gender|`Gender?`|Allowed: `F`, `M`|Person gender. M=Male;F=Female;null=not known/not provided. `Filter(eq)` |
|GLN|`String`|||
|Is_Active|`Boolean`|||
|Last_Name|`MultilanguageString`||Last name of the person. `Filter(eq;like)` |
|Middle_Name|`MultilanguageString`||Middle name of the person. `Filter(eq;like)` |
|National_Number|`String`||Government assigned unique personal number. null means unknown. `Filter(eq;like)` |
|Notes|`String`||Internal notes for the person. |
|Party_Code|`String`|Readonly||
|Creation_Time|`DateTime?`|Readonly||
|Creation_User|`String`|Readonly||
|Party_Name|`MultilanguageString`|||
|Notes|`String`|||
|Party_Type|`PartyType`|Allowed: `C`, `L`, `P`, `S`, `V`||
|Party_Unique_Number|`String`|Readonly||
|Update_Time|`DateTime?`|Readonly||
|Update_User|`String`|Readonly||
|Passport_Issuing_Date|`DateTime?`||Date of issuing the passport. null means unknown. `Filter(ge;le)` |
|Passport_Number|`String`||Current passport number. null means unknown. `Filter(eq)` |
|Title|`MultilanguageString`||The persons title. It may be one of the standard titles - Mr., Mrs., etc., but it can also contains professional or academic qualification. |
|Update_Time|`DateTime?`|Readonly|Date and time when the Person was last updated. `Filter(ge;le)` `ReadOnly` |
|Update_User|`String`|Readonly|Login name of the user, who last updated the Person. `Filter(like)` `ReadOnly` |
