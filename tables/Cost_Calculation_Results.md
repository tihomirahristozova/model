# Table Cost_Calculation_Results

Contains the results of cost calculations. Entity: Cost_Calculation_Results

## Owner Tables Hierarchy

* [Cost_Calculations](Cost_Calculations.md)
* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Line_No](#line_no)|`int` |Consecutive number of the line within the calculation|
|[Calculation_Result_Id](#calculation_result_id)|`uniqueidentifier` `PK`||
|[Calculation_Id](#calculation_id)|`uniqueidentifier` ||
|[Project_Id](#project_id)|`uniqueidentifier` |The Project to which the cost was allocated. When NULL, the cost was not allocated to any specific Project.|
|[Sales_Order_Id](#sales_order_id)|`uniqueidentifier` |The Sales Order to which the cost was allocated. When NULL, the cost was not allocated to any specific Sales Order.|
|[Product_Id](#product_id)|`uniqueidentifier` |The Product to which the cost was allocated. When NULL, the cost was not allocated to any specific Product.|
|[Lot_Id](#lot_id)|`uniqueidentifier` |The Lot to which the cost was allocated. When NULL, the cost was not allocated to any specific Lot.|
|[Profit_Center_Id](#profit_center_id)|`uniqueidentifier` |The Profit Center to which the cost was allocated. When NULL, the cost was not allocated to any specific Profit Center.|
|[Workgroup_Id](#workgroup_id)|`uniqueidentifier` |The Workgroup to which the cost was allocated. When NULL, the cost was not allocated to any specific Workgroup.|
|[Quantity](#quantity)|`decimal(14, 3)` |The quantity of the product|
|[Full_Cost](#full_cost)|`decimal(14, 2)` |The full cost of the specified quantity|
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
|Derived From|[Cost_Calculation_Results](Cost_Calculation_Results.md).[Line_No](Cost_Calculation_Results.md#line_no)|
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

### Calculation_Result_Id


Calculation_Result_Id

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
|Derived From|[Cost_Calculation_Results](Cost_Calculation_Results.md).[Calculation_Result_Id](Cost_Calculation_Results.md#calculation_result_id)|
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
|Derived From|[Cost_Calculation_Results](Cost_Calculation_Results.md).[Calculation_Id](Cost_Calculation_Results.md#calculation_id)|
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

### Project_Id


Project_Id


The Project to which the cost was allocated. When NULL, the cost was not allocated to any specific Project.


The Project to which the cost was allocated. When NULL, the cost was not allocated to any specific Project.

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
|Derived From|[Cost_Calculation_Results](Cost_Calculation_Results.md).[Project_Id](Cost_Calculation_Results.md#project_id)|
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


The Sales Order to which the cost was allocated. When NULL, the cost was not allocated to any specific Sales Order.


The Sales Order to which the cost was allocated. When NULL, the cost was not allocated to any specific Sales Order.

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
|Derived From|[Cost_Calculation_Results](Cost_Calculation_Results.md).[Sales_Order_Id](Cost_Calculation_Results.md#sales_order_id)|
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


The Product to which the cost was allocated. When NULL, the cost was not allocated to any specific Product.


The Product to which the cost was allocated. When NULL, the cost was not allocated to any specific Product.

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
|Derived From|[Cost_Calculation_Results](Cost_Calculation_Results.md).[Product_Id](Cost_Calculation_Results.md#product_id)|
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


The Lot to which the cost was allocated. When NULL, the cost was not allocated to any specific Lot.


The Lot to which the cost was allocated. When NULL, the cost was not allocated to any specific Lot.

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
|Derived From|[Cost_Calculation_Results](Cost_Calculation_Results.md).[Lot_Id](Cost_Calculation_Results.md#lot_id)|
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


The Profit Center to which the cost was allocated. When NULL, the cost was not allocated to any specific Profit Center.


The Profit Center to which the cost was allocated. When NULL, the cost was not allocated to any specific Profit Center.

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
|Derived From|[Cost_Calculation_Results](Cost_Calculation_Results.md).[Profit_Center_Id](Cost_Calculation_Results.md#profit_center_id)|
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


The Workgroup to which the cost was allocated. When NULL, the cost was not allocated to any specific Workgroup.


The Workgroup to which the cost was allocated. When NULL, the cost was not allocated to any specific Workgroup.

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
|Derived From|[Cost_Calculation_Results](Cost_Calculation_Results.md).[Workgroup_Id](Cost_Calculation_Results.md#workgroup_id)|
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

### Quantity


Quantity


The quantity of the product


The quantity of the product

| Property | Value |
| - | - |
|Type|decimal(14, 3)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|0|
|Derived From|[Cost_Calculation_Results](Cost_Calculation_Results.md).[Quantity](Cost_Calculation_Results.md#quantity)|
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

### Full_Cost


Full_Cost


The full cost of the specified quantity


The full cost of the specified quantity

| Property | Value |
| - | - |
|Type|decimal(14, 2)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|0|
|Derived From|[Cost_Calculation_Results](Cost_Calculation_Results.md).[Full_Cost](Cost_Calculation_Results.md#full_cost)|
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
|Derived From|[Cost_Calculation_Results](Cost_Calculation_Results.md).[Row_Version](Cost_Calculation_Results.md#row_version)|
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


