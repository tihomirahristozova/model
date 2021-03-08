# Table Crm_Sales_Order_Promotional_Packages

The promotional packages, included in a sales order. Entity: Crm_Sales_Order_Promotional_Packages

# Aggregate Hierarchy

* [Crm_Sales_Orders](Crm_Sales_Orders.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Sales_Order_Promotional_Package_Id|`Guid`|`PK`, Readonly||
|Line_Number|`Int32`||Consecutive line number of the package, unique within the document. `Required` `Filter(eq)` |
|Number_Of_Packages|`Int32`||Number of packages sold. `Required` `Default(0)` |
