# Table Log_Transportation_Executions

Contains executions (loading, unloading or other operations) of the transportation orders. Entity: Log_Transportation_Executions (Introduced in version 18.2)

## Owner Tables Hierarchy

* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Transportation_Execution_Id](#transportation_execution_id)|`uniqueidentifier` `PK`||
|[Document_Id](#document_id)|`uniqueidentifier` ||
|[Execution_Date](#execution_date)|`date` |Specifies the execution date, if it is the same for all lines. NULL means that the lines have different execution dates.|
|[Execution_Time](#execution_time)|`time` |Specifies the execution time, if it is the same for all lines. NULL means that the lines have different execution times.|
|[Geo_Point_Id](#geo_point_id)|`uniqueidentifier` |Specifies the execution geographic point, if it is the same for all lines. NULL means that the lines have different geographic points.|

## Columns

### Transportation_Execution_Id


Transportation_Execution_Id

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
|Derived From|[Log_Transportation_Executions](Log_Transportation_Executions.md).[Transportation_Execution_Id](Log_Transportation_Executions.md#transportation_execution_id)|
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

### Document_Id


Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|yes|
|Referenced Table|[Gen_Documents](Gen_Documents.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Log_Transportation_Executions](Log_Transportation_Executions.md).[Document_Id](Log_Transportation_Executions.md#document_id)|
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

### Execution_Date


Execution_Date


Specifies the execution date, if it is the same for all lines. NULL means that the lines have different execution dates.


Specifies the execution date, if it is the same for all lines. NULL means that the lines have different execution dates.

| Property | Value |
| - | - |
|Type|date|
|DateTime Format|Date|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Log_Transportation_Executions](Log_Transportation_Executions.md).[Execution_Date](Log_Transportation_Executions.md#execution_date)|
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

### Execution_Time


Execution_Time


Specifies the execution time, if it is the same for all lines. NULL means that the lines have different execution times.


Specifies the execution time, if it is the same for all lines. NULL means that the lines have different execution times.

| Property | Value |
| - | - |
|Type|time|
|DateTime Format|Time|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Log_Transportation_Executions](Log_Transportation_Executions.md).[Execution_Time](Log_Transportation_Executions.md#execution_time)|
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

### Geo_Point_Id


Geo_Point_Id


Specifies the execution geographic point, if it is the same for all lines. NULL means that the lines have different geographic points.


Specifies the execution geographic point, if it is the same for all lines. NULL means that the lines have different geographic points.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Geo_Points](Gen_Geo_Points.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Log_Transportation_Executions](Log_Transportation_Executions.md).[Geo_Point_Id](Log_Transportation_Executions.md#geo_point_id)|
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


