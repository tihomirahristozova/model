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

| Property | Value |
| - | - |
|Type|int|

### Property_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Required

| Property | Value |
| - | - |
|Type|bit|

### Product_Type_Purchase_Invoice_Line_Property_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


