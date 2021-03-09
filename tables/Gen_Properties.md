# Table Gen_Properties

User-defined properties, which can supplement the system properties of almost all entities in the system. Entity: Gen_Properties

## Summary

| Name | Type | Description |
| - | - | --- |
|[Property_Id](#property_id)|`uniqueidentifier` `PK`||
|[Property_Code](#property_code)|`nvarchar(40)` |Unique property code.|
|[Property_Name](#property_name)|`nvarchar(254)` `ML`||
|[Entity_Name](#entity_name)|`nvarchar(64)` |The entity for which the property is applicable.|
|[Allowed_Values_Entity_Name](#allowed_values_entity_name)|`nvarchar(64)` |When not NULL, specifies that the allowed values are retrieved from the specified entity|
|[Allowed_Values_Filter_XML](#allowed_values_filter_xml)|`nvarchar(1073741823)` |When not NULL specifies the filter to apply when extracting allowed values from entity|
|[Limit_To_Allowed_Values](#limit_to_allowed_values)|`bit` |When true, allows the property to be set only to allowed value. When false, the property can have any value.|
|[Mask_Length](#mask_length)|`smallint` |Limits te length of the property value to the specified number of characters. Null means no limitation|
|[Allowed_Values_Property_Id](#allowed_values_property_id)|`uniqueidentifier` |When not null, specifies that the current property can have the same allowed values as the specified property. Also, this makes the current and the specified property copy-compatible.|
|[Properties_Category_Id](#properties_category_id)|`uniqueidentifier` |When not null, categorizes the property under a category.|
|[Property_Type](#property_type)|`nvarchar(1)` Allowed: `T`, `N`, `P`, `D`|Type of property values. 'T' - text; 'P' - picture; 'N' - number; 'D' - date.|
|[Key_Order](#key_order)|`tinyint` |When not null, indicates, that the property is a key property and contains the property consequtive position withing the entity. Used for BI and other analysis|
|[Allowed_Values_Parent_Property_Id](#allowed_values_parent_property_id)|`uniqueidentifier` |Specifies the user defined property, which is used for filtering the allowed values by value of the parent property|
|[Row_Version](#row_version)|`timestamp` ||
|[Hint](#hint)|`nvarchar(2147483647)` `ML`|The hint, which is displayed alongside the property.|
|[Notes](#notes)|`nvarchar(2147483647)` ||

## Columns

### Property_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Property_Code

| Property | Value |
| - | - |
|Type|nvarchar(40)|

### Property_Name

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Entity_Name

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### Allowed_Values_Entity_Name

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### Allowed_Values_Filter_XML

| Property | Value |
| - | - |
|Type|nvarchar(1073741823)|

### Limit_To_Allowed_Values

| Property | Value |
| - | - |
|Type|bit|

### Mask_Length

| Property | Value |
| - | - |
|Type|smallint|

### Allowed_Values_Property_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Properties_Category_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Property_Type

| Property | Value |
| - | - |
|Type|nvarchar(1)|

### Key_Order

| Property | Value |
| - | - |
|Type|tinyint|

### Allowed_Values_Parent_Property_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|

### Hint

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|


