# Query Gen_Properties_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Property_Id](#property_id)|`uniqueidentifier` `PK`||
|[Property_Code](#property_code)|`nvarchar` ||
|[Property_Name](#property_name)|`nvarchar` `ML`||
|[Entity_Name](#entity_name)|`nvarchar` ||
|[Allowed_Values_Entity_Name](#allowed_values_entity_name)|`nvarchar` ||
|[Allowed_Values_Filter_XML](#allowed_values_filter_xml)|`nvarchar` ||
|[Limit_To_Allowed_Values](#limit_to_allowed_values)|`bit` ||
|[Mask_Length](#mask_length)|`smallint` ||
|[Allowed_Values_Property_Id](#allowed_values_property_id)|`uniqueidentifier` ||
|[Properties_Category_Id](#properties_category_id)|`uniqueidentifier` ||
|[Property_Type](#property_type)|`nvarchar` Allowed: `T`, `N`, `P`, `D`||
|[Key_Order](#key_order)|`tinyint` |When not null, indicates, that the property is a key property and contains the property consequtive position withing the entity. Used for BI and other analysis|
|[Allowed_Values_Parent_Property_Id](#allowed_values_parent_property_id)|`uniqueidentifier` |Specifies the user defined property, which is used for filtering the allowed values by value of the parent property|
|[Row_Version](#row_version)|`timestamp` ||
|[Hint](#hint)|`nvarchar` `ML`|The hint, which is displayed alongside the property.|
|[Notes](#notes)|`nvarchar` ||

## Columns

### Property_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Property_Code

| Property | Value |
| - | - |
|Type|nvarchar|

### Property_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Entity_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Allowed_Values_Entity_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Allowed_Values_Filter_XML

| Property | Value |
| - | - |
|Type|nvarchar|

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
|Type|nvarchar|

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
|Type|nvarchar|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar|


