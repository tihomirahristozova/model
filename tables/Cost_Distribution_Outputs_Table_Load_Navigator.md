# Query Cost_Distribution_Outputs_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Cost_Distribution_Output_Id](#cost_distribution_output_id)|`uniqueidentifier` `PK`||
|[Cost_Distribution_Id](#cost_distribution_id)|`uniqueidentifier` ||
|[Line_No](#line_no)|`int` |Unique, consecutive line number.|
|[Store_Transaction_Line_Id](#store_transaction_line_id)|`uniqueidentifier` |The store transaction line, for which costs will be distributed.|
|[Weight_Coefficient](#weight_coefficient)|`decimal(0, 0)` |The weight coefficient for prorate distribution of cost over the current line.|

## Columns

### Cost_Distribution_Output_Id


Cost_Distribution_Output_Id

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
|Derived From|[Cost_Distribution_Outputs](Cost_Distribution_Outputs.md).[Cost_Distribution_Output_Id](Cost_Distribution_Outputs.md#cost_distribution_output_id)|
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
|Order|0|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Cost_Distribution_Id


Cost_Distribution_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Cost_Distributions](Cost_Distributions.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Cost_Distribution_Outputs](Cost_Distribution_Outputs.md).[Cost_Distribution_Id](Cost_Distribution_Outputs.md#cost_distribution_id)|
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
|Order|1|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Line_No


Line_No


Unique, consecutive line number.


Unique, consecutive line number.

| Property | Value |
| - | - |
|Type|int|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Autoincrement|1|
|Derived From|[Cost_Distribution_Outputs](Cost_Distribution_Outputs.md).[Line_No](Cost_Distribution_Outputs.md#line_no)|
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
|Order|2|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Store_Transaction_Line_Id


Store_Transaction_Line_Id


The store transaction line, for which costs will be distributed.


The store transaction line, for which costs will be distributed.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Inv_Transaction_Lines](Inv_Transaction_Lines.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Cost_Distribution_Outputs](Cost_Distribution_Outputs.md).[Store_Transaction_Line_Id](Cost_Distribution_Outputs.md#store_transaction_line_id)|
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
|Order|3|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Weight_Coefficient


Weight_Coefficient


The weight coefficient for prorate distribution of cost over the current line.


The weight coefficient for prorate distribution of cost over the current line.

| Property | Value |
| - | - |
|Type|decimal(0, 0)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|1|
|Derived From|[Cost_Distribution_Outputs](Cost_Distribution_Outputs.md).[Weight_Coefficient](Cost_Distribution_Outputs.md#weight_coefficient)|
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
|Order|4|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|


