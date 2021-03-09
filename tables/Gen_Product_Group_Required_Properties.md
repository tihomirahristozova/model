# Table Gen_Product_Group_Required_Properties

Contains the properties, that are required to be set, when creating new products in the category and its sub-categories. Entity: Gen_Product_Group_Required_Properties

## Owner Tables Hierarchy

* [Gen_Product_Groups](Gen_Product_Groups.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Property_No](#property_no)|`int` |The consecutive number (position) of the property within the product group and its subgroups. The parent groups of each leaf group should contain only unique property numbers.|
|[Property_Id](#property_id)|`uniqueidentifier` |The property, that is required when creating new products in the group. The property is automatically added to new products, created in the group. The property should be with Entity Type = 'Product'.|
|[Default_Property_Value](#default_property_value)|`nvarchar(254)` |When not null, specifies the default value of the property, for new products in the group.|
|[Default_Property_Value_Description](#default_property_value_description)|`nvarchar(254)` |When not null, specifies the default description value of the property, for new products in the group.|
|[Required_Property_Id](#required_property_id)|`uniqueidentifier` `PK`||
|[Product_Group_Id](#product_group_id)|`uniqueidentifier` ||
|[Default_Value_Id](#default_value_id)|`uniqueidentifier` |When not null, specifies the default internal Id value of the property, for new products in the group.|
|[Required](#required)|`bit` |Specifies whether the property is required (or only suggested) to be set for new products. Suggested properties are used by product configuration and other product creation services. 1=Required, 0=Suggested.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Property_No

| Property | Value |
| - | - |
|Type|int|

### Property_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Default_Property_Value

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Default_Property_Value_Description

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Required_Property_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Group_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Default_Value_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Required

| Property | Value |
| - | - |
|Type|bit|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


