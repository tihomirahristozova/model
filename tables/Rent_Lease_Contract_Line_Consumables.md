# Table Rent_Lease_Contract_Line_Consumables

Contains the consumables, which are sold accompanying asset rentals. Entity: Rent_Lease_Contract_Line_Consumables

# Aggregate Hierarchy

* [Rent_Lease_Contract_Lines](Rent_Lease_Contract_Lines.md)
* [Rent_Lease_Contracts](Rent_Lease_Contracts.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Lease_Line_Consumable_Id|`Guid`|`PK`, Readonly||
|Line_No|`Int32`||Consecutive number of the consumable within the lease contract line. `Required` `Filter(eq;ge;le)` |
