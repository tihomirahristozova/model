# Table Wms_Warehouse_Requisition_Fulfillments

Fulfillment ledger for warehouse requisitions. Entity: Wms_Warehouse_Requisition_Fulfillments (Introduced in version 20.1)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Warehouse_Requisition_Fulfillment_Id|`Guid`|`PK`, Readonly||
|Creation_Time_Utc|`DateTime`||The exact time in UTC, when the fulfillment was created in the system. `Required` |
|Fulfillment_Type|`String`||Type of fulfillment: P=Plan created; C=Requisition completed. `Required` |
|Is_Final|`Boolean`||Specifies whether this fulfillment finalizes the requisition line, regardless of any remaining quantities. `Required` |
|Quantity|`Decimal`||Quantity fulfilled (in the measurement unit of the requisition line). `Required` |
