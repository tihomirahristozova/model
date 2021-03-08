# Table Crm_Price_Lists

Price Lists are used to manage multiple price records, assign to customers, etc. Entity: Crm_Price_Lists

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Price_List_Id|`Guid`|`PK`, Readonly||
|Description|`String`||The description of this PriceList. |
|From_Date|`DateTime?`||Starting validity of the price list. `Filter(eq;ge;le)` |
|Price_List_Name|`String`||The name of this PriceList. `Required` `Filter(eq;like)` `ORD` |
|Thru_Date|`DateTime?`||Ending validity of the price list. `Filter(eq;ge;le)` |
