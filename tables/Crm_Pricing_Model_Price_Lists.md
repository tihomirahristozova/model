# Table Crm_Pricing_Model_Price_Lists

The price lists, which are updated by the pricing model. Entity: Crm_Pricing_Model_Price_Lists

# Aggregate Hierarchy

* [Crm_Pricing_Models](Crm_Pricing_Models.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Pricing_Model_Price_List_Id|`Guid`|`PK`, Readonly||
|Line_No|`Int32`||The consecutive number of this price list within the pricing model. `Required` |
|Margin_Percent|`Decimal?`||Used, when the price will be automatically calculated as percentage difference from standard price. It is usually a negative value. null, when the price will not be automatically calculated in this way. |
