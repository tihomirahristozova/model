# Table Wms_Warehouse_Order_Fulfillments

Fulfillment of a warehouse order line. Entity: Wms_Warehouse_Order_Fulfillments (Introduced in version 20.1)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Warehouse_Order_Fulfillment_Id|`Guid`|`PK`, Readonly||
|Creation_Time_Utc|`DateTime`||The exact time in UTC, when the fulfillment was created in the system. `Required` |
|Is_Final|`Boolean`||Specifies whether this fulfillment will finalize the fulfillment of the order line, regardless of any remaining quantities. `Required` |
|Quantity|`Decimal`||Fulfilled quantity in the measurement unit of the warehouse order line. `Required` |
