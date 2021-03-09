# Query Gen_Resource_Instances_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Resource_Instance_Id](#resource_instance_id)|`uniqueidentifier` `PK`||
|[Resource_Id](#resource_id)|`uniqueidentifier` |The resource of which this is instance.|
|[Resource_Instance_Name](#resource_instance_name)|`nvarchar` ||
|[Resource_Instance_Code](#resource_instance_code)|`nvarchar` ||
|[Notes](#notes)|`nvarchar` ||
|[Party_Id](#party_id)|`uniqueidentifier` |The party, which is represented by this resource instance. NULL, when the resource instance is not a party.|
|[Asset_Id](#asset_id)|`uniqueidentifier` |The asset, which is represented by this resource instance. NULL, when the resource instance is not an asset.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Resource_Instance_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Resource_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Resource_Instance_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Resource_Instance_Code

| Property | Value |
| - | - |
|Type|nvarchar|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar|

### Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Asset_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


