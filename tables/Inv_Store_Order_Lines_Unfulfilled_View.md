# View Inv_Store_Order_Lines_Unfulfilled_View

Returns the remaining (unfulfilled) quantity and cost for each Store Order Line in Store Orders, which are Planned, FirmPlanned or Released. Is_Fulfilled and Is_QuantityFulfilled can be used to filter out lines which appear fulfilled. For best performance, the store orders should be finished after fulfilling. Entity: Inv_Store_Order_Lines_Unfulfilled_View (Introduced in version 21.1.1.16)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Serial_Number_Id](#serial_number_id)|`uniqueidentifier` |Which serial number to receive/issue. NULL means that serial number is unknown or not applicable|
|[Lot_Id](#lot_id)|`uniqueidentifier` |If non-null, contains the specific lot to use for the movement|
|[Store_Order_Line_Id](#store_order_line_id)|`uniqueidentifier` ||
|[Document_Date](#document_date)|`datetime` ||
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` ||
|[Store_Id](#store_id)|`uniqueidentifier` ||
|[Product_Id](#product_id)|`uniqueidentifier` ||
|[Product_Variant_Id](#product_variant_id)|`uniqueidentifier` |If specified determines which product variant of the current product in this line is used.|
|[Order_Remaining_Quantity_Base](#order_remaining_quantity_base)|`decimal(38, 3)` |The remaining (unfulfilled) quantity of the order line in base measurement unit.|
|[Order_Remaining_Line_Cost](#order_remaining_line_cost)|`decimal(38, 2)` |The remaining (unfulfilled) line cost of the order line.|
|[Is_Fulfilled](#is_fulfilled)|`int` |Returns 1/true when both the Quantity and Cost are fulfilled or only negligible (less than 0.001 for qty and 0.01 for cost) sums remain. Please note, that filtering by this fields forces full scan and calculation of remaining amounts for all non-finished store orders. For best performance, the store orders should be finished after fulfilling.|
|[Is_QuantityFulfilled](#is_quantityfulfilled)|`int` |Returns 1/true when the Quantity is fulfilled or only negligible (less than 0.001) sum remains. Please note, that filtering by this fields forces full scan and calculation of remaining amounts for all non-finished store orders. For best performance, the store orders should be finished after fulfilling.|

## Columns

### Serial_Number_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Lot_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Store_Order_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Date

| Property | Value |
| - | - |
|Type|datetime|

### Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Store_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Variant_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Order_Remaining_Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(38, 3)|

### Order_Remaining_Line_Cost

| Property | Value |
| - | - |
|Type|decimal(38, 2)|

### Is_Fulfilled

| Property | Value |
| - | - |
|Type|int|

### Is_QuantityFulfilled

| Property | Value |
| - | - |
|Type|int|


