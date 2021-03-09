# Query Prd_Workgroup_Shifts_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Id](#id)|`uniqueidentifier` `PK`|Unique workgroup shift Id|
|[Workgroup_Id](#workgroup_id)|`uniqueidentifier` ||
|[Shift_Name](#shift_name)|`nvarchar` |The name of the workgroup shift.|
|[Establishment_Date](#establishment_date)|`datetime` |When the workgroup shift was established. Used as minimum date when generating calendar|
|[Work_Schedule_Id](#work_schedule_id)|`uniqueidentifier` |The work schedule used to calculate the working time for the shift.|
|[Efficiency_Factor_Percent](#efficiency_factor_percent)|`decimal(3, 2)` |Efficiency factor of the routing steps for this shift, expressed as percentage|

## Columns

### Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Workgroup_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Shift_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Establishment_Date

| Property | Value |
| - | - |
|Type|datetime|

### Work_Schedule_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Efficiency_Factor_Percent

| Property | Value |
| - | - |
|Type|decimal(3, 2)|


