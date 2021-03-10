# Table Eam_Maintenance_Types

Types of maintenances which can be scheduled and performed on the managed assets. Maintenances can be scheduled based on date and tracked parameter change. Entity: Eam_Maintenance_Types (Introduced in version 19.1)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Maintenance_Type_Id](#maintenance_type_id)|`uniqueidentifier` `PK`||
|[Maintenance_Type_Code](#maintenance_type_code)|`nvarchar(16)` |Unique code of the maintenance type.|
|[Maintenance_Type_Group_Id](#maintenance_type_group_id)|`uniqueidentifier` |The group, to which this maintenance type belongs.|
|[Maintenance_Type_Name](#maintenance_type_name)|`nvarchar(254)` `ML`|Multilanguage name of the maintenance type.|
|[Description](#description)|`nvarchar(2147483647)` `ML`|Detailed description of the maintenance (multilanguage).|
|[Default_Schedule_Months](#default_schedule_months)|`int` |Specifies the maximum number of months between two maintenances. NULL means that there is no default schedule in months.|
|[Default_Schedule_Days](#default_schedule_days)|`int` |Specifies the maximum number of days between two maintenances (in addition to the number of months specified in Default Schedule Months). NULL means that there is no default schedule in days.|
|[Tracked_Parameter_Id](#tracked_parameter_id)|`uniqueidentifier` |Specifies the parameter, on which the next scheduled maintenance will be based. NULL means that there is no default schedule, based on parameter.|
|[Default_Parameter_Change](#default_parameter_change)|`int` |Default positive change of the tracked parameter between two maintenances. NULL means, that maintenances are not scheduled based on parameter change.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Maintenance_Type_Id


Maintenance_Type_Id

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
|Derived From|[Eam_Maintenance_Types](Eam_Maintenance_Types.md).[Maintenance_Type_Id](Eam_Maintenance_Types.md#maintenance_type_id)|
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

### Maintenance_Type_Code


Maintenance_Type_Code


Unique code of the maintenance type.


Unique code of the maintenance type.

| Property | Value |
| - | - |
|Type|nvarchar(16)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|yes|
|Attributes|None|
|Default Value|None|
|Derived From|[Eam_Maintenance_Types](Eam_Maintenance_Types.md).[Maintenance_Type_Code](Eam_Maintenance_Types.md#maintenance_type_code)|
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
|Max Length|16|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|yes|
|Like|None|no|no|

### Maintenance_Type_Group_Id


Maintenance_Type_Group_Id


The group, to which this maintenance type belongs.


The group, to which this maintenance type belongs.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Eam_Maintenance_Type_Groups](Eam_Maintenance_Type_Groups.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Eam_Maintenance_Types](Eam_Maintenance_Types.md).[Maintenance_Type_Group_Id](Eam_Maintenance_Types.md#maintenance_type_group_id)|
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

### Maintenance_Type_Name


Maintenance_Type_Name


Multilanguage name of the maintenance type.


Multilanguage name of the maintenance type.

| Property | Value |
| - | - |
|Type|nvarchar(254)|
|Is Mulitlanguage|yes|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Eam_Maintenance_Types](Eam_Maintenance_Types.md).[Maintenance_Type_Name](Eam_Maintenance_Types.md#maintenance_type_name)|
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
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|yes|
|Like|None|no|no|

### Description


Description


Detailed description of the maintenance (multilanguage).


Detailed description of the maintenance (multilanguage).

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|
|Is Mulitlanguage|yes|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Eam_Maintenance_Types](Eam_Maintenance_Types.md).[Description](Eam_Maintenance_Types.md#description)|
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

### Default_Schedule_Months


Default_Schedule_Months


Specifies the maximum number of months between two maintenances. NULL means that there is no default schedule in months.


Specifies the maximum number of months between two maintenances. NULL means that there is no default schedule in months.

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
|Derived From|[Eam_Maintenance_Types](Eam_Maintenance_Types.md).[Default_Schedule_Months](Eam_Maintenance_Types.md#default_schedule_months)|
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

### Default_Schedule_Days


Default_Schedule_Days


Specifies the maximum number of days between two maintenances (in addition to the number of months specified in Default Schedule Months). NULL means that there is no default schedule in days.


Specifies the maximum number of days between two maintenances (in addition to the number of months specified in Default Schedule Months). NULL means that there is no default schedule in days.

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
|Derived From|[Eam_Maintenance_Types](Eam_Maintenance_Types.md).[Default_Schedule_Days](Eam_Maintenance_Types.md#default_schedule_days)|
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

### Tracked_Parameter_Id


Tracked_Parameter_Id


Specifies the parameter, on which the next scheduled maintenance will be based. NULL means that there is no default schedule, based on parameter.


Specifies the parameter, on which the next scheduled maintenance will be based. NULL means that there is no default schedule, based on parameter.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Eam_Tracked_Parameters](Eam_Tracked_Parameters.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Eam_Maintenance_Types](Eam_Maintenance_Types.md).[Tracked_Parameter_Id](Eam_Maintenance_Types.md#tracked_parameter_id)|
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

### Default_Parameter_Change


Default_Parameter_Change


Default positive change of the tracked parameter between two maintenances. NULL means, that maintenances are not scheduled based on parameter change.


Default positive change of the tracked parameter between two maintenances. NULL means, that maintenances are not scheduled based on parameter change.

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
|Derived From|[Eam_Maintenance_Types](Eam_Maintenance_Types.md).[Default_Parameter_Change](Eam_Maintenance_Types.md#default_parameter_change)|
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
|Derived From|[Eam_Maintenance_Types](Eam_Maintenance_Types.md).[Row_Version](Eam_Maintenance_Types.md#row_version)|
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


