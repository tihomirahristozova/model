# Table Pos_Locations

Defines a company location as POS enabled location. Entity: Pos_Locations (Introduced in version 19.1)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Pos_Location_Id](#pos_location_id)|`uniqueidentifier` `PK`||
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` |The enterprise company of the POS location.|
|[Enterprise_Company_Location_Id](#enterprise_company_location_id)|`uniqueidentifier` |The enterprise company location of the POS location. Currently, only one POS location is allowed for each company location.|
|[Pos_Location_Code](#pos_location_code)|`nvarchar(16)` |Unique (with the enterprise company) code of this POS location.|
|[Is_Active](#is_active)|`bit` |Indicates whether the POS location is currently active and can be chosen in drop-downs, etc.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Pos_Location_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Enterprise_Company_Location_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Pos_Location_Code

| Property | Value |
| - | - |
|Type|nvarchar(16)|

### Is_Active

| Property | Value |
| - | - |
|Type|bit|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


