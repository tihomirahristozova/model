# Table Fleet_Maintenance_Profile_Plans

Contains the plans, included in the maintenance profile. Entity: Fleet_Maintenance_Profile_Plans

## Owner Tables Hierarchy

* [Fleet_Maintenance_Profiles](Fleet_Maintenance_Profiles.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Maintenance_Profile_Plan_Id](#maintenance_profile_plan_id)|`uniqueidentifier` `PK`||
|[Maintenance_Profile_Id](#maintenance_profile_id)|`uniqueidentifier` |The maintenance profile, which includes the plan.|
|[Maintenance_Plan_Id](#maintenance_plan_id)|`uniqueidentifier` |The maintenance plan, which is included in the profile.|
|[Notes](#notes)|`nvarchar(2147483647)` ||
|[Is_Active](#is_active)|`bit` |1 if the maintenance plan is active for this profile. When a plan is not active, maintenance for it will not occur for the current profile.|

## Columns

### Maintenance_Profile_Plan_Id


Maintenance_Profile_Plan_Id

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
|Derived From|[Fleet_Maintenance_Profile_Plans](Fleet_Maintenance_Profile_Plans.md).[Maintenance_Profile_Plan_Id](Fleet_Maintenance_Profile_Plans.md#maintenance_profile_plan_id)|
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

### Maintenance_Profile_Id


Maintenance_Profile_Id


The maintenance profile, which includes the plan.


The maintenance profile, which includes the plan.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|yes|
|Referenced Table|[Fleet_Maintenance_Profiles](Fleet_Maintenance_Profiles.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Fleet_Maintenance_Profile_Plans](Fleet_Maintenance_Profile_Plans.md).[Maintenance_Profile_Id](Fleet_Maintenance_Profile_Plans.md#maintenance_profile_id)|
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

### Maintenance_Plan_Id


Maintenance_Plan_Id


The maintenance plan, which is included in the profile.


The maintenance plan, which is included in the profile.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Fleet_Maintenance_Plans](Fleet_Maintenance_Plans.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Fleet_Maintenance_Profile_Plans](Fleet_Maintenance_Profile_Plans.md).[Maintenance_Plan_Id](Fleet_Maintenance_Profile_Plans.md#maintenance_plan_id)|
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
|Attributes|None|
|Default Value|None|
|Derived From|[Fleet_Maintenance_Profile_Plans](Fleet_Maintenance_Profile_Plans.md).[Notes](Fleet_Maintenance_Profile_Plans.md#notes)|
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

### Is_Active


Is_Active


1 if the maintenance plan is active for this profile. When a plan is not active, maintenance for it will not occur for the current profile.


1 if the maintenance plan is active for this profile. When a plan is not active, maintenance for it will not occur for the current profile.

| Property | Value |
| - | - |
|Type|bit|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|True|
|Derived From|[Fleet_Maintenance_Profile_Plans](Fleet_Maintenance_Profile_Plans.md).[Is_Active](Fleet_Maintenance_Profile_Plans.md#is_active)|
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


