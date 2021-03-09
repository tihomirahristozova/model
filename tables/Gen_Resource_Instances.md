# Table Gen_Resource_Instances

Represents concrete instances of resources. Entity: Gen_Resource_Instances

## Owner Tables Hierarchy

* [Gen_Resources](Gen_Resources.md)
* [Gen_Resource_Groups](Gen_Resource_Groups.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Resource_Instance_Id](#resource_instance_id)|`uniqueidentifier` `PK`||
|[Resource_Id](#resource_id)|`uniqueidentifier` |The resource of which this is instance.|
|[Resource_Instance_Name](#resource_instance_name)|`nvarchar(2147483647)` |Multilanguage resource instance name.|
|[Resource_Instance_Code](#resource_instance_code)|`nvarchar(16)` |Code of the instance, unique within the resource.|
|[Notes](#notes)|`nvarchar(2147483647)` ||
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
|Type|nvarchar(2147483647)|

### Resource_Instance_Code

| Property | Value |
| - | - |
|Type|nvarchar(16)|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

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


