# Table Scm_Purchase_Price_Lists

Contains purchase price list headers. Entity: Scm_Purchase_Price_Lists

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Purchase_Price_List_Id|`Guid`|`PK`, Readonly||
|From_Date|`DateTime?`||Starting validity of the price list. `Filter(eq;ge;le)` |
|Purchase_Price_List_Name|`String`||The name of this PurchasePriceList. `Required` `Filter(eq;like)` `ORD` |
|Thru_Date|`DateTime?`||Ending validity of the price list. `Filter(eq;ge;le)` |
