# Table Srv_Services

Contains the services, which can be performed. Entity: Srv_Services

## Summary

| Name | Type | Description |
| - | - | --- |
|[Service_Id](#service_id)|`uniqueidentifier` `PK`||
|[Service_Code](#service_code)|`nvarchar(16)` |Unique code of the service.|
|[Service_Name](#service_name)|`nvarchar(254)` |The name of the service.|
|[Measurement_Unit_Id](#measurement_unit_id)|`uniqueidentifier` |The measurement unit in which the service rendered to the customer is quantified|
|[Is_Active](#is_active)|`bit` |Indicates wheather this service is currently used.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Service_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Service_Code

| Property | Value |
| - | - |
|Type|nvarchar(16)|

### Service_Name

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Measurement_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Is_Active

| Property | Value |
| - | - |
|Type|bit|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


