# Table Acc_Cost_Centers

Defines cost centers and their relation to profit centers. Entity: Acc_Cost_Centers

## Summary

| Name | Type | Description |
| - | - | --- |
|[Cost_Center_Id](#cost_center_id)|`uniqueidentifier` `PK`||
|[Parent_Cost_Center_Id](#parent_cost_center_id)|`uniqueidentifier` |Parent cost center, NULL if this is root cost center|
|[Cost_Center_Name](#cost_center_name)|`nvarchar(254)` ||
|[Relative_Weight](#relative_weight)|`decimal(18, 4)` |The weight of this cost center, relative to the other cost centers within the same parent. The weight is used during cost distribution calculations. The sum of weights of all cost centers within a parent does not need to be 100, the ratio of total weight over weight is used.|
|[Notes](#notes)|`nvarchar(254)` ||
|[Transfer_Cost_To_Profit_Center_Id](#transfer_cost_to_profit_center_id)|`uniqueidentifier` |Points to the profit center to which to transfer the cost. Valid only for leaf cost centers|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Cost_Center_Id


Cost_Center_Id

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
|Derived From|[Acc_Cost_Centers](Acc_Cost_Centers.md).[Cost_Center_Id](Acc_Cost_Centers.md#cost_center_id)|
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

### Parent_Cost_Center_Id


Parent_Cost_Center_Id


Parent cost center, NULL if this is root cost center


Parent cost center, NULL if this is root cost center

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Acc_Cost_Centers](Acc_Cost_Centers.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Acc_Cost_Centers](Acc_Cost_Centers.md).[Parent_Cost_Center_Id](Acc_Cost_Centers.md#parent_cost_center_id)|
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
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Cost_Center_Name


Cost_Center_Name

| Property | Value |
| - | - |
|Type|nvarchar(254)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Acc_Cost_Centers](Acc_Cost_Centers.md).[Cost_Center_Name](Acc_Cost_Centers.md#cost_center_name)|
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
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Long|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Like|None|no|no|

### Relative_Weight


Relative_Weight


The weight of this cost center, relative to the other cost centers within the same parent. The weight is used during cost distribution calculations. The sum of weights of all cost centers within a parent does not need to be 100, the ratio of total weight over weight is used.


The weight of this cost center, relative to the other cost centers within the same parent. The weight is used during cost distribution calculations. The sum of weights of all cost centers within a parent does not need to be 100, the ratio of total weight over weight is used.

| Property | Value |
| - | - |
|Type|decimal(18, 4)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|1|
|Derived From|[Acc_Cost_Centers](Acc_Cost_Centers.md).[Relative_Weight](Acc_Cost_Centers.md#relative_weight)|
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
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Notes


Notes

| Property | Value |
| - | - |
|Type|nvarchar(254)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None, IsLongString|
|Default Value|None|
|Derived From|[Acc_Cost_Centers](Acc_Cost_Centers.md).[Notes](Acc_Cost_Centers.md#notes)|
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
|Visible|yes|
|Max Length|254|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
|Supports EQUALS_IN|no|

### Transfer_Cost_To_Profit_Center_Id


Transfer_Cost_To_Profit_Center_Id


Points to the profit center to which to transfer the cost. Valid only for leaf cost centers


Points to the profit center to which to transfer the cost. Valid only for leaf cost centers

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Acc_Profit_Centers](Acc_Profit_Centers.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Acc_Cost_Centers](Acc_Cost_Centers.md).[Transfer_Cost_To_Profit_Center_Id](Acc_Cost_Centers.md#transfer_cost_to_profit_center_id)|
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
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

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
|Derived From|[Acc_Cost_Centers](Acc_Cost_Centers.md).[Row_Version](Acc_Cost_Centers.md#row_version)|
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


