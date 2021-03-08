# Table Gen_Product_Type_Purchase_Invoice_Line_Properties

When specified for a product type, contains the suggested user-defined properties, which can be specified when creating new purchase invoice lines with products of this type. Entity: Gen_Product_Type_Purchase_Invoice_Line_Properties

# Aggregate Hierarchy

* [Gen_Product_Types](Gen_Product_Types.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Product_Type_Purchase_Invoice_Line_Property_Id|`Guid`|`PK`, Readonly||
|Property_No|`Int32`||The consecutive number (position) of the property within the current product type. `Required` |
|Required|`Boolean`||True when the property is required, when creating new purchase invoice lines. False when this only suggests the usage of the property. `Required` `Default(false)` |
