# Table Scm_Purchase_Product_Prices

Contains purchase prices of the products. Used for automatically loading unit prices in the purchase documents. Entity: Scm_Purchase_Product_Prices

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Purchase_Product_Price_Id|`Guid`|`PK`, Readonly||
|From_Date|`DateTime?`||Starting date of validity of the price. `Filter(eq;ge;le)` |
|Notes|`String`||Notes for this PurchaseProductPrice. |
|Priority|`Priority`|Allowed: `1`, `2`, `3`, `4`, `5`|Priority of the price comparative to other prices. `Required` `Default(2)` `Filter(multi eq)` |
|Thru_Date|`DateTime?`||Ending date (inclusive) of the validity of the price. `Filter(eq;ge;le)` |
