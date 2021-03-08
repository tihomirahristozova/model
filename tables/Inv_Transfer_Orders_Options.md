# Table Inv_Transfer_Orders_Options

Options per document type for the transfer orders. Entity: Inv_Transfer_Orders_Options

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Transfer_Order_Option_Id|`Guid`|`PK`, Readonly||
|Available_Quantity_Only|`Boolean`||Specifies, that transfer orders of this document type will be allowed to be released only when the requested quantity is less than the available (ATP) quantity. `Required` `Default(false)` `Filter(eq)` |
