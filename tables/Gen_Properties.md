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


Property_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|yes|
|Order in Primary Key|1|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|NewGuid|
|Derived From|[Gen_Properties](Gen_Properties.md).[Property_Id](Gen_Properties.md#property_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Property_Code


Property_Code


Unique property code.


Unique property code.

| Property | Value |
| - | - |
|Type|nvarchar(40)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|yes|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Properties](Gen_Properties.md).[Property_Code](Gen_Properties.md#property_code)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|40|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|
|Like|None|no|no|

### Property_Name


Property_Name

| Property | Value |
| - | - |
|Type|nvarchar(254)|
|Is Mulitlanguage|yes|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|yes|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Properties](Gen_Properties.md).[Property_Name](Gen_Properties.md#property_name)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|254|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Long|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Like|None|no|no|

### Entity_Name


Entity_Name


The entity for which the property is applicable.


The entity for which the property is applicable.

| Property | Value |
| - | - |
|Type|nvarchar(64)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|yes|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Properties](Gen_Properties.md).[Entity_Name](Gen_Properties.md#entity_name)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|64|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Allowed_Values_Entity_Name


Allowed_Values_Entity_Name


When not NULL, specifies that the allowed values are retrieved from the specified entity


When not NULL, specifies that the allowed values are retrieved from the specified entity

| Property | Value |
| - | - |
|Type|nvarchar(64)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Properties](Gen_Properties.md).[Allowed_Values_Entity_Name](Gen_Properties.md#allowed_values_entity_name)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|64|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Allowed_Values_Filter_XML


Allowed_Values_Filter_XML


When not NULL specifies the filter to apply when extracting allowed values from entity


When not NULL specifies the filter to apply when extracting allowed values from entity

| Property | Value |
| - | - |
|Type|nvarchar(1073741823)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Properties](Gen_Properties.md).[Allowed_Values_Filter_XML](Gen_Properties.md#allowed_values_filter_xml)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|1073741823|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
|Supports EQUALS_IN|no|

### Limit_To_Allowed_Values


Limit_To_Allowed_Values


When true, allows the property to be set only to allowed value. When false, the property can have any value.


When true, allows the property to be set only to allowed value. When false, the property can have any value.

| Property | Value |
| - | - |
|Type|bit|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|False|
|Derived From|[Gen_Properties](Gen_Properties.md).[Limit_To_Allowed_Values](Gen_Properties.md#limit_to_allowed_values)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Short|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Mask_Length


Mask_Length


Limits te length of the property value to the specified number of characters. Null means no limitation


Limits te length of the property value to the specified number of characters. Null means no limitation

| Property | Value |
| - | - |
|Type|smallint|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Properties](Gen_Properties.md).[Mask_Length](Gen_Properties.md#mask_length)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Short|
|Supports EQUALS_IN|no|

### Allowed_Values_Property_Id


Allowed_Values_Property_Id


When not null, specifies that the current property can have the same allowed values as the specified property. Also, this makes the current and the specified property copy-compatible.


When not null, specifies that the current property can have the same allowed values as the specified property. Also, this makes the current and the specified property copy-compatible.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Properties](Gen_Properties.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Properties](Gen_Properties.md).[Allowed_Values_Property_Id](Gen_Properties.md#allowed_values_property_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Properties_Category_Id


Properties_Category_Id


When not null, categorizes the property under a category.


When not null, categorizes the property under a category.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Properties_Categories](Gen_Properties_Categories.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Properties](Gen_Properties.md).[Properties_Category_Id](Gen_Properties.md#properties_category_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Property_Type


Property_Type


Type of property values. 'T' - text; 'P' - picture; 'N' - number; 'D' - date.


Type of property values. 'T' - text; 'P' - picture; 'N' - number; 'D' - date.

| Property | Value |
| - | - |
|Type|nvarchar(1)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Allowed Values|`T`, `N`, `P`, `D`|
|Default Value|T|
|Derived From|[Gen_Properties](Gen_Properties.md).[Property_Type](Gen_Properties.md#property_type)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Key_Order


Key_Order


When not null, indicates, that the property is a key property and contains the property consequtive position withing the entity. Used for BI and other analysis


When not null, indicates, that the property is a key property and contains the property consequtive position withing the entity. Used for BI and other analysis

| Property | Value |
| - | - |
|Type|tinyint|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Properties](Gen_Properties.md).[Key_Order](Gen_Properties.md#key_order)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Allowed_Values_Parent_Property_Id


Allowed_Values_Parent_Property_Id


Specifies the user defined property, which is used for filtering the allowed values by value of the parent property


Specifies the user defined property, which is used for filtering the allowed values by value of the parent property

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Properties](Gen_Properties.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Properties](Gen_Properties.md).[Allowed_Values_Parent_Property_Id](Gen_Properties.md#allowed_values_parent_property_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Row_Version


Row_Version

| Property | Value |
| - | - |
|Type|timestamp|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Properties](Gen_Properties.md).[Row_Version](Gen_Properties.md#row_version)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Hint


Hint


The hint, which is displayed alongside the property.


The hint, which is displayed alongside the property.

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|
|Is Mulitlanguage|yes|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Properties](Gen_Properties.md).[Hint](Gen_Properties.md#hint)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|2147483647|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|
|Like|None|no|no|

### Notes


Notes

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Properties](Gen_Properties.md).[Notes](Gen_Properties.md#notes)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|2147483647|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Long|
|Supports EQUALS_IN|no|


