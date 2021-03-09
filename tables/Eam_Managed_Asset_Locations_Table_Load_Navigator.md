# Query Eam_Managed_Asset_Locations_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Managed_Asset_Location_Id](#managed_asset_location_id)|`uniqueidentifier` `PK`||
|[Managed_Asset_Id](#managed_asset_id)|`uniqueidentifier` |The asset, whose location is recorded.|
|[Enterprise_Company_Location_Id](#enterprise_company_location_id)|`uniqueidentifier` |The enterprise company location, where the asset is assigned.|
|[From_Date](#from_date)|`date` |The date on which the asset is assigned to the location.|
|[Responsible_Person_Id](#responsible_person_id)|`uniqueidentifier` |The responsible person, to which the asset is assigned. NULL when the asset is not assigned to any particular responsible person.|
|[Notes](#notes)|`nvarchar` |Might contain additional notes for the exact location of the asset within the enterprise company location.|
|[Party_Id](#party_id)|`uniqueidentifier` |The party of the company location.|
|[Company_Id](#company_id)|`uniqueidentifier` |The company to which this location belongs.|
|[Location_Name](#location_name)|`nvarchar` `ML`|The name of the company location.|
|[Working_Time](#working_time)|`nvarchar` |Textual representation of the working time of the location.|
|[Bill_To](#bill_to)|`nvarchar` Allowed: `C`, `L`|If filled indicates which party is billed for the amounts from documents that require payments. This setting is used in CRM module when the company and the location are customers. Possible values: 'C' = Company, 'L' = Company location, NULL = unidentified|
|[Access_Key_Id](#access_key_id)|`uniqueidentifier` ||
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` |The enterprise company to which the managed asset belongs.|
|[Managed_Asset_Code](#managed_asset_code)|`nvarchar` |Unique code of the managed asset. The code is unique among all managed assets in the same enterprise company.|
|[Managed_Asset_Name](#managed_asset_name)|`nvarchar` `ML`|Name of the managed asset (multi-language).|
|[Managed_Asset_Type_Id](#managed_asset_type_id)|`uniqueidentifier` |The type of the asset. Determines the tracked parameters for the asset, the applicable maintenance types, etc.|
|[Managed_Asset_Group_Id](#managed_asset_group_id)|`uniqueidentifier` |The organizational group of the asset. Used for organizational purposes only.|
|[Registration_Number](#registration_number)|`nvarchar` |Registration number of the asset with the national registration authorities. NULL means the registation number is unknown or N/A.|
|[Managed_Asset_Notes](#managed_asset_notes)|`nvarchar` ||

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
|Type|nvarchar|

### Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Location_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Working_Time

| Property | Value |
| - | - |
|Type|nvarchar|

### Bill_To

| Property | Value |
| - | - |
|Type|nvarchar|

### Access_Key_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Managed_Asset_Code

| Property | Value |
| - | - |
|Type|nvarchar|

### Managed_Asset_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Managed_Asset_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Managed_Asset_Group_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Registration_Number

| Property | Value |
| - | - |
|Type|nvarchar|

### Managed_Asset_Notes

| Property | Value |
| - | - |
|Type|nvarchar|


