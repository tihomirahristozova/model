# Table Crm_Pricing_Model_Costs

List of costs, associated with a pricing model. Entity: Crm_Pricing_Model_Costs

# Aggregate Hierarchy

* [Crm_Pricing_Models](Crm_Pricing_Models.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Pricing_Model_Cost_Id|`Guid`|`PK`, Readonly||
|Amount_Percent|`Decimal?`||Used when the cost is calculated as percent of the amount. null when the cost is calculated in a different way. |
|Line_No|`Int32`||The consequtive number of the cost within the pricing model. `Required` |
