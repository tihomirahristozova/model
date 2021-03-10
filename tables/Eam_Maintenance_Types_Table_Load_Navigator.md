# Query Eam_Maintenance_Types_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Maintenance_Type_Id](#maintenance_type_id)|`uniqueidentifier` `PK`||
|[Maintenance_Type_Code](#maintenance_type_code)|`nvarchar` |Unique code of the maintenance type.|
|[Maintenance_Type_Group_Id](#maintenance_type_group_id)|`uniqueidentifier` |The group, to which this maintenance type belongs.|
|[Maintenance_Type_Name](#maintenance_type_name)|`nvarchar` `ML`|Multilanguage name of the maintenance type.|
|[Description](#description)|`nvarchar` `ML`|Detailed description of the maintenance (multilanguage).|
|[Default_Schedule_Months](#default_schedule_months)|`int` |Specifies the maximum number of months between two maintenances. NULL means that there is no default schedule in months.|
|[Default_Schedule_Days](#default_schedule_days)|`int` |Specifies the maximum number of days between two maintenances (in addition to the number of months specified in Default Schedule Months). NULL means that there is no default schedule in days.|
|[Tracked_Parameter_Id](#tracked_parameter_id)|`uniqueidentifier` |Specifies the parameter, on which the next scheduled maintenance will be based. NULL means that there is no default schedule, based on parameter.|
|[Default_Parameter_Change](#default_parameter_change)|`int` |Default positive change of the tracked parameter between two maintenances. NULL means, that maintenances are not scheduled based on parameter change.|
|[Maintenance_Type_Group_Code](#maintenance_type_group_code)|`nvarchar` |Unique code of the group.|
|[Parent_Maintenance_Type_Group_Id](#parent_maintenance_type_group_id)|`uniqueidentifier` |Parent group. NULL denotes a root group.|
|[Maintenance_Type_Group_Name](#maintenance_type_group_name)|`nvarchar` `ML`|Multilanguage name of the group.|
|[Notes](#notes)|`nvarchar` ||

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
|Order|0|
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
|Type|nvarchar|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
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
|Max Length|-1|
|Order|1|
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
|Order|2|
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
|Type|nvarchar|
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
|Max Length|-1|
|Order|3|
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
|Type|nvarchar|
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
|Max Length|-1|
|Order|4|
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
|Order|5|
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
|Order|6|
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
|Order|7|
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
|Order|8|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Maintenance_Type_Group_Code


Maintenance_Type_Group_Code


Unique code of the group.


Unique code of the group.

| Property | Value |
| - | - |
|Type|nvarchar|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Eam_Maintenance_Type_Groups](Eam_Maintenance_Type_Groups.md).[Maintenance_Type_Group_Code](Eam_Maintenance_Type_Groups.md#maintenance_type_group_code)|
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
|Order|9|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|yes|
|Like|None|no|no|

### Parent_Maintenance_Type_Group_Id


Parent_Maintenance_Type_Group_Id


Parent group. NULL denotes a root group.


Parent group. NULL denotes a root group.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Eam_Maintenance_Type_Groups](Eam_Maintenance_Type_Groups.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Eam_Maintenance_Type_Groups](Eam_Maintenance_Type_Groups.md).[Parent_Maintenance_Type_Group_Id](Eam_Maintenance_Type_Groups.md#parent_maintenance_type_group_id)|
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
|Order|10|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Maintenance_Type_Group_Name


Maintenance_Type_Group_Name


Multilanguage name of the group.


Multilanguage name of the group.

| Property | Value |
| - | - |
|Type|nvarchar|
|Is Mulitlanguage|yes|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Eam_Maintenance_Type_Groups](Eam_Maintenance_Type_Groups.md).[Maintenance_Type_Group_Name](Eam_Maintenance_Type_Groups.md#maintenance_type_group_name)|
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
|Order|11|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|yes|
|Like|None|no|no|

### Notes


Notes

| Property | Value |
| - | - |
|Type|nvarchar|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Eam_Maintenance_Type_Groups](Eam_Maintenance_Type_Groups.md).[Notes](Eam_Maintenance_Type_Groups.md#notes)|
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
|Order|12|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|


