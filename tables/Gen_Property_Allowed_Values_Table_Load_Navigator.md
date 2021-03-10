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


Property_Allowed_Value_Id

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
|Derived From|[Gen_Property_Allowed_Values](Gen_Property_Allowed_Values.md).[Property_Allowed_Value_Id](Gen_Property_Allowed_Values.md#property_allowed_value_id)|
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
|Order|0|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Property_Id


Property_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Properties](Gen_Properties.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Property_Allowed_Values](Gen_Property_Allowed_Values.md).[Property_Id](Gen_Property_Allowed_Values.md#property_id)|
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
|Order|1|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Long|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Property_Allowed_Value


Property_Allowed_Value


The actual allowed value.


The actual allowed value.

| Property | Value |
| - | - |
|Type|nvarchar|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Property_Allowed_Values](Gen_Property_Allowed_Values.md).[Property_Allowed_Value](Gen_Property_Allowed_Values.md#property_allowed_value)|
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
|Order|2|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Long|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|
|Like|None|no|no|

### Description


Description


The description of the property allowed value. Used to fill the Description column of the Property_Value in Gen_Property_Values_Table.


The description of the property allowed value. Used to fill the Description column of the Property_Value in Gen_Property_Values_Table.

| Property | Value |
| - | - |
|Type|nvarchar|
|Is Mulitlanguage|yes|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Property_Allowed_Values](Gen_Property_Allowed_Values.md).[Description](Gen_Property_Allowed_Values.md#description)|
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
|Order|3|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|
|Like|None|no|no|

### Enterprise_Company_Id


Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Enterprise_Companies](Gen_Enterprise_Companies.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Property_Allowed_Values](Gen_Property_Allowed_Values.md).[Enterprise_Company_Id](Gen_Property_Allowed_Values.md#enterprise_company_id)|
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
|Order|4|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Active


Active


Specifies whether the allowed value is active and can be used when selecting property values.


Specifies whether the allowed value is active and can be used when selecting property values.

| Property | Value |
| - | - |
|Type|bit|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|True|
|Derived From|[Gen_Property_Allowed_Values](Gen_Property_Allowed_Values.md).[Active](Gen_Property_Allowed_Values.md#active)|
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
|Order|5|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|True|no|no|

### Picture


Picture


When not null, specifies a picture representation of the allowed value.


When not null, specifies a picture representation of the allowed value.

| Property | Value |
| - | - |
|Type|varbinary|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Property_Allowed_Values](Gen_Property_Allowed_Values.md).[Picture](Gen_Property_Allowed_Values.md#picture)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|yes|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|6|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
|Supports EQUALS_IN|no|

### Long_Description


Long_Description


When not null, specifies a long description of the allowed value. This long description is only used as helper information when selecting values, it is not copied in the property value.


When not null, specifies a long description of the allowed value. This long description is only used as helper information when selecting values, it is not copied in the property value.

| Property | Value |
| - | - |
|Type|nvarchar|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None, IsLongString|
|Default Value|None|
|Derived From|[Gen_Property_Allowed_Values](Gen_Property_Allowed_Values.md).[Long_Description](Gen_Property_Allowed_Values.md#long_description)|
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
|Order|7|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Long|
|Supports EQUALS_IN|no|

### Parent_Allowed_Value_Id


Parent_Allowed_Value_Id


The value of the parent property, for which this allowed value is valid.


The value of the parent property, for which this allowed value is valid.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Property_Allowed_Values](Gen_Property_Allowed_Values.md).[Parent_Allowed_Value_Id](Gen_Property_Allowed_Values.md#parent_allowed_value_id)|
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
|Order|8|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Property_Code


Property_Code


Unique property code.


Unique property code.

| Property | Value |
| - | - |
|Type|nvarchar|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
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
|Max Length|-1|
|Order|9|
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
|Type|nvarchar|
|Is Mulitlanguage|yes|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
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
|Max Length|-1|
|Order|10|
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
|Type|nvarchar|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|yes|
|Sortable|no|
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
|Max Length|-1|
|Order|11|
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
|Type|nvarchar|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|yes|
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
|Max Length|-1|
|Order|12|
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
|Type|nvarchar|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|yes|
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
|Max Length|-1|
|Order|13|
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
|Readonly|yes|
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
|Order|14|
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
|Readonly|yes|
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
|Order|15|
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
|Readonly|yes|
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
|Order|16|
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
|Readonly|yes|
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
|Order|17|
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
|Type|nvarchar|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|yes|
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
|Max Length|-1|
|Order|18|
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
|Readonly|yes|
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
|Order|19|
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
|Readonly|yes|
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
|Order|20|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Hint


Hint


The hint, which is displayed alongside the property.


The hint, which is displayed alongside the property.

| Property | Value |
| - | - |
|Type|nvarchar|
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
|Max Length|-1|
|Order|21|
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
|Type|nvarchar|
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
|Max Length|-1|
|Order|22|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Long|
|Supports EQUALS_IN|no|


