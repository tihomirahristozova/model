# Table Acc_Financial_Statement_Nodes

Contains the hierarchical structure of the user-defined financial statements. Entity: Acc_Financial_Statement_Nodes

## Owner Tables Hierarchy

* [Acc_Financial_Statements](Acc_Financial_Statements.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Parent_Full_Path](#parent_full_path)|`nvarchar(25)` |Parent financial statement node specified through its full identification path|
|[Financial_Statement_Node_Code](#financial_statement_node_code)|`nvarchar(3)` |Identifying code of the financial statement node. Unique within the parent financial statement node.|
|[Financial_Statement_Node_Name](#financial_statement_node_name)|`nvarchar(254)` `ML`|Name of the financial statement node|
|[Full_Path](#full_path)|`nvarchar(25)` Readonly|Full identification path of the financial statement node|
|[Financial_Statement_Node_Id](#financial_statement_node_id)|`uniqueidentifier` `PK`||
|[Financial_Statement_Id](#financial_statement_id)|`uniqueidentifier` ||
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Parent_Full_Path

| Property | Value |
| - | - |
|Type|nvarchar(25)|

### Financial_Statement_Node_Code

| Property | Value |
| - | - |
|Type|nvarchar(3)|

### Financial_Statement_Node_Name

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Full_Path

| Property | Value |
| - | - |
|Type|nvarchar(25)|

### Financial_Statement_Node_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Financial_Statement_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


