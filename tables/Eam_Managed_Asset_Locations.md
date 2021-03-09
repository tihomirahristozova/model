# Table Eam_Managed_Asset_Locations

Contains the locations to which the assets are assigned at various moments in time. Entity: Eam_Managed_Asset_Locations (Introduced in version 19.1)

## Owner Tables Hierarchy

* [Eam_Managed_Assets](Eam_Managed_Assets.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Managed_Asset_Location_Id](#managed_asset_location_id)|`uniqueidentifier` `PK`||
|[Managed_Asset_Id](#managed_asset_id)|`uniqueidentifier` |The asset, whose location is recorded.|
|[Enterprise_Company_Location_Id](#enterprise_company_location_id)|`uniqueidentifier` |The enterprise company location, where the asset is assigned.|
|[From_Date](#from_date)|`date` |The date on which the asset is assigned to the location.|
|[Responsible_Person_Id](#responsible_person_id)|`uniqueidentifier` |The responsible person, to which the asset is assigned. NULL when the asset is not assigned to any particular responsible person.|
|[Notes](#notes)|`nvarchar(2147483647)` |Might contain additional notes for the exact location of the asset within the enterprise company location.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Managed_Asset_Location_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Managed_Asset_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Enterprise_Company_Location_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### From_Date

| Property | Value |
| - | - |
|Type|date|

### Responsible_Person_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


