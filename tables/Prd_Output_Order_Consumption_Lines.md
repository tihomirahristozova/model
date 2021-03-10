# Table Prd_Output_Order_Consumption_Lines

The internal production consumption of materials. Used only for control purposes - for comparison with the active consumption orders. Warehouse and accounting are still updated only by Consumption Orders. Entity: Prd_Output_Order_Consumption_Lines

## Owner Tables Hierarchy

* [Prd_Output_Orders](Prd_Output_Orders.md)
* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Output_Order_Consumption_Line_Id](#output_order_consumption_line_id)|`uniqueidentifier` `PK`||
|[Output_Order_Id](#output_order_id)|`uniqueidentifier` ||
|[Line_No](#line_no)|`int` ||
|[Line_Work_Order_Id](#line_work_order_id)|`uniqueidentifier` |Work order for the line. Initially copied from the header (if there work order is not null)|
|[Work_Order_Item_Id](#work_order_item_id)|`uniqueidentifier` |The work order item, for which the consumption is recorded.|
|[Work_Order_Item_Operation_Id](#work_order_item_operation_id)|`uniqueidentifier` |The operation in which the material was consumed. NULL = unknown|
|[Material_Id](#material_id)|`uniqueidentifier` |The consumed material|
|[Consumed_Quantity_For_Setup](#consumed_quantity_for_setup)|`decimal(18, 3)` |The consumed quantity of the material while setting up the operation.|
|[Consumed_Quantity_For_Run](#consumed_quantity_for_run)|`decimal(18, 3)` |The consumed quantity of the material for the operation.|
|[Consumed_Quantity_For_Scrap](#consumed_quantity_for_scrap)|`decimal(18, 3)` |The scrapped quantity of the material for this operation.|
|[Quantity_Unit_Id](#quantity_unit_id)|`uniqueidentifier` |The measurement unit for the consumed quantity for setup, run and scrap.|
|[Scrap_Type_Id](#scrap_type_id)|`uniqueidentifier` |When Consumed_Quantity_For_Scrap <> 0 denotes the reason for the scrap|
|[Notes](#notes)|`nvarchar(2147483647)` ||
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Output_Order_Consumption_Line_Id


Output_Order_Consumption_Line_Id

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
|Derived From|[Prd_Output_Order_Consumption_Lines](Prd_Output_Order_Consumption_Lines.md).[Output_Order_Consumption_Line_Id](Prd_Output_Order_Consumption_Lines.md#output_order_consumption_line_id)|
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

### Output_Order_Id


Output_Order_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|yes|
|Referenced Table|[Prd_Output_Orders](Prd_Output_Orders.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Prd_Output_Order_Consumption_Lines](Prd_Output_Order_Consumption_Lines.md).[Output_Order_Id](Prd_Output_Order_Consumption_Lines.md#output_order_id)|
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

### Line_No


Line_No

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
|Autoincrement|10|
|Derived From|[Prd_Output_Order_Consumption_Lines](Prd_Output_Order_Consumption_Lines.md).[Line_No](Prd_Output_Order_Consumption_Lines.md#line_no)|
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

### Line_Work_Order_Id


Line_Work_Order_Id


Work order for the line. Initially copied from the header (if there work order is not null)


Work order for the line. Initially copied from the header (if there work order is not null)

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Prd_Work_Orders](Prd_Work_Orders.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Prd_Output_Order_Consumption_Lines](Prd_Output_Order_Consumption_Lines.md).[Line_Work_Order_Id](Prd_Output_Order_Consumption_Lines.md#line_work_order_id)|
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
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Work_Order_Item_Id


Work_Order_Item_Id


The work order item, for which the consumption is recorded.


The work order item, for which the consumption is recorded.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Prd_Work_Order_Items](Prd_Work_Order_Items.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Prd_Output_Order_Consumption_Lines](Prd_Output_Order_Consumption_Lines.md).[Work_Order_Item_Id](Prd_Output_Order_Consumption_Lines.md#work_order_item_id)|
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
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Work_Order_Item_Operation_Id


Work_Order_Item_Operation_Id


The operation in which the material was consumed. NULL = unknown


The operation in which the material was consumed. NULL = unknown

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Prd_Work_Order_Item_Operations](Prd_Work_Order_Item_Operations.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Prd_Output_Order_Consumption_Lines](Prd_Output_Order_Consumption_Lines.md).[Work_Order_Item_Operation_Id](Prd_Output_Order_Consumption_Lines.md#work_order_item_operation_id)|
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
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Material_Id


Material_Id


The consumed material


The consumed material

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Products](Gen_Products.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Prd_Output_Order_Consumption_Lines](Prd_Output_Order_Consumption_Lines.md).[Material_Id](Prd_Output_Order_Consumption_Lines.md#material_id)|
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

### Consumed_Quantity_For_Setup


Consumed_Quantity_For_Setup


The consumed quantity of the material while setting up the operation.


The consumed quantity of the material while setting up the operation.

| Property | Value |
| - | - |
|Type|decimal(18, 3)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|0|
|Derived From|[Prd_Output_Order_Consumption_Lines](Prd_Output_Order_Consumption_Lines.md).[Consumed_Quantity_For_Setup](Prd_Output_Order_Consumption_Lines.md#consumed_quantity_for_setup)|
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

### Consumed_Quantity_For_Run


Consumed_Quantity_For_Run


The consumed quantity of the material for the operation.


The consumed quantity of the material for the operation.

| Property | Value |
| - | - |
|Type|decimal(18, 3)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|0|
|Derived From|[Prd_Output_Order_Consumption_Lines](Prd_Output_Order_Consumption_Lines.md).[Consumed_Quantity_For_Run](Prd_Output_Order_Consumption_Lines.md#consumed_quantity_for_run)|
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

### Consumed_Quantity_For_Scrap


Consumed_Quantity_For_Scrap


The scrapped quantity of the material for this operation.


The scrapped quantity of the material for this operation.

| Property | Value |
| - | - |
|Type|decimal(18, 3)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|0|
|Derived From|[Prd_Output_Order_Consumption_Lines](Prd_Output_Order_Consumption_Lines.md).[Consumed_Quantity_For_Scrap](Prd_Output_Order_Consumption_Lines.md#consumed_quantity_for_scrap)|
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

### Quantity_Unit_Id


Quantity_Unit_Id


The measurement unit for the consumed quantity for setup, run and scrap.


The measurement unit for the consumed quantity for setup, run and scrap.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Measurement_Units](Gen_Measurement_Units.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Prd_Output_Order_Consumption_Lines](Prd_Output_Order_Consumption_Lines.md).[Quantity_Unit_Id](Prd_Output_Order_Consumption_Lines.md#quantity_unit_id)|
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
|UI Width|Short|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Scrap_Type_Id


Scrap_Type_Id


When Consumed_Quantity_For_Scrap <> 0 denotes the reason for the scrap


When Consumed_Quantity_For_Scrap <> 0 denotes the reason for the scrap

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Inv_Scrap_Types](Inv_Scrap_Types.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Prd_Output_Order_Consumption_Lines](Prd_Output_Order_Consumption_Lines.md).[Scrap_Type_Id](Prd_Output_Order_Consumption_Lines.md#scrap_type_id)|
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
|Equals|NULL|yes|no|

### Notes


Notes

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None, IsLongString|
|Default Value|None|
|Derived From|[Prd_Output_Order_Consumption_Lines](Prd_Output_Order_Consumption_Lines.md).[Notes](Prd_Output_Order_Consumption_Lines.md#notes)|
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
|Max Length|2147483647|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
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
|Derived From|[Prd_Output_Order_Consumption_Lines](Prd_Output_Order_Consumption_Lines.md).[Row_Version](Prd_Output_Order_Consumption_Lines.md#row_version)|
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


