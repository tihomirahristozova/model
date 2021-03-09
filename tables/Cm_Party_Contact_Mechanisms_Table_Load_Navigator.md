# Query Cm_Party_Contact_Mechanisms_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Id](#id)|`uniqueidentifier` `PK`||
|[Party_Id](#party_id)|`uniqueidentifier` ||
|[Party_Name](#party_name)|`nvarchar` `ML`||
|[Contact_Mechanism_Id](#contact_mechanism_id)|`uniqueidentifier` ||
|[Contact_Mechanism_Name](#contact_mechanism_name)|`nvarchar` ||
|[Contact_Mechanism_Type](#contact_mechanism_type)|`nvarchar` Allowed: `A`, `E`, `F`, `M`, `O`, `T`, `W`||
|[From_Date](#from_date)|`datetime` ||
|[Thru_Date](#thru_date)|`datetime` ||
|[Non_Solicitation](#non_solicitation)|`bit` ||
|[Notes](#notes)|`nvarchar` ||
|[Is_Default](#is_default)|`bit` ||
|[Is_Active](#is_active)|`bit` ||
|[Geo_Point_Id](#geo_point_id)|`uniqueidentifier` |The geographical point, where the contact mechanism is situated. Null if this is unknown or N/A.|
|[Administrative_Region_Id](#administrative_region_id)|`uniqueidentifier` |The administrative region, where the contact mechanism is situated. Null if this is unknown or N/A.|
|[Line_Ord](#line_ord)|`int` ||
|[Contact_Mechanism_Purpose_Id](#contact_mechanism_purpose_id)|`uniqueidentifier` ||
|[Parent_Party_Id](#parent_party_id)|`uniqueidentifier` ||
|[Party_Type](#party_type)|`nvarchar` Allowed: `C`, `L`, `P`, `S`, `V`||

## Columns

### Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Party_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Contact_Mechanism_Id

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

### From_Date

| Property | Value |
| - | - |
|Type|datetime|

### Thru_Date

| Property | Value |
| - | - |
|Type|datetime|

### Non_Solicitation

| Property | Value |
| - | - |
|Type|bit|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar|

### Is_Default

| Property | Value |
| - | - |
|Type|bit|

### Is_Active

| Property | Value |
| - | - |
|Type|bit|

### Geo_Point_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Administrative_Region_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Line_Ord

| Property | Value |
| - | - |
|Type|int|

### Contact_Mechanism_Purpose_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Parent_Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Party_Type

| Property | Value |
| - | - |
|Type|nvarchar|


