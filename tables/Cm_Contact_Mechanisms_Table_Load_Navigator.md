# Query Cm_Contact_Mechanisms_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Id](#id)|`uniqueidentifier` `PK`|Unique contact mechanism Id|
|[Contact_Mechanism_Name](#contact_mechanism_name)|`nvarchar` |Contact mechanism description|
|[Contact_Mechanism_Type](#contact_mechanism_type)|`nvarchar` Allowed: `A`, `E`, `F`, `M`, `O`, `T`, `W`|A=Address; E=e-mail; T=Telephone|
|[Row_Version](#row_version)|`timestamp` ||
|[Geo_Point_Id](#geo_point_id)|`uniqueidentifier` ||
|[Administrative_Region_Id](#administrative_region_id)|`uniqueidentifier` |The administrative region, where the contact mechanism is situated. Null if this is unknown or N/A.|

## Columns

### Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Contact_Mechanism_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Contact_Mechanism_Type

| Property | Value |
| - | - |
|Type|nvarchar|

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


