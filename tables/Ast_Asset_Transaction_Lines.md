# Table Ast_Asset_Transaction_Lines

Asset value transaction lines. Each line changes the values of one asset in one valuation model. Entity: Ast_Asset_Transaction_Lines

# Aggregate Hierarchy

* [Ast_Asset_Transactions](Ast_Asset_Transactions.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Asset_Transaction_Line_Id|`Guid`|`PK`, Readonly||
|Operation_Type|`OperationType`|Allowed: `ADJ`, `DEP`, `PUR`, `SLS`, `REV`|Type of the current asset operation: PUR = Purchase, SLS = Sale, DEP = Depreciation, ADJ = Adjustment, REV = Reevaluation. `Required` `Default("ADJ")` `Filter(multi eq)` |
