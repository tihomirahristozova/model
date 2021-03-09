# Table Gen_Product_Group_Range_Properties

When specified for a product group, provides a way for automatical creation of new products, based on altering a set of values of some user-defined properties. Each value combination is used to create a new, unique product within the group. Entity: Gen_Product_Group_Range_Properties

## Owner Tables Hierarchy

* [Gen_Product_Groups](Gen_Product_Groups.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Range_Property_Id](#range_property_id)|`uniqueidentifier` `PK`||
|[Product_Group_Id](#product_group_id)|`uniqueidentifier` ||
|[Property_Id](#property_id)|`uniqueidentifier` |The property whose values will be altered.|
|[Range_Type](#range_type)|`nvarchar(1)` Allowed: `R`, `L`|Specifies the method of the creation of the value set: R - by range from-to; E - by enumeration of all values;|
|[From_Property_Value](#from_property_value)|`nvarchar(254)` |Starting value of the range of alternative values. Used only when Rage Type = R (range).|
|[To_Property_Value](#to_property_value)|`nvarchar(254)` |Ending value of the range of alternative values. Used only when Rage Type = R (range).|
|[Property_Values_List](#property_values_list)|`nvarchar(2147483647)` |Contains the enumeration of all values in the alternating value set. Used only when Rage Type = E (enumeratio).|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Range_Property_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Group_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Property_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Range_Type

| Property | Value |
| - | - |
|Type|nvarchar(1)|

### From_Property_Value

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### To_Property_Value

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Property_Values_List

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


