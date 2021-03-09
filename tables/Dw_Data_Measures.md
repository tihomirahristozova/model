# Table Dw_Data_Measures

Contains the data measures of the General data warehouse. Entity: Dw_Data_Measures (Introduced in version 18.2)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Data_Measure_Id](#data_measure_id)|`uniqueidentifier` `PK`||
|[Data_Measure_Code](#data_measure_code)|`nvarchar(16)` |Unique measure code.|
|[Data_Measure_Group_Id](#data_measure_group_id)|`uniqueidentifier` |The group to which this measure belongs.|
|[Data_Measure_Name](#data_measure_name)|`nvarchar(254)` |The name of the measure (multilanguage).|
|[Period](#period)|`nvarchar(1)` Allowed: `D`, `M`, `Q`, `Y`|The period for which the data is collected. D=Day, M=Month, Q=Quarter, Y=Year.|
|[Green_Zone_Spread_Percent](#green_zone_spread_percent)|`decimal(3, 2)` |The plus or minus percent, by which the goal can be missed, but still considered achieved.|
|[Horizontal_Trend_Spread_Percent](#horizontal_trend_spread_percent)|`decimal(3, 2)` |The change in percents, which is considered neutral. Higher positive/negative changes are considered positive/negative trends.|
|[Notes](#notes)|`nvarchar(2147483647)` ||

## Columns

### Data_Measure_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Data_Measure_Code

| Property | Value |
| - | - |
|Type|nvarchar(16)|

### Data_Measure_Group_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Data_Measure_Name

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Period

| Property | Value |
| - | - |
|Type|nvarchar(1)|

### Green_Zone_Spread_Percent

| Property | Value |
| - | - |
|Type|decimal(3, 2)|

### Horizontal_Trend_Spread_Percent

| Property | Value |
| - | - |
|Type|decimal(3, 2)|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|


