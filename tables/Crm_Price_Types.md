# Table Crm_Price_Types

Price types. Entity: Crm_Price_Types

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Price_Type_Id|`Guid`|`PK`, Readonly||
|Price_Type_Code|`String`||Short identification code of the price type. `Required` `Filter(eq)` `ORD` |
|Price_Type_Name|`String`||Full name of the price type. `Required` `Filter(eq;like)` |
|Notes|`String`||Notes for this PriceType. |
|Ordinal_Pos|`Int32`||Priority position of the price type, with respect to the other price types. `Required` `ORD` |
