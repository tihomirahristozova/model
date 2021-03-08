# Table Crm_Bonus_Program_Products

Provides a way to specify additional (to the one specified in Bonus Program.Conditional Product) products, which will be used to evaluate bonus program conditions. When any of the products exists in the sales document, the conditions are satisfied and the program is applied. When the conditional products list for a bonus program is empty, it is considered that the program is valid for all products. Entity: Crm_Bonus_Program_Products

# Aggregate Hierarchy

* [Crm_Bonus_Programs](Crm_Bonus_Programs.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Bonus_Program_Product_Id|`Guid`|`PK`, Readonly||
