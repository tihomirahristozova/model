# Table Crm_Dealers

External dealers. Entity: Crm_Dealers

# Aggregate Hierarchy

* [Gen_Parties](Gen_Parties.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Dealer_Id|`Guid`|`PK`, Readonly||
|From_Date|`DateTime?`||Start of the dealer relationship. `Default(Today)` `Filter(ge;le)` |
|Notes|`String`||Notes for this Dealer. |
|Thru_Date|`DateTime?`||Termination date of the dealership. null for active dealers. `Filter(ge;le)` |
