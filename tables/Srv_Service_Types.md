# Table Srv_Service_Types

Service levels. Entity: Srv_Service_Types

## Summary

| Name | Type | Description |
| - | - | --- |
|[Service_Type_Id](#service_type_id)|`uniqueidentifier` `PK`||
|[Service_Object_Type_Id](#service_object_type_id)|`uniqueidentifier` |The service object type to which this service type is applicable|
|[Service_Type_Name](#service_type_name)|`nvarchar(254)` ||
|[Is_Default](#is_default)|`bit` |1 when this is the default service type for the service object type. 0 otherwise|
|[Description](#description)|`nvarchar(2147483647)` ||
|[Price_List_Id](#price_list_id)|`uniqueidentifier` |When not NULL, specifies the price list that should be applied when invoicing service activities|
|[Is_Active](#is_active)|`bit` |True when the service type is currently active and selectable in new documents.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Service_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Service_Object_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Service_Type_Name

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Is_Default

| Property | Value |
| - | - |
|Type|bit|

### Description

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Price_List_Id

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


