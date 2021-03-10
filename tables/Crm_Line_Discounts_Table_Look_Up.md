# Query Crm_Line_Discounts_Table_Look_Up


## Summary

| Name | Type | Description |
| - | - | --- |
|[Line_Discount_Id](#line_discount_id)|`uniqueidentifier` `PK`||
|[Description](#description)|`nvarchar` |The description of the discount that is shown to the operator when he/she should choose between different discounts|
|[Discount_Percent](#discount_percent)|`decimal(7, 6)` |The discount percent that should be applied if all the matching criteria are met.|
|[Priority](#priority)|`tinyint` Allowed: `1`, `2`, `3`, `4`, `5`|The priority of this discount policy. When selecting a discount for a sales document line, only the highest priority policy, matching the criteria is applied.|

## Columns

### Line_Discount_Id


Line_Discount_Id

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
|Derived From|[Crm_Line_Discounts](Crm_Line_Discounts.md).[Line_Discount_Id](Crm_Line_Discounts.md#line_discount_id)|
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
|Equals|NULL|no|no|

### Description


Description


The description of the discount that is shown to the operator when he/she should choose between different discounts


The description of the discount that is shown to the operator when he/she should choose between different discounts

| Property | Value |
| - | - |
|Type|nvarchar|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Line_Discounts](Crm_Line_Discounts.md).[Description](Crm_Line_Discounts.md#description)|
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
|UI Width|Long|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Like|None|no|no|

### Discount_Percent


Discount_Percent


The discount percent that should be applied if all the matching criteria are met.


The discount percent that should be applied if all the matching criteria are met.

| Property | Value |
| - | - |
|Type|decimal(7, 6)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None, IsPercent|
|Default Value|0|
|Derived From|[Crm_Line_Discounts](Crm_Line_Discounts.md).[Discount_Percent](Crm_Line_Discounts.md#discount_percent)|
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

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|GreaterThanOrLessThan|None|yes|no|

### Priority


Priority


The priority of this discount policy. When selecting a discount for a sales document line, only the highest priority policy, matching the criteria is applied.


The priority of this discount policy. When selecting a discount for a sales document line, only the highest priority policy, matching the criteria is applied.

| Property | Value |
| - | - |
|Type|tinyint|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Allowed Values|`1`, `2`, `3`, `4`, `5`|
|Default Value|3|
|Derived From|[Crm_Line_Discounts](Crm_Line_Discounts.md).[Priority](Crm_Line_Discounts.md#priority)|
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
|UI Width|Short|
|Supports EQUALS_IN|no|


