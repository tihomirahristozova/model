# Table Prj_Project_Risks

Contains risks, associated to projects. Entity: Prj_Project_Risks

## Owner Tables Hierarchy

* [Prj_Projects](Prj_Projects.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Project_Risk_Id](#project_risk_id)|`uniqueidentifier` `PK`||
|[Project_Id](#project_id)|`uniqueidentifier` |The project for which this risk applies.|
|[Risk_Name](#risk_name)|`nvarchar(254)` |The short name of the risk.|
|[Description](#description)|`nvarchar(2147483647)` ||
|[Create_Date](#create_date)|`date` |The creation date of the project risk.|
|[Probability_Percent](#probability_percent)|`decimal(3, 2)` |The probability of the risk occurring.|
|[Impact_Percent](#impact_percent)|`decimal(3, 2)` |The impact of the risk to the project, expressed as percentage of the total project value.|
|[Responsible_Person_Id](#responsible_person_id)|`uniqueidentifier` |The person who is responsible for handling the risk|
|[Resolution_Strategy](#resolution_strategy)|`nvarchar(2147483647)` |The strategy chosen to handle the risk|
|[Resolved](#resolved)|`bit` |1 if the risk is resolved|
|[Resolve_Date](#resolve_date)|`date` |The date on which the risk is resolved|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Project_Risk_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Project_Id

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

### Create_Date

| Property | Value |
| - | - |
|Type|date|

### Probability_Percent

| Property | Value |
| - | - |
|Type|decimal(3, 2)|

### Impact_Percent

| Property | Value |
| - | - |
|Type|decimal(3, 2)|

### Responsible_Person_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Resolution_Strategy

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Resolved

| Property | Value |
| - | - |
|Type|bit|

### Resolve_Date

| Property | Value |
| - | - |
|Type|date|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


