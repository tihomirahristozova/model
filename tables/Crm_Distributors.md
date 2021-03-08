# Table Crm_Distributors

Distributors are external for the enterprise persons or companies who obtain sales orders from end-customers in benefit of the enterprise. Entity: Crm_Distributors

# Aggregate Hierarchy

* [Gen_Parties](Gen_Parties.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Distributor_Id|`Guid`|`PK`, Readonly||
|Flat_Commision_Percentage|`Decimal`||Not-zero if commision percentage should be applyied to all sales, regardless of product/discount/progressive/qunatity considerations. `Required` `Default(0)` |
