# Table Gen_Parties

Contains base data for different kind of parties - companies, persons, departments, etc. Entity: Gen_Parties

## Summary

| Name | Type | Description |
| - | - | --- |
|[Id](#id)|`uniqueidentifier` `PK`|Unique party id|
|[Party_Name](#party_name)|`nvarchar(254)` `ML`|The name of the party|
|[Party_Type](#party_type)|`nvarchar(1)` Allowed: `C`, `L`, `P`, `S`, `V`|Type of party. Currently supported are P=Person, C=Company, S=Store, L=Company Location, V=Division|
|[Party_Code](#party_code)|`nvarchar(16)` Readonly|The unique code of the party|
|[Notes](#notes)|`nvarchar(254)` ||
|[Parent_Party_Id](#parent_party_id)|`uniqueidentifier` |Organizational unit (branch from the hierarchy of all parties) to which this party is referred to|
|[Party_Unique_Number](#party_unique_number)|`nvarchar(16)` Readonly|Unique number of the party (National number for persons, Registration number for companies)|
|[Creation_Time](#creation_time)|`datetime` Readonly||
|[Creation_User](#creation_user)|`nvarchar(64)` Readonly||
|[Update_Time](#update_time)|`datetime` Readonly||
|[Update_User](#update_user)|`nvarchar(64)` Readonly||
|[GLN](#gln)|`nvarchar(13)` |Global Location Number used by EDI systems|
|[Area_Id](#area_id)|`uniqueidentifier` |The area in which the party is situated.|
|[Default_Product_Coding_System_Id](#default_product_coding_system_id)|`uniqueidentifier` |When not null, specifies coding system for products, which is required by the party. The coding system is used primarily for document printouts and document import/exports.|
|[Administrative_Region_Id](#administrative_region_id)|`uniqueidentifier` |The administrative region in which the party is situated.|
|[Is_Active](#is_active)|`bit` |Specifies whether the current party is active in the system or not.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Party_Name

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Party_Type

| Property | Value |
| - | - |
|Type|nvarchar(1)|

### Party_Code

| Property | Value |
| - | - |
|Type|nvarchar(16)|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Parent_Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Party_Unique_Number

| Property | Value |
| - | - |
|Type|nvarchar(16)|

### Creation_Time

| Property | Value |
| - | - |
|Type|datetime|

### Creation_User

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### Update_Time

| Property | Value |
| - | - |
|Type|datetime|

### Update_User

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### GLN

| Property | Value |
| - | - |
|Type|nvarchar(13)|

### Area_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Default_Product_Coding_System_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Administrative_Region_Id

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


