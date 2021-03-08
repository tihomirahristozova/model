# Table Acc_Financial_Statement_Node_Correspondances

Contains the actual correspondance filters, which specify how each financial statement node is calculated. Entity: Acc_Financial_Statement_Node_Correspondances

# Aggregate Hierarchy

* [Acc_Financial_Statement_Nodes](Acc_Financial_Statement_Nodes.md)
* [Acc_Financial_Statements](Acc_Financial_Statements.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Financial_Statement_Node_Correspondance_Id|`Guid`|`PK`, Readonly||
|Multiplier|`Decimal`||Factor by which the correspondence balance will be multiplied. `Required` `Default(1)` |
