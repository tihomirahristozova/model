# Table Acc_Financial_Statement_Node_Correspondances

Contains the actual correspondance filters, which specify how each financial statement node is calculated. Entity: Acc_Financial_Statement_Node_Correspondances

## Owner Tables Hierarchy

* [Acc_Financial_Statement_Nodes](Acc_Financial_Statement_Nodes.md)
* [Acc_Financial_Statements](Acc_Financial_Statements.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Financial_Statement_Node_Correspondance_Id](#financial_statement_node_correspondance_id)|`uniqueidentifier` `PK`||
|[Financial_Statement_Node_Id](#financial_statement_node_id)|`uniqueidentifier` ||
|[Account_Group_Id](#account_group_id)|`uniqueidentifier` |Main account group determining the correspondances for which the balances are summed|
|[Correspondant_Account_Group_Id](#correspondant_account_group_id)|`uniqueidentifier` |Correspondant account group determining the correspondances for which the balances are summed. If NULL means that the balances of all correspondances for the main account group are summed.|
|[Multiplier](#multiplier)|`decimal(18, 0)` |Factor by which the correspondence balance will be multiplied.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Financial_Statement_Node_Correspondance_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Financial_Statement_Node_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Account_Group_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Correspondant_Account_Group_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Multiplier

| Property | Value |
| - | - |
|Type|decimal(18, 0)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


