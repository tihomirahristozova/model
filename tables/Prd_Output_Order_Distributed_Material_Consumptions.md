# Table Prd_Output_Order_Distributed_Material_Consumptions

Contains the quantity of materials distributed over the output order lines. Entity: Prd_Output_Order_Distributed_Material_Consumptions

## Owner Tables Hierarchy

* [Prd_Output_Order_Lines](Prd_Output_Order_Lines.md)
* [Prd_Output_Orders](Prd_Output_Orders.md)
* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Id](#id)|`uniqueidentifier` `PK`||
|[Output_Order_Line_Id](#output_order_line_id)|`uniqueidentifier` Readonly|The output order line for which the distribution is recorded.|
|[Consumption_Order_Line_Id](#consumption_order_line_id)|`uniqueidentifier` Readonly|Consumption order line which requested the Consumed_Quantity|
|[Consumed_Quantity](#consumed_quantity)|`decimal(18, 3)` Readonly|Part of the quantity in the consumption order line which was used for the product in the output order line|
|[Consumed_Cost](#consumed_cost)|`decimal(14, 2)` Readonly|Cost of the actually issued Consumed_Quantity|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Id


Id

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
|Derived From|[Prd_Output_Order_Distributed_Material_Consumptions](Prd_Output_Order_Distributed_Material_Consumptions.md).[Id](Prd_Output_Order_Distributed_Material_Consumptions.md#id)|
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

### Output_Order_Line_Id


Output_Order_Line_Id


The output order line for which the distribution is recorded.


The output order line for which the distribution is recorded.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|yes|
|Referenced Table|[Prd_Output_Order_Lines](Prd_Output_Order_Lines.md)|
|Readonly|yes|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Prd_Output_Order_Distributed_Material_Consumptions](Prd_Output_Order_Distributed_Material_Consumptions.md).[Output_Order_Line_Id](Prd_Output_Order_Distributed_Material_Consumptions.md#output_order_line_id)|
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
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Consumption_Order_Line_Id


Consumption_Order_Line_Id


Consumption order line which requested the Consumed_Quantity


Consumption order line which requested the Consumed_Quantity

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Prd_Consumption_Order_Lines](Prd_Consumption_Order_Lines.md)|
|Readonly|yes|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Prd_Output_Order_Distributed_Material_Consumptions](Prd_Output_Order_Distributed_Material_Consumptions.md).[Consumption_Order_Line_Id](Prd_Output_Order_Distributed_Material_Consumptions.md#consumption_order_line_id)|
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
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Consumed_Quantity


Consumed_Quantity


Part of the quantity in the consumption order line which was used for the product in the output order line


Part of the quantity in the consumption order line which was used for the product in the output order line

| Property | Value |
| - | - |
|Type|decimal(18, 3)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|yes|
|Sortable|no|
|Attributes|None|
|Default Value|0|
|Derived From|[Prd_Output_Order_Distributed_Material_Consumptions](Prd_Output_Order_Distributed_Material_Consumptions.md).[Consumed_Quantity](Prd_Output_Order_Distributed_Material_Consumptions.md#consumed_quantity)|
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

### Consumed_Cost


Consumed_Cost


Cost of the actually issued Consumed_Quantity


Cost of the actually issued Consumed_Quantity

| Property | Value |
| - | - |
|Type|decimal(14, 2)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|yes|
|Sortable|no|
|Attributes|None|
|Default Value|0|
|Derived From|[Prd_Output_Order_Distributed_Material_Consumptions](Prd_Output_Order_Distributed_Material_Consumptions.md).[Consumed_Cost](Prd_Output_Order_Distributed_Material_Consumptions.md#consumed_cost)|
|Format|N2|
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
|Derived From|[Prd_Output_Order_Distributed_Material_Consumptions](Prd_Output_Order_Distributed_Material_Consumptions.md).[Row_Version](Prd_Output_Order_Distributed_Material_Consumptions.md#row_version)|
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


