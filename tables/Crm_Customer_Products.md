# Table Crm_Customer_Products

Contains the products, that are contracted (listed) with a customer. Entity: Crm_Customer_Products

# Aggregate Hierarchy

* [Crm_Customers](Crm_Customers.md)
* [Gen_Parties](Gen_Parties.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Customer_Product_Id|`Guid`|`PK`, Readonly||
|From_Date|`DateTime?`||The initial date of the listing. null when the initial date is unknown. `Filter(eq;ge;le)` |
|Notes|`String`||Notes for the listing. |
|To_Date|`DateTime?`||The final date of the listing. null when the final date is unknown. `Filter(eq;ge;le)` |
