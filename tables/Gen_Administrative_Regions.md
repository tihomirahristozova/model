# Table Gen_Administrative_Regions

Hierarchical structure of the legally defined administrative regions. Administrative regions are sub-divisions of the countries. Entity: Gen_Administrative_Regions

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Administrative_Region_Id|`Guid`|`PK`, Readonly||
|Administrative_Region_Code|`String`||Administrative code of country territorial subdivision. `Required` `Filter(eq;like)` |
|Full_Path|`String`||Full identification path of the current country territorial subdivision. `Filter(eq;like)` |
|Administrative_Region_Name|`MultilanguageString`||Name of country territorial subdivision. `Required` `Filter(like)` |
|Parent_Full_Path|`String`||Parent region of the current territorial subdivision. `Filter(eq;like)` |
|Valid_From|`DateTime?`||Start date of validity of this administrative division. null when the starting date is unknown in the past. `Filter(ge;le)` |
|Valid_To|`DateTime?`||End date of validity of this administative division. null when the division is still active or ending date is unknown. `Filter(ge;le)` |
