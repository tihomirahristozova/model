# Table Crm_Campaigns

Marketing campaigns. Used to treat target groups with marketing messages, plan budgets and marketing activities. Entity: Crm_Campaigns

## Summary

| Name | Type | Description |
| - | - | --- |
|[Campaign_Id](#campaign_id)|`uniqueidentifier` `PK`||
|[Campaign_Name](#campaign_name)|`nvarchar(64)` |Short name of the campaign|
|[Description](#description)|`nvarchar(254)` |Campaign description|
|[Start_Date](#start_date)|`datetime` |Starting date of the campaign|
|[End_Date](#end_date)|`datetime` |End date of the campaign. NULL means that the end date is still unknown|
|[Forecasted_Cost](#forecasted_cost)|`decimal(18, 0)` |Forecasted total cost of the campaign|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Campaign_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Campaign_Name

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### Description

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Start_Date

| Property | Value |
| - | - |
|Type|datetime|

### End_Date

| Property | Value |
| - | - |
|Type|datetime|

### Forecasted_Cost

| Property | Value |
| - | - |
|Type|decimal(18, 0)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


