# Query Gen_Property_Allowed_Values_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Property_Allowed_Value_Id](#property_allowed_value_id)|`uniqueidentifier` `PK`||
|[Property_Id](#property_id)|`uniqueidentifier` ||
|[Property_Allowed_Value](#property_allowed_value)|`nvarchar` |The actual allowed value.|
|[Description](#description)|`nvarchar` `ML`|The description of the property allowed value. Used to fill the Description column of the Property_Value in Gen_Property_Values_Table.|
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` ||
|[Active](#active)|`bit` |Specifies whether the allowed value is active and can be used when selecting property values.|
|[Picture](#picture)|`varbinary` |When not null, specifies a picture representation of the allowed value.|
|[Long_Description](#long_description)|`nvarchar` |When not null, specifies a long description of the allowed value. This long description is only used as helper information when selecting values, it is not copied in the property value.|
|[Parent_Allowed_Value_Id](#parent_allowed_value_id)|`uniqueidentifier` |The value of the parent property, for which this allowed value is valid.|
|[Property_Code](#property_code)|`nvarchar` |Unique property code.|
|[Property_Name](#property_name)|`nvarchar` `ML`||
|[Entity_Name](#entity_name)|`nvarchar` Readonly|The entity for which the property is applicable.|
|[Allowed_Values_Entity_Name](#allowed_values_entity_name)|`nvarchar` Readonly|When not NULL, specifies that the allowed values are retrieved from the specified entity|
|[Allowed_Values_Filter_XML](#allowed_values_filter_xml)|`nvarchar` Readonly|When not NULL specifies the filter to apply when extracting allowed values from entity|
|[Limit_To_Allowed_Values](#limit_to_allowed_values)|`bit` Readonly|When true, allows the property to be set only to allowed value. When false, the property can have any value.|
|[Mask_Length](#mask_length)|`smallint` Readonly|Limits te length of the property value to the specified number of characters. Null means no limitation|
|[Allowed_Values_Property_Id](#allowed_values_property_id)|`uniqueidentifier` Readonly|When not null, specifies that the current property can have the same allowed values as the specified property. Also, this makes the current and the specified property copy-compatible.|
|[Properties_Category_Id](#properties_category_id)|`uniqueidentifier` Readonly|When not null, categorizes the property under a category.|
|[Property_Type](#property_type)|`nvarchar` Allowed: `T`, `N`, `P`, `D`, Readonly|Type of property values. 'T' - text; 'P' - picture; 'N' - number; 'D' - date.|
|[Key_Order](#key_order)|`tinyint` Readonly|When not null, indicates, that the property is a key property and contains the property consequtive position withing the entity. Used for BI and other analysis|
|[Allowed_Values_Parent_Property_Id](#allowed_values_parent_property_id)|`uniqueidentifier` Readonly|Specifies the user defined property, which is used for filtering the allowed values by value of the parent property|
|[Hint](#hint)|`nvarchar` `ML`|The hint, which is displayed alongside the property.|
|[Notes](#notes)|`nvarchar` ||

## Columns

### Property_Allowed_Value_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Property_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Property_Allowed_Value

| Property | Value |
| - | - |
|Type|nvarchar|

### Description

| Property | Value |
| - | - |
|Type|nvarchar|

### Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Active

| Property | Value |
| - | - |
|Type|bit|

### Picture

| Property | Value |
| - | - |
|Type|varbinary|

### Long_Description

| Property | Value |
| - | - |
|Type|nvarchar|

### Parent_Allowed_Value_Id

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

### Hint

| Property | Value |
| - | - |
|Type|nvarchar|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar|


