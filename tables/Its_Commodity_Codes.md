# Table Its_Commodity_Codes

Contains the approved Intrastat commodity codes for each period. Entity: Its_Commodity_Codes

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Intrastat_Commodity_Code_Id|`Guid`|`PK`, Readonly||
|Commodity_Code|`String`||Product code from the Intrastat Combined nomenclature. `Required` `Filter(eq;like)` `ORD` |
|Description|`MultilanguageString`||Description of the product code from the Intrastat Combined nomenclature. `Required` `Filter(like)` |
|Supplementary_Unit|`String`||If not null, the related product should have additional measurement unit with the same code as specified in this field. The additional unit will be used for the purposes of the Intrastat declarations. `Required` |
|Valid_From|`DateTime?`||The starting date of validity of this code. `Filter(ge;le)` |
|Valid_To|`DateTime?`||The ending date of validity of this code. `Filter(ge;le)` |
