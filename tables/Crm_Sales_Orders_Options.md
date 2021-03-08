# Table Crm_Sales_Orders_Options

Options for sales orders of specific user defined document type. Entity: Crm_Sales_Orders_Options

# Aggregate Hierarchy

* [Gen_Document_Types](Gen_Document_Types.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Sales_Order_Option_Id|`Guid`|`PK`, Readonly||
|Allowed_Directions|`AllowedDirections`|Allowed: `S`, `R`, `*`, `A`|Allowed directions (return or normal sale) for the sales orders of this document type. 'S' = Normal sale, 'R' = Sales return, '*' = No limit, 'A' = Allow any, but not both (default). `Required` `Default("A")` `Filter(multi eq)` |
|Available_Quantity_Only|`Boolean`||When true indicates that the sales order can be released only if there is sufficient available quantity (by ATP). `Required` `Default(false)` `Filter(eq)` |
|Shipment_Allowance|`ShipmentAllowance`|Allowed: `A`, `P`, `W`|Terms on which the shipment of the products in the sales order is allowed. `Required` `Default("A")` |
