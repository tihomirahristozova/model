# Table Cost_Calculation_Product_Outputs

Represents costs allocated to product outputs. Entity: Cost_Calculation_Product_Outputs

## Owner Tables Hierarchy

* [Cost_Calculations](Cost_Calculations.md)
* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Line_No](#line_no)|`int` |Consecutive number of the line within the calculation|
|[Calculation_Product_Output_Id](#calculation_product_output_id)|`uniqueidentifier` `PK`||
|[Calculation_Id](#calculation_id)|`uniqueidentifier` ||
|[Quantity](#quantity)|`decimal(18, 3)` |The quantity produced|
|[Parent_Calculation_Product_Output_Id](#parent_calculation_product_output_id)|`uniqueidentifier` |When not NULL specifies the parent output, whose cost is "absorbed" within the current output.|
|[Project_Id](#project_id)|`uniqueidentifier` |The Project, which absorbed the cost.|
|[Sales_Order_Id](#sales_order_id)|`uniqueidentifier` |The Sales Order, which absorbed the cost.|
|[Product_Id](#product_id)|`uniqueidentifier` |The Product, which absorbed the cost.|
|[Lot_Id](#lot_id)|`uniqueidentifier` |The Lot, which absorbed the cost.|
|[Profit_Center_Id](#profit_center_id)|`uniqueidentifier` |The Profit Center, which absorbed the cost.|
|[Workgroup_Id](#workgroup_id)|`uniqueidentifier` |The Workgroup, which absorbed the cost.|
|[Work_Order_Id](#work_order_id)|`uniqueidentifier` |The Work Order, which absorbed the cost.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Line_No


Line_No


Consecutive number of the line within the calculation


Consecutive number of the line within the calculation

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
|Derived From|[Cost_Calculation_Product_Outputs](Cost_Calculation_Product_Outputs.md).[Line_No](Cost_Calculation_Product_Outputs.md#line_no)|
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
|Order|0|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|25|
|Supports EQUALS_IN|no|

### Calculation_Product_Output_Id


Calculation_Product_Output_Id

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
|Derived From|[Cost_Calculation_Product_Outputs](Cost_Calculation_Product_Outputs.md).[Calculation_Product_Output_Id](Cost_Calculation_Product_Outputs.md#calculation_product_output_id)|
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

### Calculation_Id


Calculation_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|yes|
|Referenced Table|[Cost_Calculations](Cost_Calculations.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Cost_Calculation_Product_Outputs](Cost_Calculation_Product_Outputs.md).[Calculation_Id](Cost_Calculation_Product_Outputs.md#calculation_id)|
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
|UI Width|100|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Quantity


Quantity


The quantity produced


The quantity produced

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
|Derived From|[Cost_Calculation_Product_Outputs](Cost_Calculation_Product_Outputs.md).[Quantity](Cost_Calculation_Product_Outputs.md#quantity)|
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
|UI Width|100|
|Supports EQUALS_IN|no|

### Parent_Calculation_Product_Output_Id


Parent_Calculation_Product_Output_Id


When not NULL specifies the parent output, whose cost is "absorbed" within the current output.


When not NULL specifies the parent output, whose cost is "absorbed" within the current output.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Cost_Calculation_Product_Outputs](Cost_Calculation_Product_Outputs.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Cost_Calculation_Product_Outputs](Cost_Calculation_Product_Outputs.md).[Parent_Calculation_Product_Output_Id](Cost_Calculation_Product_Outputs.md#parent_calculation_product_output_id)|
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
|UI Width|100|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Project_Id


Project_Id


The Project, which absorbed the cost.


The Project, which absorbed the cost.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Cost_Calculation_Product_Outputs](Cost_Calculation_Product_Outputs.md).[Project_Id](Cost_Calculation_Product_Outputs.md#project_id)|
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
|UI Width|100|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Sales_Order_Id


Sales_Order_Id


The Sales Order, which absorbed the cost.


The Sales Order, which absorbed the cost.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Crm_Sales_Orders](Crm_Sales_Orders.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Cost_Calculation_Product_Outputs](Cost_Calculation_Product_Outputs.md).[Sales_Order_Id](Cost_Calculation_Product_Outputs.md#sales_order_id)|
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
|UI Width|100|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Product_Id


Product_Id


The Product, which absorbed the cost.


The Product, which absorbed the cost.

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
|Derived From|[Cost_Calculation_Product_Outputs](Cost_Calculation_Product_Outputs.md).[Product_Id](Cost_Calculation_Product_Outputs.md#product_id)|
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
|UI Width|100|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Lot_Id


Lot_Id


The Lot, which absorbed the cost.


The Lot, which absorbed the cost.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Inv_Lots](Inv_Lots.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Cost_Calculation_Product_Outputs](Cost_Calculation_Product_Outputs.md).[Lot_Id](Cost_Calculation_Product_Outputs.md#lot_id)|
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
|UI Width|100|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Profit_Center_Id


Profit_Center_Id


The Profit Center, which absorbed the cost.


The Profit Center, which absorbed the cost.

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
|Derived From|[Cost_Calculation_Product_Outputs](Cost_Calculation_Product_Outputs.md).[Profit_Center_Id](Cost_Calculation_Product_Outputs.md#profit_center_id)|
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
|UI Width|100|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Workgroup_Id


Workgroup_Id


The Workgroup, which absorbed the cost.


The Workgroup, which absorbed the cost.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Prd_Workgroups](Prd_Workgroups.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Cost_Calculation_Product_Outputs](Cost_Calculation_Product_Outputs.md).[Workgroup_Id](Cost_Calculation_Product_Outputs.md#workgroup_id)|
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
|UI Width|100|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Work_Order_Id


Work_Order_Id


The Work Order, which absorbed the cost.


The Work Order, which absorbed the cost.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Prd_Work_Orders](Prd_Work_Orders.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Cost_Calculation_Product_Outputs](Cost_Calculation_Product_Outputs.md).[Work_Order_Id](Cost_Calculation_Product_Outputs.md#work_order_id)|
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
|UI Width|100|
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
|Derived From|[Cost_Calculation_Product_Outputs](Cost_Calculation_Product_Outputs.md).[Row_Version](Cost_Calculation_Product_Outputs.md#row_version)|
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


