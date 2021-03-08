# Table Crm_Promotional_Package_Lines

Detail records (lines) of promotional package definition. Entity: Crm_Promotional_Package_Lines

# Aggregate Hierarchy

* [Crm_Promotional_Packages](Crm_Promotional_Packages.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Promotional_Package_Line_Id|`Guid`|`PK`, Readonly||
|Line_Number|`Int32`||Consecutive line number. `Required` |
|Standard_Discount_Adjust_Or_Replace|`StandardDiscountAdjustOrReplace`|Allowed: `A`, `R`, `M`|Specifies standard discount change action: A=ADD, M=Mark down - apply after standard discount; R=REPLACE the standard discount. `Required` `Default("R")` |
|Standard_Discount_Percent_Adjust|`Decimal`||The value of change (in percents) for the standard discount. `Required` `Default(0)` |
