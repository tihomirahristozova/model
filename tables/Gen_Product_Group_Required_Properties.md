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


Property_No


The consecutive number (position) of the property within the product group and its subgroups. The parent groups of each leaf group should contain only unique property numbers.


The consecutive number (position) of the property within the product group and its subgroups. The parent groups of each leaf group should contain only unique property numbers.

| Property | Value |
| - | - |
|Type|int|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|0|
|Autoincrement|1|
|Derived From|[Gen_Product_Group_Required_Properties](Gen_Product_Group_Required_Properties.md).[Property_No](Gen_Product_Group_Required_Properties.md#property_no)|
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
|Order|0|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Property_Id


Property_Id


The property, that is required when creating new products in the group. The property is automatically added to new products, created in the group. The property should be with Entity Type = 'Product'.


The property, that is required when creating new products in the group. The property is automatically added to new products, created in the group. The property should be with Entity Type = 'Product'.

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
|Derived From|[Gen_Product_Group_Required_Properties](Gen_Product_Group_Required_Properties.md).[Property_Id](Gen_Product_Group_Required_Properties.md#property_id)|
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
|Order|1|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Long|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Default_Property_Value


Default_Property_Value


When not null, specifies the default value of the property, for new products in the group.


When not null, specifies the default value of the property, for new products in the group.

| Property | Value |
| - | - |
|Type|nvarchar(254)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Product_Group_Required_Properties](Gen_Product_Group_Required_Properties.md).[Default_Property_Value](Gen_Product_Group_Required_Properties.md#default_property_value)|
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
|Max Length|254|
|Order|2|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
|Supports EQUALS_IN|no|

### Default_Property_Value_Description


Default_Property_Value_Description


When not null, specifies the default description value of the property, for new products in the group.


When not null, specifies the default description value of the property, for new products in the group.

| Property | Value |
| - | - |
|Type|nvarchar(254)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Product_Group_Required_Properties](Gen_Product_Group_Required_Properties.md).[Default_Property_Value_Description](Gen_Product_Group_Required_Properties.md#default_property_value_description)|
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
|Max Length|254|
|Order|3|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
|Supports EQUALS_IN|no|

### Required_Property_Id


Required_Property_Id

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
|Derived From|[Gen_Product_Group_Required_Properties](Gen_Product_Group_Required_Properties.md).[Required_Property_Id](Gen_Product_Group_Required_Properties.md#required_property_id)|
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

### Product_Group_Id


Product_Group_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|yes|
|Referenced Table|[Gen_Product_Groups](Gen_Product_Groups.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Product_Group_Required_Properties](Gen_Product_Group_Required_Properties.md).[Product_Group_Id](Gen_Product_Group_Required_Properties.md#product_group_id)|
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
|UI Width|Long|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Default_Value_Id


Default_Value_Id


When not null, specifies the default internal Id value of the property, for new products in the group.


When not null, specifies the default internal Id value of the property, for new products in the group.

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
|Derived From|[Gen_Product_Group_Required_Properties](Gen_Product_Group_Required_Properties.md).[Default_Value_Id](Gen_Product_Group_Required_Properties.md#default_value_id)|
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

### Required


Required


Specifies whether the property is required (or only suggested) to be set for new products. Suggested properties are used by product configuration and other product creation services. 1=Required, 0=Suggested.


Specifies whether the property is required (or only suggested) to be set for new products. Suggested properties are used by product configuration and other product creation services. 1=Required, 0=Suggested.

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
|Derived From|[Gen_Product_Group_Required_Properties](Gen_Product_Group_Required_Properties.md).[Required](Gen_Product_Group_Required_Properties.md#required)|
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
|Derived From|[Gen_Product_Group_Required_Properties](Gen_Product_Group_Required_Properties.md).[Row_Version](Gen_Product_Group_Required_Properties.md#row_version)|
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


