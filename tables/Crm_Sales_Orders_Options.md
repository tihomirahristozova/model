# Table Crm_Sales_Orders_Options

Options for sales orders of specific user defined document type. Entity: Crm_Sales_Orders_Options

## Owner Tables Hierarchy

* [Gen_Document_Types](Gen_Document_Types.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Sales_Order_Option_Id](#sales_order_option_id)|`uniqueidentifier` `PK`||
|[Document_Type_Id](#document_type_id)|`uniqueidentifier` |The document type for which the sales order option applies.|
|[Available_Quantity_Only](#available_quantity_only)|`bit` |When 1 indicates that the sales order can be released only if there is sufficient available quantity (by ATP)|
|[Allowed_Directions](#allowed_directions)|`nvarchar(1)` Allowed: `S`, `R`, `*`, `A`|Allowed directions (return or normal sale) for the sales orders of this document type. 'S' = Normal sale, 'R' = Sales return, '*' = No limit, 'A' = Allow any, but not both (default)|
|[Minimum_Amount](#minimum_amount)|`decimal(14, 2)` |When not NULL, specifies minimal total amount of the sales order, which is required for order releasing.|
|[Minimum_Amount_Currency_Id](#minimum_amount_currency_id)|`uniqueidentifier` |The currency of Minimal Amount|
|[VAT_Deviation_Document_Amount_Type_Id](#vat_deviation_document_amount_type_id)|`uniqueidentifier` |Document amount that contains the difference between the total amount of the sales order formed by unit prices with VAT and the amount formed by unit prices without VAT|
|[Deal_Document_Type_Id](#deal_document_type_id)|`uniqueidentifier` |If filled then new opportunities (deals) from the specified type are created automatically by the sales orders that aren't assigned to existing opportunities.|
|[Shipment_Allowance](#shipment_allowance)|`nvarchar(1)` Allowed: `A`, `P`, `W`|Terms on which the shipment of the products in the sales order is allowed.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Sales_Order_Option_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Available_Quantity_Only

| Property | Value |
| - | - |
|Type|bit|

### Allowed_Directions

| Property | Value |
| - | - |
|Type|nvarchar(1)|

### Minimum_Amount

| Property | Value |
| - | - |
|Type|decimal(14, 2)|

### Minimum_Amount_Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### VAT_Deviation_Document_Amount_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Deal_Document_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Shipment_Allowance

| Property | Value |
| - | - |
|Type|nvarchar(1)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


