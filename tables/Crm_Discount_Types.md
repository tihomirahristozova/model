# Table Crm_Discount_Types

Contains the different types of discounts, which can be applied to sales lines. Different types of discounts can be combined for a single sales line. Entity: Crm_Discount_Types

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Discount_Type_Id|`Guid`|`PK`, Readonly||
|Action_Type|`ActionType`|Allowed: `A`, `R`, `M`|Specifies the way the discount is applied over the previous discounts. `Required` `Default("A")` `Filter(multi eq)` |
|Calculation_Method|`CalculationMethod`|Allowed: `S`, `P`, `B`|Specifies whether the calculation method of the discount is based on a standard discount, promotional package, bonus program, etc. `Required` `Filter(multi eq)` |
|Discount_Type_Code|`String`||The unique code of the DiscountType. `Required` `Filter(eq)` |
|Is_System|`Boolean`||Specifies whether this discount type is created and managed by the system. `Required` `Default(false)` `Filter(multi eq)` |
|Discount_Type_Name|`String`||The name of this DiscountType. `Required` `Filter(like)` |
|Notes|`String`||Notes for this DiscountType. |
|Ord|`Int32`||Determines the order in which the discounts are applied. The discounts with smaller Ord are applied first. `Required` `Default(1)` `Filter(ge;le)` |
