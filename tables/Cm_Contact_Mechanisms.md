# Table Cm_Contact_Mechanisms

Contains contacting mechanisms - telephone numbers, addresses, web sites, etc. Contact mechanisms can be attached to parties. Currently each contact mechanism is attached to strictly one party. Entity: Cm_Contact_Mechanisms

## Summary

| Name | Type | Description |
| - | - | --- |
|[Id](#id)|`uniqueidentifier` `PK`|Unique contact mechanism Id|
|[Contact_Mechanism_Name](#contact_mechanism_name)|`nvarchar(254)` |Contact mechanism description|
|[Contact_Mechanism_Type](#contact_mechanism_type)|`nvarchar(1)` Allowed: `A`, `E`, `F`, `M`, `O`, `T`, `W`|A=Address; E=e-mail; T=Telephone|
|[Row_Version](#row_version)|`timestamp` ||
|[Geo_Point_Id](#geo_point_id)|`uniqueidentifier` |The geographical point, where the contact mechanism is situated. Null if this is unknown or N/A.|
|[Administrative_Region_Id](#administrative_region_id)|`uniqueidentifier` |The administrative region, where the contact mechanism is situated. Null if this is unknown or N/A.|

## Columns

### Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Contact_Mechanism_Name

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Contact_Mechanism_Type

| Property | Value |
| - | - |
|Type|nvarchar(1)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|

### Geo_Point_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Administrative_Region_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|


