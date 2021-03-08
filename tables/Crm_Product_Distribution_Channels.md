# Table Crm_Product_Distribution_Channels

Channel assignments (listing) for products. Entity: Crm_Product_Distribution_Channels

# Aggregate Hierarchy

* [Gen_Products](Gen_Products.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Product_Distribution_Channel_Id|`Guid`|`PK`, Readonly||
|From_Date|`DateTime?`||When the product was listed. null-the product was not yet listed. The data is for informational purposes only and does not affect the listing status of the product (Is_Active does). `Default(Today)` `Filter(ge;le)` |
|Is_Active|`Boolean`||Is this product listing active? true=Yes, false=No. `Required` `Default(true)` `Filter(eq)` |
|Minimal_Sales_Quantity_Base|`Decimal?`||Minimal base quantity of the current product that has to be specified in any sale for this distribution channel. |
|To_Date|`DateTime?`||When the product was de-listed. null=unknown or the product was not de-listed. The data is for informational purposes only and does not affect the listing status of the product (Is_Active does). `Filter(ge;le)` |
