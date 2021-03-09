# Table Prj_Template_Risks

Contains project risks, which will be copied to projects, based on the template. Entity: Prj_Template_Risks

## Owner Tables Hierarchy

* [Prj_Templates](Prj_Templates.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Project_Template_Risk_Id](#project_template_risk_id)|`uniqueidentifier` `PK`||
|[Project_Template_Id](#project_template_id)|`uniqueidentifier` ||
|[Risk_Name](#risk_name)|`nvarchar(254)` |The name of the risk.|
|[Description](#description)|`nvarchar(2147483647)` ||
|[Probability_Percent](#probability_percent)|`decimal(3, 2)` |The probability of the risk occurring.|
|[Impact_Percent](#impact_percent)|`decimal(3, 2)` |The impact of the risk to the project, expressed as percentage of the total project value.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Project_Template_Risk_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Project_Template_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Risk_Name

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Description

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Probability_Percent

| Property | Value |
| - | - |
|Type|decimal(3, 2)|

### Impact_Percent

| Property | Value |
| - | - |
|Type|decimal(3, 2)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


