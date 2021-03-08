# Table Wms_Warehouse_Transactions

Represents increase or decrease in the quantity available in a warehouse location. Entity: Wms_Warehouse_Transactions (Introduced in version 21.1.1.26)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Warehouse_Transaction_Id|`Guid`|`PK`, Readonly||
|Catch_Quantity|`Decimal?`||Catch (measured) quantity for the transaction. Positive values indicate transactions. Negative values are used for adjustments. null when catch measurement is not configured for the product. `Filter(eq;ge;le)` |
|Creation_Time_Utc|`DateTime`|||
|Direction|`Direction`|Allowed: `I`, `O`|Direction of the transaction - I=IN, O=OUT. `Required` `Default("I")` `Filter(eq)` |
|Quantity|`Decimal`||The transacted net change in quantity. Positive values indicate transactions. Negative values are used for adjustments. `Required` `Default(0)` `Filter(multi eq;ge;le)` |
