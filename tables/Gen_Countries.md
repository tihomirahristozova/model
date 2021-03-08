# Table Gen_Countries

List of countries, listed by their internet suffix code. Entity: Gen_Countries

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Country_Id|`Guid`|`PK`, Readonly||
|Code|`String`||Internet suffix code of the country. `Required` `Filter(eq;like)` `ORD` |
|Intrastat_Code|`String`||This code is used when creating the Intrastat Declaration. If the field is empty, then the value from the 'Code' field is used. `Introduced in version 20.1` |
|Country_Name|`MultilanguageString`||Name of the country. `Required` `Filter(like)` |
