# Table Log_Transportation_Execution_Lines

Contains details of executions of transportation order lines. Entity: Log_Transportation_Execution_Lines (Introduced in version 18.2)

## Owner Tables Hierarchy

* [Log_Transportation_Executions](Log_Transportation_Executions.md)
* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Transportation_Execution_Line_Id](#transportation_execution_line_id)|`uniqueidentifier` `PK`||
|[Transportation_Execution_Id](#transportation_execution_id)|`uniqueidentifier` ||
|[Line_No](#line_no)|`int` |Consecutive line number within this execution.|
|[Execution_Of_Transportation_Order_Line_Id](#execution_of_transportation_order_line_id)|`uniqueidentifier` |The transportation order line, which is executed.|
|[Geo_Point_Id](#geo_point_id)|`uniqueidentifier` |The geographic point, where the operation is executed.|
|[Operation_Type](#operation_type)|`nvarchar(1)` Allowed: `L`, `U`, `O`|The type of operation being executed. L=Loading; U=Unloading; O=Other.|
|[Pallets_Count](#pallets_count)|`int` |Number of pallets affected by this operation. NULL when unknown or N/A.|
|[Weight_Kg](#weight_kg)|`int` |Cargo weight in kg, affected by this operation. NULL when unknown or N/A.|
|[Volume_Cbm](#volume_cbm)|`int` |Cargo volume in cubic meters, affected by this operation. NULL when unknown or N/A.|
|[Execution_Date](#execution_date)|`date` |The date when the operation was executed.|
|[Execution_Time](#execution_time)|`time` |The time when the operation was executed.|
|[Pallet_Number](#pallet_number)|`nvarchar(32)` |Pallet number, when applicable. NULL when unknown or not applicable.|
|[Notes](#notes)|`nvarchar(2147483647)` ||

## Columns

### Transportation_Execution_Line_Id


Transportation_Execution_Line_Id

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
|Derived From|[Log_Transportation_Execution_Lines](Log_Transportation_Execution_Lines.md).[Transportation_Execution_Line_Id](Log_Transportation_Execution_Lines.md#transportation_execution_line_id)|
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

### Transportation_Execution_Id


Transportation_Execution_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|yes|
|Referenced Table|[Log_Transportation_Executions](Log_Transportation_Executions.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Log_Transportation_Execution_Lines](Log_Transportation_Execution_Lines.md).[Transportation_Execution_Id](Log_Transportation_Execution_Lines.md#transportation_execution_id)|
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


Consecutive line number within this execution.


Consecutive line number within this execution.

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
|Derived From|[Log_Transportation_Execution_Lines](Log_Transportation_Execution_Lines.md).[Line_No](Log_Transportation_Execution_Lines.md#line_no)|
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

### Execution_Of_Transportation_Order_Line_Id


Execution_Of_Transportation_Order_Line_Id


The transportation order line, which is executed.


The transportation order line, which is executed.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Log_Transportation_Order_Lines](Log_Transportation_Order_Lines.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Log_Transportation_Execution_Lines](Log_Transportation_Execution_Lines.md).[Execution_Of_Transportation_Order_Line_Id](Log_Transportation_Execution_Lines.md#execution_of_transportation_order_line_id)|
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

### Geo_Point_Id


Geo_Point_Id


The geographic point, where the operation is executed.


The geographic point, where the operation is executed.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Geo_Points](Gen_Geo_Points.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Log_Transportation_Execution_Lines](Log_Transportation_Execution_Lines.md).[Geo_Point_Id](Log_Transportation_Execution_Lines.md#geo_point_id)|
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

### Operation_Type


Operation_Type


The type of operation being executed. L=Loading; U=Unloading; O=Other.


The type of operation being executed. L=Loading; U=Unloading; O=Other.

| Property | Value |
| - | - |
|Type|nvarchar(1)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Allowed Values|`L`, `U`, `O`|
|Default Value|None|
|Derived From|[Log_Transportation_Execution_Lines](Log_Transportation_Execution_Lines.md).[Operation_Type](Log_Transportation_Execution_Lines.md#operation_type)|
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
|Max Length|1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Pallets_Count


Pallets_Count


Number of pallets affected by this operation. NULL when unknown or N/A.


Number of pallets affected by this operation. NULL when unknown or N/A.

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
|Derived From|[Log_Transportation_Execution_Lines](Log_Transportation_Execution_Lines.md).[Pallets_Count](Log_Transportation_Execution_Lines.md#pallets_count)|
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

### Weight_Kg


Weight_Kg


Cargo weight in kg, affected by this operation. NULL when unknown or N/A.


Cargo weight in kg, affected by this operation. NULL when unknown or N/A.

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
|Derived From|[Log_Transportation_Execution_Lines](Log_Transportation_Execution_Lines.md).[Weight_Kg](Log_Transportation_Execution_Lines.md#weight_kg)|
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

### Volume_Cbm


Volume_Cbm


Cargo volume in cubic meters, affected by this operation. NULL when unknown or N/A.


Cargo volume in cubic meters, affected by this operation. NULL when unknown or N/A.

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
|Derived From|[Log_Transportation_Execution_Lines](Log_Transportation_Execution_Lines.md).[Volume_Cbm](Log_Transportation_Execution_Lines.md#volume_cbm)|
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

### Execution_Date


Execution_Date


The date when the operation was executed.


The date when the operation was executed.

| Property | Value |
| - | - |
|Type|date|
|DateTime Format|Date|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Log_Transportation_Execution_Lines](Log_Transportation_Execution_Lines.md).[Execution_Date](Log_Transportation_Execution_Lines.md#execution_date)|
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


The time when the operation was executed.


The time when the operation was executed.

| Property | Value |
| - | - |
|Type|time|
|DateTime Format|Time|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Log_Transportation_Execution_Lines](Log_Transportation_Execution_Lines.md).[Execution_Time](Log_Transportation_Execution_Lines.md#execution_time)|
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

### Pallet_Number


Pallet_Number


Pallet number, when applicable. NULL when unknown or not applicable.


Pallet number, when applicable. NULL when unknown or not applicable.

| Property | Value |
| - | - |
|Type|nvarchar(32)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Log_Transportation_Execution_Lines](Log_Transportation_Execution_Lines.md).[Pallet_Number](Log_Transportation_Execution_Lines.md#pallet_number)|
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
|Max Length|32|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

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
|Attributes|None|
|Default Value|None|
|Derived From|[Log_Transportation_Execution_Lines](Log_Transportation_Execution_Lines.md).[Notes](Log_Transportation_Execution_Lines.md#notes)|
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
|UI Width|Medium|
|Supports EQUALS_IN|no|


