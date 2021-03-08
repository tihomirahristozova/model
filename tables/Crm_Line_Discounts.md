# Table Crm_Line_Discounts

Discount policies for sales documents. Entity: Crm_Line_Discounts

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Line_Discount_Id|`Guid`|`PK`, Readonly||
|Description|`String`||The description of the discount that is shown to the operator when he/she should choose between different discounts. `Filter(like)` |
|Discount_Percent|`Decimal`||The discount percent that should be applied if all the matching criteria are met. `Required` `Default(0)` `Filter(ge;le)` |
|From_Date|`DateTime?`||Starting date of validity of the discount. null means no from date restriction. `Filter(eq;ge;le)` |
|Priority|`Priority`|Allowed: `1`, `2`, `3`, `4`, `5`|The priority of this discount policy. When selecting a discount for a sales document line, only the highest priority policy, matching the criteria is applied. `Required` `Default(3)` |
|Thru_Date|`DateTime?`||Ending date (inclusive) of validity of the discount. If null, the discount is valid forever. `Filter(eq;ge;le)` |
