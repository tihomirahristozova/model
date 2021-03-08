# Table Cm_Company_Locations

Stores company locations. The locations are parties and as such, can be organized hierarchically mixed with other structuring mechanisms. The locations, departments and divisions are parallel and different structuring mechanisms for the companies. Entity: Cm_Company_Locations

# Inheritance

* [Gen_Parties](Gen_Parties.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Company_Location_Id|`Guid`|`PK`, Readonly||
|Bill_To|`BillTo?`|Allowed: `C`, `L`|If filled indicates which party is billed for the amounts from documents that require payments. This setting is used in CRM module when the company and the location are customers. Possible values: 'C' = Company, 'L' = Company location, null = unidentified. |
|GLN|`String`|||
|Is_Active|`Boolean`|||
|Location_Name|`MultilanguageString`||The name of the company location. `Required` `Filter(eq;like)` |
|Party_Code|`String`|Readonly||
|Creation_Time|`DateTime?`|Readonly||
|Creation_User|`String`|Readonly||
|Party_Name|`MultilanguageString`|||
|Notes|`String`|||
|Party_Type|`PartyType`|Allowed: `C`, `L`, `P`, `S`, `V`||
|Party_Unique_Number|`String`|Readonly||
|Update_Time|`DateTime?`|Readonly||
|Update_User|`String`|Readonly||
|Working_Time|`String`||Textual representation of the working time of the location. |
