# Table Eam_Managed_Asset_Scheduled_Maintenances

Contains the scheduled maintenances for the managed assets. Each maintenance can be planned based on date, parameter value or both. Past maintenance plans are kept only for reference and can be deleted at any time. Entity: Eam_Managed_Asset_Scheduled_Maintenances (Introduced in version 19.1)

## Owner Tables Hierarchy

* [Eam_Managed_Assets](Eam_Managed_Assets.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Managed_Asset_Scheduled_Maintenance_Id](#managed_asset_scheduled_maintenance_id)|`uniqueidentifier` `PK`||
|[Managed_Asset_Id](#managed_asset_id)|`uniqueidentifier` |The asset, which will be maintained.|
|[Maintenance_Type_Id](#maintenance_type_id)|`uniqueidentifier` |The type of maintenance, which will be performed.|
|[Date](#date)|`date` |The date, when the maintenance is planned. NULL means, that the plan is not related to date, but to tracked parameter value. If both date and parameter are specified, the maintenance is performed when any of the conditions is met.|
|[Tracked_Parameter_Value](#tracked_parameter_value)|`int` |The value of the tracked parameter (as specified in the maintenance type) at which the maintenance will be performed. For example, for a car, we can schedule maintenance at 20,000 km mileage. NULL means, that the maintenance is not planned based on parameter, but rather only for date. If both date and parameter are specified, the maintenance is performed when any of the conditions is met.|
|[Is_Dismissed](#is_dismissed)|`bit` |Specifies whether the notification for the maintenance is dismissed and the planner has decided the course of action.|
|[Notes](#notes)|`nvarchar(2147483647)` ||
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Managed_Asset_Scheduled_Maintenance_Id


Managed_Asset_Scheduled_Maintenance_Id

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
|Derived From|[Eam_Managed_Asset_Scheduled_Maintenances](Eam_Managed_Asset_Scheduled_Maintenances.md).[Managed_Asset_Scheduled_Maintenance_Id](Eam_Managed_Asset_Scheduled_Maintenances.md#managed_asset_scheduled_maintenance_id)|
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

### Managed_Asset_Id


Managed_Asset_Id


The asset, which will be maintained.


The asset, which will be maintained.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|yes|
|Referenced Table|[Eam_Managed_Assets](Eam_Managed_Assets.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Eam_Managed_Asset_Scheduled_Maintenances](Eam_Managed_Asset_Scheduled_Maintenances.md).[Managed_Asset_Id](Eam_Managed_Asset_Scheduled_Maintenances.md#managed_asset_id)|
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

### Maintenance_Type_Id


Maintenance_Type_Id


The type of maintenance, which will be performed.


The type of maintenance, which will be performed.

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
|Derived From|[Eam_Managed_Asset_Scheduled_Maintenances](Eam_Managed_Asset_Scheduled_Maintenances.md).[Maintenance_Type_Id](Eam_Managed_Asset_Scheduled_Maintenances.md#maintenance_type_id)|
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

### Date


Date


The date, when the maintenance is planned. NULL means, that the plan is not related to date, but to tracked parameter value. If both date and parameter are specified, the maintenance is performed when any of the conditions is met.


The date, when the maintenance is planned. NULL means, that the plan is not related to date, but to tracked parameter value. If both date and parameter are specified, the maintenance is performed when any of the conditions is met.

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
|Derived From|[Eam_Managed_Asset_Scheduled_Maintenances](Eam_Managed_Asset_Scheduled_Maintenances.md).[Date](Eam_Managed_Asset_Scheduled_Maintenances.md#date)|
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
|GreaterThanOrLessThan|None|yes|no|

### Tracked_Parameter_Value


Tracked_Parameter_Value


The value of the tracked parameter (as specified in the maintenance type) at which the maintenance will be performed. For example, for a car, we can schedule maintenance at 20,000 km mileage. NULL means, that the maintenance is not planned based on parameter, but rather only for date. If both date and parameter are specified, the maintenance is performed when any of the conditions is met.


The value of the tracked parameter (as specified in the maintenance type) at which the maintenance will be performed. For example, for a car, we can schedule maintenance at 20,000 km mileage. NULL means, that the maintenance is not planned based on parameter, but rather only for date. If both date and parameter are specified, the maintenance is performed when any of the conditions is met.

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
|Derived From|[Eam_Managed_Asset_Scheduled_Maintenances](Eam_Managed_Asset_Scheduled_Maintenances.md).[Tracked_Parameter_Value](Eam_Managed_Asset_Scheduled_Maintenances.md#tracked_parameter_value)|
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
|GreaterThanOrLessThan|None|no|no|

### Is_Dismissed


Is_Dismissed


Specifies whether the notification for the maintenance is dismissed and the planner has decided the course of action.


Specifies whether the notification for the maintenance is dismissed and the planner has decided the course of action.

| Property | Value |
| - | - |
|Type|bit|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|False|
|Derived From|[Eam_Managed_Asset_Scheduled_Maintenances](Eam_Managed_Asset_Scheduled_Maintenances.md).[Is_Dismissed](Eam_Managed_Asset_Scheduled_Maintenances.md#is_dismissed)|
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
|Attributes|None, IsLongString|
|Default Value|None|
|Derived From|[Eam_Managed_Asset_Scheduled_Maintenances](Eam_Managed_Asset_Scheduled_Maintenances.md).[Notes](Eam_Managed_Asset_Scheduled_Maintenances.md#notes)|
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
|Derived From|[Eam_Managed_Asset_Scheduled_Maintenances](Eam_Managed_Asset_Scheduled_Maintenances.md).[Row_Version](Eam_Managed_Asset_Scheduled_Maintenances.md#row_version)|
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


