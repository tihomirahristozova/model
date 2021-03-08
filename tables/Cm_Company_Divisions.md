# Table Cm_Company_Divisions

Stores company divisions structure. The divisions are parties and as such, can be organized hierarchically mixed with other structuring mechanisms. The departments and divisions are parallel and different structuring mechanisms for the companies. Entity: Cm_Company_Divisions

# Inheritance

* [Gen_Parties](Gen_Parties.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Company_Division_Id|`Guid`|`PK`, Readonly||
|Company_Division_Code|`String`||Company division code, unique within the company. `Required` `Filter(eq;like)` |
|GLN|`String`|||
|Is_Active|`Boolean`|||
|Company_Division_Name|`MultilanguageString`||Multi-language company divsion name. `Required` `Filter(eq;like)` |
|Party_Code|`String`|Readonly||
|Creation_Time|`DateTime?`|Readonly||
|Creation_User|`String`|Readonly||
|Party_Name|`MultilanguageString`|||
|Notes|`String`|||
|Party_Type|`PartyType`|Allowed: `C`, `L`, `P`, `S`, `V`||
|Party_Unique_Number|`String`|Readonly||
|Update_Time|`DateTime?`|Readonly||
|Update_User|`String`|Readonly||
