# Table Prj_Resources

Contains the enterprise resources, which are available for including in projects. Entity: Prj_Resources

## Owner Tables Hierarchy

* [Gen_Enterprise_Companies](Gen_Enterprise_Companies.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Resource_Id](#resource_id)|`uniqueidentifier` `PK`||
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` |The enterprise company owning the resource|
|[Resource_Name](#resource_name)|`nvarchar(254)` ||
|[Description](#description)|`nvarchar(2147483647)` ||
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Resource_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Resource_Name

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Description

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


