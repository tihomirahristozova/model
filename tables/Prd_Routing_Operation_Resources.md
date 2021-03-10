# Table Prd_Routing_Operation_Resources


## Owner Tables Hierarchy

* [Prd_Routing_Operations](Prd_Routing_Operations.md)
* [Prd_Routings](Prd_Routings.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Id](#id)|`uniqueidentifier` `PK`||
|[Routing_Operation_Id](#routing_operation_id)|`uniqueidentifier` |The routing operation, containing the line|
|[Function_Id](#function_id)|`uniqueidentifier` |Specifies the function, that the resource must be able to perform. This helps the selection of specific resource for the operation.|
|[Lock_Quantity](#lock_quantity)|`decimal(18, 3)` |the quantity of the resource to be locked. The measurement unit is specified in the Prd_Functions table.Primary_Unit.|
|[Line_Ord](#line_ord)|`int` |The position of the line in the recipe model|
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
|Derived From|[Prd_Routing_Operation_Resources](Prd_Routing_Operation_Resources.md).[Id](Prd_Routing_Operation_Resources.md#id)|
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

### Routing_Operation_Id


Routing_Operation_Id


The routing operation, containing the line


The routing operation, containing the line

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|yes|
|Referenced Table|[Prd_Routing_Operations](Prd_Routing_Operations.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Prd_Routing_Operation_Resources](Prd_Routing_Operation_Resources.md).[Routing_Operation_Id](Prd_Routing_Operation_Resources.md#routing_operation_id)|
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

### Function_Id


Function_Id


Specifies the function, that the resource must be able to perform. This helps the selection of specific resource for the operation.


Specifies the function, that the resource must be able to perform. This helps the selection of specific resource for the operation.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Prd_Functions](Prd_Functions.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Prd_Routing_Operation_Resources](Prd_Routing_Operation_Resources.md).[Function_Id](Prd_Routing_Operation_Resources.md#function_id)|
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

### Lock_Quantity


Lock_Quantity


the quantity of the resource to be locked. The measurement unit is specified in the Prd_Functions table.Primary_Unit.


the quantity of the resource to be locked. The measurement unit is specified in the Prd_Functions table.Primary_Unit.

| Property | Value |
| - | - |
|Type|decimal(18, 3)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|1|
|Derived From|[Prd_Routing_Operation_Resources](Prd_Routing_Operation_Resources.md).[Lock_Quantity](Prd_Routing_Operation_Resources.md#lock_quantity)|
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

### Line_Ord


Line_Ord


The position of the line in the recipe model


The position of the line in the recipe model

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
|Derived From|[Prd_Routing_Operation_Resources](Prd_Routing_Operation_Resources.md).[Line_Ord](Prd_Routing_Operation_Resources.md#line_ord)|
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
|Derived From|[Prd_Routing_Operation_Resources](Prd_Routing_Operation_Resources.md).[Row_Version](Prd_Routing_Operation_Resources.md#row_version)|
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


