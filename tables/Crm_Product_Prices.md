# Table Crm_Product_Prices

Specific prices of products. A price is applied after matching the specified criteria. Entity: Crm_Product_Prices

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Product_Price_Id|`Guid`|`PK`, Readonly||
|From_Date|`DateTime?`||Starting date of validity of the price. `Filter(eq;ge;le)` |
|Notes|`String`||Notes for this ProductPrice. |
|Priority|`Priority`|Allowed: `1`, `2`, `3`, `4`, `5`|Priority of the price comparative to other prices. Only the highest priority price is applied. `Required` `Default(2)` `Filter(multi eq)` |
|Thru_Date|`DateTime?`||Ending date (inclusive) of the validity of the price. `Filter(eq;ge;le)` |
