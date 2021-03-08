# Table Inv_Reconciliation_Lines

Store reconciliations (physical counting) detail lines. Each line contains the reconciliation for one combination of product, lot, bin and serial number. Entity: Inv_Reconciliation_Lines

# Aggregate Hierarchy

* [Inv_Reconciliations](Inv_Reconciliations.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Reconciliation_Line_Id|`Guid`|`PK`, Readonly||
|Line_Ord|`Int32`||The ordinal position of the line within the document. Duplicates are allowed, but not suggested. `Required` |
|Notes|`String`||Notes for this ReconciliationLine. |
|Transaction_Timestamp|`DateTime?`||Exact time when the transaction occurred. |
