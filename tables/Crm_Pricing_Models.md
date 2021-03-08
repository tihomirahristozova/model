# Table Crm_Pricing_Models

Pricing models are assigned to product groups and are used to automate creation of standard costs and prices and related price records. Entity: Crm_Pricing_Models

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Pricing_Model_Id|`Guid`|`PK`, Readonly||
|Default_Margin_Percent|`Decimal`||Default margin between standard cost and standard price. The margin is applied to the products when calculating standard price. `Required` `Default(0)` |
|Pricing_Model_Name|`String`||The name of the pricing model. `Required` `Filter(eq;like)` |
