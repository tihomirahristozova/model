# Table Its_Declaration_Lines

Contains the details of the Intrastat declarations, issued by the enterprise companies. Entity: Its_Declaration_Lines

# Aggregate Hierarchy

* [Its_Declarations](Its_Declarations.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Intrastat_Declaration_Line_Id|`Guid`|`PK`, Readonly||
|Delivery_Terms|`DeliveryTerms`|Allowed: `EXW`, `FCA`, `FAS`, `FOB`, `CFR`, `CIF`, `CPT`, `CIP`, `DAP`, `DAT`, `DDP`, `DPU`|Delivery terms - classification according to Intrastat (which uses the common abbreviations). `Required` |
|Line_Action|`LineAction`|Allowed: `NEW`, `EDN`, `EDO`, `DEL`|Line action - 'NEW' = New, 'EDN' = Edited-New, 'EDO' = Edited-Old, 'DEL' = Deleted. `Required` `Default("NEW")` |
|Line_No|`Int32`||Consequtive line number within the intrastat declaration. `Required` `Filter(eq)` |
|Net_Mass_Kg|`Decimal`||Net mass of the goods in kg. `Required` `Filter(multi eq)` |
|Quantity_Supplementary_Unit|`Decimal?`||Quantity of the goods in the supplementary unit. null when no supplementary unit is specified. |
|Transaction_Nature|`TransactionNature`|Allowed: `11`, `12`, `13`, `14`, `19`, `21`, `22`, `23`, `29`, `60`, `70`, `80`, `91`, `99`, `30`, `41`, `42`, `51`, `52`|Transaction nature, according to the Intrastat classification. `Required` |
|Transport_Mode|`TransportMode`|Allowed: `1`, `2`, `3`, `4`, `5`, `7`, `8`, `9`|Transportation mode - type of transportation used. `Required` |
