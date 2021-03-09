# Table Fleet_Maintenance_Profiles

Profiles contain multiple maintenance plans and can be assigned directly to a vehicle. Entity: Fleet_Maintenance_Profiles

## Summary

| Name | Type | Description |
| - | - | --- |
|[Maintenance_Profile_Id](#maintenance_profile_id)|`uniqueidentifier` `PK`||
|[Maintenance_Profile_Code](#maintenance_profile_code)|`nvarchar(16)` ||
|[Maintenance_Profile_Name](#maintenance_profile_name)|`nvarchar(254)` |Name of the maintenance profile (Multilanguage).|
|[Notes](#notes)|`nvarchar(2147483647)` ||
|[Is_Active](#is_active)|`bit` |1 if the profile is active and can be assigned to vehicles. However, if a profile is already assigned to a vehicle, it will still work even if it is de-activated.|

## Columns

### Maintenance_Profile_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Maintenance_Profile_Code

| Property | Value |
| - | - |
|Type|nvarchar(16)|

### Maintenance_Profile_Name

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Is_Active

| Property | Value |
| - | - |
|Type|bit|


