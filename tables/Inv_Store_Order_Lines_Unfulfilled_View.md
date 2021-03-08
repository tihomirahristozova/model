# Table Inv_Store_Order_Lines_Unfulfilled_View

Returns the remaining (unfulfilled) quantity and cost for each Store Order Line in Store Orders, which are Planned, FirmPlanned or Released. Is_Fulfilled and Is_QuantityFulfilled can be used to filter out lines which appear fulfilled. For best performance, the store orders should be finished after fulfilling. Entity: Inv_Store_Order_Lines_Unfulfilled_View (Introduced in version 21.1.1.16)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Is_Fulfilled|`Int32`||Returns 1/true when both the Quantity and Cost are fulfilled or only negligible (less than 0.001 for qty and 0.01 for cost) sums remain. Please note, that filtering by this fields forces full scan and calculation of remaining amounts for all non-finished store orders. For best performance, the store orders should be finished after fulfilling. `Required` `Filter(multi eq)` |
|Is_QuantityFulfilled|`Int32`||Returns 1/true when the Quantity is fulfilled or only negligible (less than 0.001) sum remains. Please note, that filtering by this fields forces full scan and calculation of remaining amounts for all non-finished store orders. For best performance, the store orders should be finished after fulfilling. `Required` `Filter(multi eq)` |
|Order_Remaining_Line_Cost|`Decimal`||The remaining (unfulfilled) line cost of the order line. `Required` `Filter(multi eq;ge;le)` |
|Order_Remaining_Quantity_Base|`Decimal`||The remaining (unfulfilled) quantity of the order line in base measurement unit. `Required` `Filter(multi eq;ge;le)` |
