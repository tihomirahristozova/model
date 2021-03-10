# Table Prd_Principal_Recipe_Operations

Contains the operations within a principal recipe. Entity: Prd_Principal_Recipe_Operations

## Owner Tables Hierarchy

* [Prd_Principal_Recipes](Prd_Principal_Recipes.md)
* [Gen_Product_Groups](Gen_Product_Groups.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Id](#id)|`uniqueidentifier` `PK`||
|[Principal_Recipe_Id](#principal_recipe_id)|`uniqueidentifier` ||
|[Operation_Id](#operation_id)|`uniqueidentifier` |The generic operation definition. The data is copied locally and can be modified for this specific record.|
|[Operation_Description](#operation_description)|`nvarchar(2147483647)` |The description of the operation. Initially copied from the generic operation definition.|
|[Workgroup_Resource_Id](#workgroup_resource_id)|`uniqueidentifier` |Required workgroup resource for the operation. NULL means that no resource is required or the resource will be specified later|
|[Use_Quantity](#use_quantity)|`decimal(9, 3)` |Quantity of the workgroup resource that should be allocated for the operation|
|[Use_Quantity_Unit_Id](#use_quantity_unit_id)|`uniqueidentifier` |The measurement unit of Use_Quantity|
|[Minimum_Concurrent_Start_Time_Minutes](#minimum_concurrent_start_time_minutes)|`int` |How many minutes after the start of the previous operation can this operation start. NULL means that this operation should wait the previous operation to finish before starting|
|[Setup_Time_Minutes](#setup_time_minutes)|`int` |Time needed to setup the equipment|
|[Run_Time_Minutes](#run_time_minutes)|`int` |Duration of the operation for one piece in the standard measurement unit of the product|
|[Wait_Time_Minutes](#wait_time_minutes)|`int` |Wait time (drying, cooling, etc.) after the operation in minutes|
|[Move_Time_Minutes](#move_time_minutes)|`int` |Time to move the lot to the next operation in minutes|
|[Scrap_Rate](#scrap_rate)|`decimal(7, 6)` |Standard rate of scrap during the operation|
|[Notes](#notes)|`nvarchar(254)` ||
|[Tooling](#tooling)|`nvarchar(254)` |The tools needed for the routing step|
|[Operation_Instruction_Id](#operation_instruction_id)|`uniqueidentifier` |Link to additional data, containing instructions in external format|
|[Line_Ord](#line_ord)|`int` |Consecutive line number within the principal recipe.|
|[Conditional_Property_Id](#conditional_property_id)|`uniqueidentifier` |When not NULL, specifies that, when creating recipe, the operation will be added only if this property is set for the main product|
|[Conditional_Property_Value](#conditional_property_value)|`nvarchar(254)` |The desired value of the Conditional Property. |
|[Conditional_Property_Description](#conditional_property_description)|`nvarchar(254)` `ML`|The desired description of the Conditional Property. |
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
|Derived From|[Prd_Principal_Recipe_Operations](Prd_Principal_Recipe_Operations.md).[Id](Prd_Principal_Recipe_Operations.md#id)|
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

### Principal_Recipe_Id


Principal_Recipe_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|yes|
|Referenced Table|[Prd_Principal_Recipes](Prd_Principal_Recipes.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Prd_Principal_Recipe_Operations](Prd_Principal_Recipe_Operations.md).[Principal_Recipe_Id](Prd_Principal_Recipe_Operations.md#principal_recipe_id)|
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

### Operation_Id


Operation_Id


The generic operation definition. The data is copied locally and can be modified for this specific record.


The generic operation definition. The data is copied locally and can be modified for this specific record.

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
|Derived From|[Prd_Principal_Recipe_Operations](Prd_Principal_Recipe_Operations.md).[Operation_Id](Prd_Principal_Recipe_Operations.md#operation_id)|
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

### Operation_Description


Operation_Description


The description of the operation. Initially copied from the generic operation definition.


The description of the operation. Initially copied from the generic operation definition.

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
|Derived From|[Prd_Principal_Recipe_Operations](Prd_Principal_Recipe_Operations.md).[Operation_Description](Prd_Principal_Recipe_Operations.md#operation_description)|
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
|Max Length|2147483647|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Workgroup_Resource_Id


Workgroup_Resource_Id


Required workgroup resource for the operation. NULL means that no resource is required or the resource will be specified later


Required workgroup resource for the operation. NULL means that no resource is required or the resource will be specified later

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
|Derived From|[Prd_Principal_Recipe_Operations](Prd_Principal_Recipe_Operations.md).[Workgroup_Resource_Id](Prd_Principal_Recipe_Operations.md#workgroup_resource_id)|
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
|Derived From|[Prd_Principal_Recipe_Operations](Prd_Principal_Recipe_Operations.md).[Use_Quantity](Prd_Principal_Recipe_Operations.md#use_quantity)|
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

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|GreaterThanOrLessThan|None|yes|no|

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
|Derived From|[Prd_Principal_Recipe_Operations](Prd_Principal_Recipe_Operations.md).[Use_Quantity_Unit_Id](Prd_Principal_Recipe_Operations.md#use_quantity_unit_id)|
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

### Minimum_Concurrent_Start_Time_Minutes


Minimum_Concurrent_Start_Time_Minutes


How many minutes after the start of the previous operation can this operation start. NULL means that this operation should wait the previous operation to finish before starting


How many minutes after the start of the previous operation can this operation start. NULL means that this operation should wait the previous operation to finish before starting

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
|Derived From|[Prd_Principal_Recipe_Operations](Prd_Principal_Recipe_Operations.md).[Minimum_Concurrent_Start_Time_Minutes](Prd_Principal_Recipe_Operations.md#minimum_concurrent_start_time_minutes)|
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
|Derived From|[Prd_Principal_Recipe_Operations](Prd_Principal_Recipe_Operations.md).[Setup_Time_Minutes](Prd_Principal_Recipe_Operations.md#setup_time_minutes)|
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

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|GreaterThanOrLessThan|None|yes|no|

### Run_Time_Minutes


Run_Time_Minutes


Duration of the operation for one piece in the standard measurement unit of the product


Duration of the operation for one piece in the standard measurement unit of the product

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
|Derived From|[Prd_Principal_Recipe_Operations](Prd_Principal_Recipe_Operations.md).[Run_Time_Minutes](Prd_Principal_Recipe_Operations.md#run_time_minutes)|
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

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|GreaterThanOrLessThan|None|yes|no|

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
|Derived From|[Prd_Principal_Recipe_Operations](Prd_Principal_Recipe_Operations.md).[Wait_Time_Minutes](Prd_Principal_Recipe_Operations.md#wait_time_minutes)|
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

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|GreaterThanOrLessThan|None|yes|no|

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
|Derived From|[Prd_Principal_Recipe_Operations](Prd_Principal_Recipe_Operations.md).[Move_Time_Minutes](Prd_Principal_Recipe_Operations.md#move_time_minutes)|
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

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|GreaterThanOrLessThan|None|yes|no|

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
|Derived From|[Prd_Principal_Recipe_Operations](Prd_Principal_Recipe_Operations.md).[Scrap_Rate](Prd_Principal_Recipe_Operations.md#scrap_rate)|
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
|Derived From|[Prd_Principal_Recipe_Operations](Prd_Principal_Recipe_Operations.md).[Notes](Prd_Principal_Recipe_Operations.md#notes)|
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
|UI Width|Short|
|Supports EQUALS_IN|no|

### Tooling


Tooling


The tools needed for the routing step


The tools needed for the routing step

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
|Derived From|[Prd_Principal_Recipe_Operations](Prd_Principal_Recipe_Operations.md).[Tooling](Prd_Principal_Recipe_Operations.md#tooling)|
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
|UI Width|Short|
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
|Derived From|[Prd_Principal_Recipe_Operations](Prd_Principal_Recipe_Operations.md).[Operation_Instruction_Id](Prd_Principal_Recipe_Operations.md#operation_instruction_id)|
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

### Line_Ord


Line_Ord


Consecutive line number within the principal recipe.


Consecutive line number within the principal recipe.

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
|Derived From|[Prd_Principal_Recipe_Operations](Prd_Principal_Recipe_Operations.md).[Line_Ord](Prd_Principal_Recipe_Operations.md#line_ord)|
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
|Supports EQUALS_IN|no|

### Conditional_Property_Id


Conditional_Property_Id


When not NULL, specifies that, when creating recipe, the operation will be added only if this property is set for the main product


When not NULL, specifies that, when creating recipe, the operation will be added only if this property is set for the main product

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Properties](Gen_Properties.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Prd_Principal_Recipe_Operations](Prd_Principal_Recipe_Operations.md).[Conditional_Property_Id](Prd_Principal_Recipe_Operations.md#conditional_property_id)|
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
|UI Width|100|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Conditional_Property_Value


Conditional_Property_Value


The desired value of the Conditional Property. 


The desired value of the Conditional Property. 

| Property | Value |
| - | - |
|Type|nvarchar(254)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Prd_Principal_Recipe_Operations](Prd_Principal_Recipe_Operations.md).[Conditional_Property_Value](Prd_Principal_Recipe_Operations.md#conditional_property_value)|
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

### Conditional_Property_Description


Conditional_Property_Description


The desired description of the Conditional Property. 


The desired description of the Conditional Property. 

| Property | Value |
| - | - |
|Type|nvarchar(254)|
|Is Mulitlanguage|yes|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Prd_Principal_Recipe_Operations](Prd_Principal_Recipe_Operations.md).[Conditional_Property_Description](Prd_Principal_Recipe_Operations.md#conditional_property_description)|
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
|Derived From|[Prd_Principal_Recipe_Operations](Prd_Principal_Recipe_Operations.md).[Row_Version](Prd_Principal_Recipe_Operations.md#row_version)|
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


