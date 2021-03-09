# Query Eam_Service_Centers_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Service_Center_Id](#service_center_id)|`uniqueidentifier` `PK`||
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` |The enterprise company, whose assets will be maintained by the service center. When NULL, the service center can maintain assets for all enterprise companies.|
|[Party_Id](#party_id)|`uniqueidentifier` |The person or company, actually performing the maintenance.|
|[Notes](#notes)|`nvarchar` ||
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Service_Center_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


