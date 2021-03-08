# Table Ast_Asset_Order_Lines

Asset purchase or sales order line for one asset. Entity: Ast_Asset_Order_Lines

# Aggregate Hierarchy

* [Ast_Asset_Orders](Ast_Asset_Orders.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Asset_Order_Line_Id|`Guid`|`PK`, Readonly||
|Parent_Line_No|`Int32?`||The number of the line within the parent document, which the current line executes. null when the current line does not execute line. `Introduced in version 18.2` |
|Quantity|`Int32`||Indicates the nature of the current operation: 1 - the operation is applied, 0 - no change, -1 - the operation is cancelled. `Required` `Default(0)` |
