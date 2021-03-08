# Table Rent_Transaction_Lines

Contains all transactions of Record of Handover / Handing-Over Record lines. Entity: Rent_Transaction_Lines

# Aggregate Hierarchy

* [Rent_Transactions](Rent_Transactions.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Rent_Transaction_Line_Id|`Guid`|`PK`, Readonly||
|Notes|`String`||Notes. |
|Transaction_Timestamp|`DateTime`||Transaction Timestamp. `Required` `Filter(multi eq;ge;le)` |
|Transaction_Type|`TransactionType`|Allowed: `D`, `R`, `W`, `S`|Transaction Type. `Required` `Filter(eq;like)` |
