# Query Eam_Managed_Asset_Type_Maintenance_Types_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Managed_Asset_Type_Maintenance_Type_Id](#managed_asset_type_maintenance_type_id)|`uniqueidentifier` `PK`||
|[Managed_Asset_Type_Id](#managed_asset_type_id)|`uniqueidentifier` |The asset type for which the allowed maintenance type is defined.|
|[Maintenance_Type_Id](#maintenance_type_id)|`uniqueidentifier` |The allowed maintenance type for the asset type.|
|[Default_Schedule_Months](#default_schedule_months)|`int` |Specifies the number of months between two maintenances. When not null, this schedule is taken with priority related to the general maintenance type schedule. NULL means that there is no default schedule in months.|
|[Default_Schedule_Days](#default_schedule_days)|`int` |Specifies the maximum number of days between two maintenances (in addition to the number of months specified in Default Schedule Months). When not null, this schedule is taken with priority related to the general maintenance type schedule. NULL means that there is no default schedule in days.|
|[Default_Parameter_Change](#default_parameter_change)|`int` |Default positive change of the tracked parameter between two maintenances. When not null, this schedule is taken with priority related to the general maintenance type schedule. NULL means, that maintenances are not scheduled based on parameter change.|
|[Notes](#notes)|`nvarchar` ||

## Columns

### Managed_Asset_Type_Maintenance_Type_Id


Managed_Asset_Type_Maintenance_Type_Id

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
|Derived From|[Eam_Managed_Asset_Type_Maintenance_Types](Eam_Managed_Asset_Type_Maintenance_Types.md).[Managed_Asset_Type_Maintenance_Type_Id](Eam_Managed_Asset_Type_Maintenance_Types.md#managed_asset_type_maintenance_type_id)|
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

### Managed_Asset_Type_Id


Managed_Asset_Type_Id


The asset type for which the allowed maintenance type is defined.


The asset type for which the allowed maintenance type is defined.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Eam_Managed_Asset_Types](Eam_Managed_Asset_Types.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Eam_Managed_Asset_Type_Maintenance_Types](Eam_Managed_Asset_Type_Maintenance_Types.md).[Managed_Asset_Type_Id](Eam_Managed_Asset_Type_Maintenance_Types.md#managed_asset_type_id)|
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

### Maintenance_Type_Id


Maintenance_Type_Id


The allowed maintenance type for the asset type.


The allowed maintenance type for the asset type.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Eam_Maintenance_Types](Eam_Maintenance_Types.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Eam_Managed_Asset_Type_Maintenance_Types](Eam_Managed_Asset_Type_Maintenance_Types.md).[Maintenance_Type_Id](Eam_Managed_Asset_Type_Maintenance_Types.md#maintenance_type_id)|
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

### Default_Schedule_Months


Default_Schedule_Months


Specifies the number of months between two maintenances. When not null, this schedule is taken with priority related to the general maintenance type schedule. NULL means that there is no default schedule in months.


Specifies the number of months between two maintenances. When not null, this schedule is taken with priority related to the general maintenance type schedule. NULL means that there is no default schedule in months.

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
|Derived From|[Eam_Managed_Asset_Type_Maintenance_Types](Eam_Managed_Asset_Type_Maintenance_Types.md).[Default_Schedule_Months](Eam_Managed_Asset_Type_Maintenance_Types.md#default_schedule_months)|
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


Specifies the maximum number of days between two maintenances (in addition to the number of months specified in Default Schedule Months). When not null, this schedule is taken with priority related to the general maintenance type schedule. NULL means that there is no default schedule in days.


Specifies the maximum number of days between two maintenances (in addition to the number of months specified in Default Schedule Months). When not null, this schedule is taken with priority related to the general maintenance type schedule. NULL means that there is no default schedule in days.

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
|Derived From|[Eam_Managed_Asset_Type_Maintenance_Types](Eam_Managed_Asset_Type_Maintenance_Types.md).[Default_Schedule_Days](Eam_Managed_Asset_Type_Maintenance_Types.md#default_schedule_days)|
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

### Default_Parameter_Change


Default_Parameter_Change


Default positive change of the tracked parameter between two maintenances. When not null, this schedule is taken with priority related to the general maintenance type schedule. NULL means, that maintenances are not scheduled based on parameter change.


Default positive change of the tracked parameter between two maintenances. When not null, this schedule is taken with priority related to the general maintenance type schedule. NULL means, that maintenances are not scheduled based on parameter change.

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
|Derived From|[Eam_Managed_Asset_Type_Maintenance_Types](Eam_Managed_Asset_Type_Maintenance_Types.md).[Default_Parameter_Change](Eam_Managed_Asset_Type_Maintenance_Types.md#default_parameter_change)|
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
|Derived From|[Eam_Managed_Asset_Type_Maintenance_Types](Eam_Managed_Asset_Type_Maintenance_Types.md).[Notes](Eam_Managed_Asset_Type_Maintenance_Types.md#notes)|
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


