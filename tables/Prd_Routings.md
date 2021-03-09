# Table Prd_Routings


## Summary

| Name | Type | Description |
| - | - | --- |
|[Id](#id)|`uniqueidentifier` `PK`||
|[Product_Group_Id](#product_group_id)|`uniqueidentifier` |The group of production items that can use the routing|
|[Routing_Name](#routing_name)|`nvarchar(64)` ||
|[Is_Shared](#is_shared)|`bit` |1 if the routing can be used by many recipes, 0 if the routing is privately used by recipe and/or recipe model.|
|[Release_Date](#release_date)|`datetime` |The date, when the route is released for use|
|[Expiry_Date](#expiry_date)|`datetime` |The last date, when the route should be used. NULL means that the route might still be in use|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Group_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Routing_Name

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### Is_Shared

| Property | Value |
| - | - |
|Type|bit|

### Release_Date

| Property | Value |
| - | - |
|Type|datetime|

### Expiry_Date

| Property | Value |
| - | - |
|Type|datetime|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


