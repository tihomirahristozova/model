# Table Fleet_Maintenance_Plans

Defines the periodic maintenance plans and the conditions for performing the next maintenance. Entity: Fleet_Maintenance_Plans

## Summary

| Name | Type | Description |
| - | - | --- |
|[Maintenance_Plan_Id](#maintenance_plan_id)|`uniqueidentifier` `PK`||
|[Maintenance_Plan_Code](#maintenance_plan_code)|`nvarchar(16)` ||
|[Maintenance_Plan_Name](#maintenance_plan_name)|`nvarchar(254)` |Maintenance plan name (Multilanguage).|
|[Check_Months](#check_months)|`int` |When not null, specifies the number of months between maintenances.|
|[Check_Days](#check_days)|`int` |When not null, specifies the number of days between maintenances.|
|[Mileage_Km](#mileage_km)|`int` |When not null, specifies the number of kilometers that must have passed since the last maintenance, for the next maintenance to occur.|
|[Trip_Count](#trip_count)|`int` |When not null, specifies the number of trips that must be performed since the last maintenance, for the next maintenance to occur.|
|[Notes](#notes)|`nvarchar(2147483647)` ||
|[Is_Active](#is_active)|`bit` |True if the plan is active and can be selected from drop-downs.|

## Columns

### Maintenance_Plan_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Maintenance_Plan_Code

| Property | Value |
| - | - |
|Type|nvarchar(16)|

### Maintenance_Plan_Name

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Check_Months

| Property | Value |
| - | - |
|Type|int|

### Check_Days

| Property | Value |
| - | - |
|Type|int|

### Mileage_Km

| Property | Value |
| - | - |
|Type|int|

### Trip_Count

| Property | Value |
| - | - |
|Type|int|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Is_Active

| Property | Value |
| - | - |
|Type|bit|


