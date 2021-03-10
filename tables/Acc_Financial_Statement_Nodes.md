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


Parent_Full_Path


Parent financial statement node specified through its full identification path


Parent financial statement node specified through its full identification path

| Property | Value |
| - | - |
|Type|nvarchar(25)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Acc_Financial_Statement_Nodes](Acc_Financial_Statement_Nodes.md).[Parent_Full_Path](Acc_Financial_Statement_Nodes.md#parent_full_path)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|25|
|Order|0|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Like|None|no|no|

### Financial_Statement_Node_Code


Financial_Statement_Node_Code


Identifying code of the financial statement node. Unique within the parent financial statement node.


Identifying code of the financial statement node. Unique within the parent financial statement node.

| Property | Value |
| - | - |
|Type|nvarchar(3)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Acc_Financial_Statement_Nodes](Acc_Financial_Statement_Nodes.md).[Financial_Statement_Node_Code](Acc_Financial_Statement_Nodes.md#financial_statement_node_code)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|3|
|Order|1|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Short|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|
|Like|None|no|no|

### Financial_Statement_Node_Name


Financial_Statement_Node_Name


Name of the financial statement node


Name of the financial statement node

| Property | Value |
| - | - |
|Type|nvarchar(254)|
|Is Mulitlanguage|yes|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Acc_Financial_Statement_Nodes](Acc_Financial_Statement_Nodes.md).[Financial_Statement_Node_Name](Acc_Financial_Statement_Nodes.md#financial_statement_node_name)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|254|
|Order|2|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Long|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Like|None|no|no|

### Full_Path


Full_Path


Full identification path of the financial statement node


Full identification path of the financial statement node

| Property | Value |
| - | - |
|Type|nvarchar(25)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|yes|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Acc_Financial_Statement_Nodes](Acc_Financial_Statement_Nodes.md).[Full_Path](Acc_Financial_Statement_Nodes.md#full_path)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|25|
|Order|3|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Like|None|no|no|

### Financial_Statement_Node_Id


Financial_Statement_Node_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|yes|
|Order in Primary Key|1|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|NewGuid|
|Derived From|[Acc_Financial_Statement_Nodes](Acc_Financial_Statement_Nodes.md).[Financial_Statement_Node_Id](Acc_Financial_Statement_Nodes.md#financial_statement_node_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|yes|

### Financial_Statement_Id


Financial_Statement_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|yes|
|Referenced Table|[Acc_Financial_Statements](Acc_Financial_Statements.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Acc_Financial_Statement_Nodes](Acc_Financial_Statement_Nodes.md).[Financial_Statement_Id](Acc_Financial_Statement_Nodes.md#financial_statement_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Row_Version


Row_Version

| Property | Value |
| - | - |
|Type|timestamp|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Acc_Financial_Statement_Nodes](Acc_Financial_Statement_Nodes.md).[Row_Version](Acc_Financial_Statement_Nodes.md#row_version)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|


