# Table Prd_Recipe_Operations

Contains the routing (operation list) of the recipes. Entity: Prd_Recipe_Operations

## Owner Tables Hierarchy

* [Prd_Recipes](Prd_Recipes.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Line_Ord](#line_ord)|`int` |Order of the operation within the recipe|
|[Id](#id)|`uniqueidentifier` `PK`||
|[Standard_Price_Per_Hour](#standard_price_per_hour)|`decimal(18, 6)` |Standard price for 1 hour work|
|[Operation_Instruction_Id](#operation_instruction_id)|`uniqueidentifier` |Link to additional data, containing instructions in external format|
|[Tooling](#tooling)|`nvarchar(2147483647)` |The tools needed for the routing step|
|[Notes](#notes)|`nvarchar(254)` ||
|[Scrap_Rate](#scrap_rate)|`decimal(7, 6)` |Standard rate of scrap during the operation|
|[Move_Time_Minutes](#move_time_minutes)|`int` |Time to move the lot to the next operation in minutes|
|[Wait_Time_Minutes](#wait_time_minutes)|`int` |Wait time (drying, cooling, etc.) after the operation in minutes|
|[Standard_Cost_Per_Hour](#standard_cost_per_hour)|`decimal(18, 6)` |Standard cost per hour for this operation. It participates in the calculation of standard cost for production for the whole recipe.|
|[Run_Time_Minutes](#run_time_minutes)|`int` |Duration of the operation for standard lot of the product|
|[Minimum_Concurrent_Start_Time_Minutes](#minimum_concurrent_start_time_minutes)|`int` |How many minutes after the start of this operation can the next operation start. NULL means that the next operation should wait this operation to finish before starting|
|[Use_Quantity_Unit_Id](#use_quantity_unit_id)|`uniqueidentifier` |The measurement unit of Use_Quantity|
|[Use_Quantity](#use_quantity)|`decimal(9, 3)` |Quantity of the workgroup resource that should be allocated for the operation|
|[Workgroup_Resource_Id](#workgroup_resource_id)|`uniqueidentifier` |The exact workgroup resource that is engaged in the operation. NULL means that no resource is needed or it will be specfied at a later stage|
|[Operation_Description](#operation_description)|`nvarchar(2147483647)` |The description of the operation.|
|[Operation_Id](#operation_id)|`uniqueidentifier` |Standard operation Id. If not NULL used to load the details. If NULL the details (times, scrap rates, etc.) must be entered manually|
|[Routing_Operation_Id](#routing_operation_id)|`uniqueidentifier` ||
|[Recipe_Id](#recipe_id)|`uniqueidentifier` ||
|[Setup_Time_Minutes](#setup_time_minutes)|`int` |Time needed to setup the equipment|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Line_Ord


Line_Ord


Order of the operation within the recipe


Order of the operation within the recipe

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
|Derived From|[Prd_Recipe_Operations](Prd_Recipe_Operations.md).[Line_Ord](Prd_Recipe_Operations.md#line_ord)|
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
|UI Width|100|
|Supports EQUALS_IN|no|

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
|Derived From|[Prd_Recipe_Operations](Prd_Recipe_Operations.md).[Id](Prd_Recipe_Operations.md#id)|
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

### Standard_Price_Per_Hour


Standard_Price_Per_Hour


Standard price for 1 hour work


Standard price for 1 hour work

| Property | Value |
| - | - |
|Type|decimal(18, 6)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|0|
|Derived From|[Prd_Recipe_Operations](Prd_Recipe_Operations.md).[Standard_Price_Per_Hour](Prd_Recipe_Operations.md#standard_price_per_hour)|
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

### Operation_Instruction_Id


Operation_Instruction_Id


Link to additional data, containing instructions in external format


Link to additional data, containing instructions in external format

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Prd_Operation_Instructions](Prd_Operation_Instructions.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Prd_Recipe_Operations](Prd_Recipe_Operations.md).[Operation_Instruction_Id](Prd_Recipe_Operations.md#operation_instruction_id)|
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
|Equals|NULL|yes|no|

### Tooling


Tooling


The tools needed for the routing step


The tools needed for the routing step

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
|Derived From|[Prd_Recipe_Operations](Prd_Recipe_Operations.md).[Tooling](Prd_Recipe_Operations.md#tooling)|
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
|Derived From|[Prd_Recipe_Operations](Prd_Recipe_Operations.md).[Notes](Prd_Recipe_Operations.md#notes)|
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
|UI Width|100|
|Supports EQUALS_IN|no|

### Scrap_Rate


Scrap_Rate


Standard rate of scrap during the operation


Standard rate of scrap during the operation

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
|Derived From|[Prd_Recipe_Operations](Prd_Recipe_Operations.md).[Scrap_Rate](Prd_Recipe_Operations.md#scrap_rate)|
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

### Move_Time_Minutes


Move_Time_Minutes


Time to move the lot to the next operation in minutes


Time to move the lot to the next operation in minutes

| Property | Value |
| - | - |
|Type|int|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|0|
|Derived From|[Prd_Recipe_Operations](Prd_Recipe_Operations.md).[Move_Time_Minutes](Prd_Recipe_Operations.md#move_time_minutes)|
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

### Wait_Time_Minutes


Wait_Time_Minutes


Wait time (drying, cooling, etc.) after the operation in minutes


Wait time (drying, cooling, etc.) after the operation in minutes

| Property | Value |
| - | - |
|Type|int|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|0|
|Derived From|[Prd_Recipe_Operations](Prd_Recipe_Operations.md).[Wait_Time_Minutes](Prd_Recipe_Operations.md#wait_time_minutes)|
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

### Standard_Cost_Per_Hour


Standard_Cost_Per_Hour


Standard cost per hour for this operation. It participates in the calculation of standard cost for production for the whole recipe.


Standard cost per hour for this operation. It participates in the calculation of standard cost for production for the whole recipe.

| Property | Value |
| - | - |
|Type|decimal(18, 6)|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Prd_Recipe_Operations](Prd_Recipe_Operations.md).[Standard_Cost_Per_Hour](Prd_Recipe_Operations.md#standard_cost_per_hour)|
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

### Run_Time_Minutes


Run_Time_Minutes


Duration of the operation for standard lot of the product


Duration of the operation for standard lot of the product

| Property | Value |
| - | - |
|Type|int|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|0|
|Derived From|[Prd_Recipe_Operations](Prd_Recipe_Operations.md).[Run_Time_Minutes](Prd_Recipe_Operations.md#run_time_minutes)|
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

### Minimum_Concurrent_Start_Time_Minutes


Minimum_Concurrent_Start_Time_Minutes


How many minutes after the start of this operation can the next operation start. NULL means that the next operation should wait this operation to finish before starting


How many minutes after the start of this operation can the next operation start. NULL means that the next operation should wait this operation to finish before starting

| Property | Value |
| - | - |
|Type|int|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Prd_Recipe_Operations](Prd_Recipe_Operations.md).[Minimum_Concurrent_Start_Time_Minutes](Prd_Recipe_Operations.md#minimum_concurrent_start_time_minutes)|
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

### Use_Quantity_Unit_Id


Use_Quantity_Unit_Id


The measurement unit of Use_Quantity


The measurement unit of Use_Quantity

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
|Derived From|[Prd_Recipe_Operations](Prd_Recipe_Operations.md).[Use_Quantity_Unit_Id](Prd_Recipe_Operations.md#use_quantity_unit_id)|
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

### Use_Quantity


Use_Quantity


Quantity of the workgroup resource that should be allocated for the operation


Quantity of the workgroup resource that should be allocated for the operation

| Property | Value |
| - | - |
|Type|decimal(9, 3)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|1|
|Derived From|[Prd_Recipe_Operations](Prd_Recipe_Operations.md).[Use_Quantity](Prd_Recipe_Operations.md#use_quantity)|
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

### Workgroup_Resource_Id


Workgroup_Resource_Id


The exact workgroup resource that is engaged in the operation. NULL means that no resource is needed or it will be specfied at a later stage


The exact workgroup resource that is engaged in the operation. NULL means that no resource is needed or it will be specfied at a later stage

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Prd_Workgroup_Resources](Prd_Workgroup_Resources.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Prd_Recipe_Operations](Prd_Recipe_Operations.md).[Workgroup_Resource_Id](Prd_Recipe_Operations.md#workgroup_resource_id)|
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

### Operation_Description


Operation_Description


The description of the operation.


The description of the operation.

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
|Derived From|[Prd_Recipe_Operations](Prd_Recipe_Operations.md).[Operation_Description](Prd_Recipe_Operations.md#operation_description)|
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

### Operation_Id


Operation_Id


Standard operation Id. If not NULL used to load the details. If NULL the details (times, scrap rates, etc.) must be entered manually


Standard operation Id. If not NULL used to load the details. If NULL the details (times, scrap rates, etc.) must be entered manually

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Prd_Operations](Prd_Operations.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Prd_Recipe_Operations](Prd_Recipe_Operations.md).[Operation_Id](Prd_Recipe_Operations.md#operation_id)|
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

### Routing_Operation_Id


Routing_Operation_Id

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
|Derived From|[Prd_Recipe_Operations](Prd_Recipe_Operations.md).[Routing_Operation_Id](Prd_Recipe_Operations.md#routing_operation_id)|
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
|Equals|NULL|yes|no|

### Recipe_Id


Recipe_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|yes|
|Referenced Table|[Prd_Recipes](Prd_Recipes.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Prd_Recipe_Operations](Prd_Recipe_Operations.md).[Recipe_Id](Prd_Recipe_Operations.md#recipe_id)|
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

### Setup_Time_Minutes


Setup_Time_Minutes


Time needed to setup the equipment


Time needed to setup the equipment

| Property | Value |
| - | - |
|Type|int|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|0|
|Derived From|[Prd_Recipe_Operations](Prd_Recipe_Operations.md).[Setup_Time_Minutes](Prd_Recipe_Operations.md#setup_time_minutes)|
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
|Derived From|[Prd_Recipe_Operations](Prd_Recipe_Operations.md).[Row_Version](Prd_Recipe_Operations.md#row_version)|
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


