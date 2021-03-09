# Table Inv_Stores

Represents the physical warehouses. Entity: Inv_Stores

## Owner Tables Hierarchy

* [Gen_Parties](Gen_Parties.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Id](#id)|`uniqueidentifier` `PK`|Unique store Id|
|[Party_Id](#party_id)|`uniqueidentifier` |The party of the store. Each store is a party and is stored based on a party definition.|
|[Parent_Store_Id](#parent_store_id)|`uniqueidentifier` |Obsolete. Not used. (Hierarchy of the stores is now represented by the Store Groups entity).|
|[Store_Code](#store_code)|`nvarchar(16)` ||
|[Store_Name](#store_name)|`nvarchar(254)` `ML`|Name of the store|
|[Access_Key_Id](#access_key_id)|`uniqueidentifier` ||
|[Responsible_Party_Id](#responsible_party_id)|`uniqueidentifier` |Primary responsible party (usually employee) for the stock in the store.|
|[Number_Of_Dimensions](#number_of_dimensions)|`int` |Number of dimensions in the coordinate system of the storage bins. 0 means single-bin store. Currently, this is only stored for information and is not used for automatical generation of store bins, as it was intended.|
|[Default_Store_Bin_Id](#default_store_bin_id)|`uniqueidentifier` |To be used when store bin is unknown|
|[Default_Supply_Store_Id](#default_supply_store_id)|`uniqueidentifier` |The store from which goods are usually supplied to this store|
|[Unmanaged](#unmanaged)|`bit` |If 0 the system will expect the user to process the store transactions. If 1 the system will auto-generate them|
|[Schema_XML](#schema_xml)|`nvarchar(1073741823)` |Obsolete. Not used.|
|[Currency_Id](#currency_id)|`uniqueidentifier` |The currency for the warehouse cost calculations. When NULL, the base currency for the enterprise company will be used|
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` ||
|[Creation_Time](#creation_time)|`datetime` Readonly||
|[Creation_User](#creation_user)|`nvarchar(64)` Readonly||
|[Update_Time](#update_time)|`datetime` Readonly||
|[Update_User](#update_user)|`nvarchar(64)` Readonly||
|[Enterprise_Company_Location_Id](#enterprise_company_location_id)|`uniqueidentifier` ||
|[Store_Group_Id](#store_group_id)|`uniqueidentifier` |The store group, to which this store belongs.|
|[Active](#active)|`bit` |Obsolete - Use Gen_Parties.Is_Active|
|[Row_Version](#row_version)|`timestamp` ||
|[Warehouse_Id](#warehouse_id)|`uniqueidentifier` |Specifies, the warehouse, which manages the warehouse operations for the store. NULL for stores, which do not have managed operations.|

## Columns

### Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Parent_Store_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Store_Code

| Property | Value |
| - | - |
|Type|nvarchar(16)|

### Store_Name

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Access_Key_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Responsible_Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Number_Of_Dimensions

| Property | Value |
| - | - |
|Type|int|

### Default_Store_Bin_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Default_Supply_Store_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Unmanaged

| Property | Value |
| - | - |
|Type|bit|

### Schema_XML

| Property | Value |
| - | - |
|Type|nvarchar(1073741823)|

### Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

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

### Enterprise_Company_Location_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Store_Group_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Active

| Property | Value |
| - | - |
|Type|bit|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|

### Warehouse_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|


