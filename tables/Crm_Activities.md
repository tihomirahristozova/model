# Table Crm_Activities

Marketing activity, part of a marketing campaign. Entity: Crm_Activities

## Owner Tables Hierarchy

* [Cm_Activities](Cm_Activities.md)
* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Crm_Activity_Id](#crm_activity_id)|`uniqueidentifier` `PK`||
|[Activity_Id](#activity_id)|`uniqueidentifier` |The Activity, on which the current marketing activity is based|
|[Campaign_Id](#campaign_id)|`uniqueidentifier` |The marketing campaing, to which this activity belongs|
|[Target_Group_Id](#target_group_id)|`uniqueidentifier` |The target group of parties to be treated by this activity|
|[Forecasted_Cost](#forecasted_cost)|`decimal(18, 0)` |Forecasted cost of the activity in base currency|
|[Activities_Created](#activities_created)|`bit` |1 if the related activites are already created. Related activity can be created for each member of the target group.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Crm_Activity_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Activity_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Campaign_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Target_Group_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Forecasted_Cost

| Property | Value |
| - | - |
|Type|decimal(18, 0)|

### Activities_Created

| Property | Value |
| - | - |
|Type|bit|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


