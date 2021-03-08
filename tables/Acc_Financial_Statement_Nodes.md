# Table Acc_Financial_Statement_Nodes

Contains the hierarchical structure of the user-defined financial statements. Entity: Acc_Financial_Statement_Nodes

# Aggregate Hierarchy

* [Acc_Financial_Statements](Acc_Financial_Statements.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Financial_Statement_Node_Id|`Guid`|`PK`, Readonly||
|Financial_Statement_Node_Code|`String`||Identifying code of the financial statement node. Unique within the parent financial statement node. `Required` `Filter(eq;like)` |
|Full_Path|`String`|Readonly|Full identification path of the financial statement node. `Filter(like)` `ReadOnly` |
|Financial_Statement_Node_Name|`MultilanguageString`||Name of the financial statement node. `Required` `Filter(like)` |
|Parent_Full_Path|`String`||Parent financial statement node specified through its full identification path. `Filter(like)` |
