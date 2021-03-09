# Table Rent_Asset_Type_Properties

Contains the properties, which are required for each asset category. Entity: Rent_Asset_Type_Properties

## Owner Tables Hierarchy

* [Rent_Asset_Types](Rent_Asset_Types.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Rental_Asset_Type_Property_Id](#rental_asset_type_property_id)|`uniqueidentifier` `PK`||
|[Rental_Asset_Type_Id](#rental_asset_type_id)|`uniqueidentifier` ||
|[Property_Id](#property_id)|`uniqueidentifier` |The user-defined property, which is required for assets of the specified type.|
|[Default_Value](#default_value)|`nvarchar(254)` |The default value of the property.|
|[Default_Value_Id](#default_value_id)|`uniqueidentifier` |The value id of the default value of the property.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Rental_Asset_Type_Property_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Rental_Asset_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Property_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Default_Value

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Default_Value_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


