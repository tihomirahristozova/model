# Query Eam_Managed_Asset_Parameter_Values_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Managed_Asset_Parameter_Value_Id](#managed_asset_parameter_value_id)|`uniqueidentifier` `PK`||
|[Managed_Asset_Id](#managed_asset_id)|`uniqueidentifier` |The managed asset for which the parameter value is recorded.|
|[Tracked_Parameter_Id](#tracked_parameter_id)|`uniqueidentifier` |The paramater, whose value is recorded.|
|[Time_Utc](#time_utc)|`datetime` |The date and time for which the parameter value is recorded.|
|[Value](#value)|`int` |The value of the parameter for the specified time.|
|[Notes](#notes)|`nvarchar` ||
|[Tracked_Parameter_Code](#tracked_parameter_code)|`nvarchar` |Unique code of the asset parameter.|
|[Tracked_Parameter_Name](#tracked_parameter_name)|`nvarchar` `ML`|Multilanguage name of the asset parameter.|
|[Tracked_Parameter_Notes](#tracked_parameter_notes)|`nvarchar` ||
|[Is_Active](#is_active)|`bit` |Specifies whether the parameter is active for choosing in drop downs.|
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` |The enterprise company to which the managed asset belongs.|
|[Managed_Asset_Code](#managed_asset_code)|`nvarchar` |Unique code of the managed asset. The code is unique among all managed assets in the same enterprise company.|
|[Managed_Asset_Name](#managed_asset_name)|`nvarchar` `ML`|Name of the managed asset (multi-language).|
|[Managed_Asset_Type_Id](#managed_asset_type_id)|`uniqueidentifier` |The type of the asset. Determines the tracked parameters for the asset, the applicable maintenance types, etc.|
|[Managed_Asset_Group_Id](#managed_asset_group_id)|`uniqueidentifier` |The organizational group of the asset. Used for organizational purposes only.|
|[Registration_Number](#registration_number)|`nvarchar` |Registration number of the asset with the national registration authorities. NULL means the registation number is unknown or N/A.|
|[Managed_Asset_Notes](#managed_asset_notes)|`nvarchar` ||

## Columns

### Managed_Asset_Parameter_Value_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Managed_Asset_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Tracked_Parameter_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Time_Utc

| Property | Value |
| - | - |
|Type|datetime|

### Value

| Property | Value |
| - | - |
|Type|int|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar|

### Tracked_Parameter_Code

| Property | Value |
| - | - |
|Type|nvarchar|

### Tracked_Parameter_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Tracked_Parameter_Notes

| Property | Value |
| - | - |
|Type|nvarchar|

### Is_Active

| Property | Value |
| - | - |
|Type|bit|

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


