# Table Rent_Lease_Contract_Lines

The detail lines of rental contracts. Each line contains rental conditions for one asset of the rental contract. Entity: Rent_Lease_Contract_Lines

# Aggregate Hierarchy

* [Rent_Lease_Contracts](Rent_Lease_Contracts.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Lease_Line_Id|`Guid`|`PK`, Readonly||
|End_Date|`DateTime`||Ending date of lease of this asset. `Required` `Filter(multi eq;ge;le)` |
|Line_No|`Int32`||Consecutive number of the line within the lease contract. `Required` `Filter(eq;ge;le)` |
|Line_Notes|`String`||Notes for this line. |
|Start_Date|`DateTime`||Starting date of lease for this asset. `Required` `Filter(multi eq;ge;le)` |
