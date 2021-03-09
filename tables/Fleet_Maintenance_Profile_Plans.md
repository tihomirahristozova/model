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

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Maintenance_Profile_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Maintenance_Plan_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Is_Active

| Property | Value |
| - | - |
|Type|bit|


