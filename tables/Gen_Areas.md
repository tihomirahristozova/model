# Table Gen_Areas

Areas are user-defined division of the sales territories. Entity: Gen_Areas

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Area_Id|`Guid`|`PK`, Readonly||
|Area_Code|`String`||The unique code of the Area. `Required` `Filter(eq;like)` `ORD` |
|Full_Path|`String`|Readonly|Full path to the area, starting with '/' and containing the area codes of all parent areas using '/' as separator and terminator. For example root area with code 'BG' would have full path = '/BG/'. `Filter(eq;like)` `ReadOnly` |
|Area_Name|`MultilanguageString`||The name of this Area. `Required` `Filter(eq;like)` `ORD` |
