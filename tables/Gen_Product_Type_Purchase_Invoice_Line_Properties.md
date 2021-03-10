# Table Gen_Product_Type_Purchase_Invoice_Line_Properties

When specified for a product type, contains the suggested user-defined properties, which can be specified when creating new purchase invoice lines with products of this type. Entity: Gen_Product_Type_Purchase_Invoice_Line_Properties

## Owner Tables Hierarchy

* [Gen_Product_Types](Gen_Product_Types.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Property_No](#property_no)|`int` |The consecutive number (position) of the property within the current product type.|
|[Property_Id](#property_id)|`uniqueidentifier` |The user-defined property. It should be with Entity Type = 'Purchase Invoice Line'.|
|[Required](#required)|`bit` |True when the property is required, when creating new purchase invoice lines. False when this only suggests the usage of the property.|
|[Product_Type_Purchase_Invoice_Line_Property_Id](#product_type_purchase_invoice_line_property_id)|`uniqueidentifier` `PK`||
|[Product_Type_Id](#product_type_id)|`uniqueidentifier` ||
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Property_No


Property_No


The consecutive number (position) of the property within the current product type.


The consecutive number (position) of the property within the current product type.

| Property | Value |
| - | - |
|Type|int|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Autoincrement|1|
|Derived From|[Gen_Product_Type_Purchase_Invoice_Line_Properties](Gen_Product_Type_Purchase_Invoice_Line_Properties.md).[Property_No](Gen_Product_Type_Purchase_Invoice_Line_Properties.md#property_no)|
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
|UI Width|Short|
|Supports EQUALS_IN|no|

### Property_Id


Property_Id


The user-defined property. It should be with Entity Type = 'Purchase Invoice Line'.


The user-defined property. It should be with Entity Type = 'Purchase Invoice Line'.

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
|Derived From|[Gen_Product_Type_Purchase_Invoice_Line_Properties](Gen_Product_Type_Purchase_Invoice_Line_Properties.md).[Property_Id](Gen_Product_Type_Purchase_Invoice_Line_Properties.md#property_id)|
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
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Required


Required


True when the property is required, when creating new purchase invoice lines. False when this only suggests the usage of the property.


True when the property is required, when creating new purchase invoice lines. False when this only suggests the usage of the property.

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
|Derived From|[Gen_Product_Type_Purchase_Invoice_Line_Properties](Gen_Product_Type_Purchase_Invoice_Line_Properties.md).[Required](Gen_Product_Type_Purchase_Invoice_Line_Properties.md#required)|
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
|Order|3|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Short|
|Supports EQUALS_IN|no|

### Product_Type_Purchase_Invoice_Line_Property_Id


Product_Type_Purchase_Invoice_Line_Property_Id

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
|Derived From|[Gen_Product_Type_Purchase_Invoice_Line_Properties](Gen_Product_Type_Purchase_Invoice_Line_Properties.md).[Product_Type_Purchase_Invoice_Line_Property_Id](Gen_Product_Type_Purchase_Invoice_Line_Properties.md#product_type_purchase_invoice_line_property_id)|
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

### Product_Type_Id


Product_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|yes|
|Referenced Table|[Gen_Product_Types](Gen_Product_Types.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Product_Type_Purchase_Invoice_Line_Properties](Gen_Product_Type_Purchase_Invoice_Line_Properties.md).[Product_Type_Id](Gen_Product_Type_Purchase_Invoice_Line_Properties.md#product_type_id)|
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
|Derived From|[Gen_Product_Type_Purchase_Invoice_Line_Properties](Gen_Product_Type_Purchase_Invoice_Line_Properties.md).[Row_Version](Gen_Product_Type_Purchase_Invoice_Line_Properties.md#row_version)|
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


