# Procedure Crm_Invoices_Table_Printout_Lines


## Summary

| Name | Type | Description |
| - | - | --- |
|[Line_No](#line_no)|`int` |Consecutive line number, unique within the invoice. Usually is increasing in steps of 10, like in 10, 20, 30, etc.|
|[Product_Id](#product_id)|`uniqueidentifier` |The invoiced product. When NULL, although rarely used, the invoice line is still valid and the Product Description contains the invoiced item.|
|[Product_Description](#product_description)|`nvarchar` `ML`|The description of the invoiced product. Initially copied from the name of the invoiced Product or from the generating document|
|[Unit_Price](#unit_price)|`decimal(14, 5)` |The unit selling price of Quantity|
|[Unit_Price_Base_Currency](#unit_price_base_currency)|`decimal(0, 0)` ||
|[Quantity](#quantity)|`decimal(12, 3)` |The quantity of the invoiced product|
|[Quantity_Unit_Id](#quantity_unit_id)|`uniqueidentifier` |The measurement unit of Quantity|
|[Line_Amount_Base_Currency](#line_amount_base_currency)|`decimal(0, 0)` ||
|[Line_Amount](#line_amount)|`decimal(14, 2)` |Amount for the line in the currency of the parent document. Usually equals Quantity * Unit_Price. When Quantity = 0, Unit Price is undefined and this contains the total line amount.|
|[Sales_Order_Id](#sales_order_id)|`uniqueidentifier` |When not NULL specifies the Sales Order that is invoiced by this line|
|[Business_Reason](#business_reason)|`nvarchar` Allowed: `P`, `S`|Business reason for invoicing of this product or service. S=Shipment, P=Payment|
|[Invoice_Order_Line_Id](#invoice_order_line_id)|`uniqueidentifier` |Invoice order line which is invoiced by this line|
|[Line_Deal_Type_Id](#line_deal_type_id)|`uniqueidentifier` |Deal type for this line. If deal type in the line is different from deal type in the header another VAT entry is created.|
|[Line_Standard_Discount_Percent](#line_standard_discount_percent)|`decimal(0, 0)` ||
|[Invoice_Line_Id](#invoice_line_id)|`uniqueidentifier` `PK`||
|[Line_Custom_Discount_Percent](#line_custom_discount_percent)|`decimal(0, 0)` ||
|[Quantity_Unit_Id_Text](#quantity_unit_id_text)|`nvarchar` ||
|[Quantity_Base](#quantity_base)|`decimal(0, 0)` Readonly||
|[Product_Name](#product_name)|`nvarchar` ||
|[Product_Id_Text](#product_id_text)|`nvarchar` ||
|[Invoice_Id](#invoice_id)|`uniqueidentifier` ||
|[Line_Discount_Id](#line_discount_id)|`uniqueidentifier` ||
|[Payment_Transaction_Id](#payment_transaction_id)|`uniqueidentifier` |The payment transaction, which is invoiced by this line, when Business Reason = P. Used to reconcile the invoice with the payments in the case of advance payment.|

## Columns

### Line_No

| Property | Value |
| - | - |
|Type|int|

### Product_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Description

| Property | Value |
| - | - |
|Type|nvarchar|

### Unit_Price

| Property | Value |
| - | - |
|Type|decimal(14, 5)|

### Unit_Price_Base_Currency

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Quantity

| Property | Value |
| - | - |
|Type|decimal(12, 3)|

### Quantity_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Line_Amount_Base_Currency

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Line_Amount

| Property | Value |
| - | - |
|Type|decimal(14, 2)|

### Sales_Order_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Business_Reason

| Property | Value |
| - | - |
|Type|nvarchar|

### Invoice_Order_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Line_Deal_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Line_Standard_Discount_Percent

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Invoice_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Line_Custom_Discount_Percent

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Quantity_Unit_Id_Text

| Property | Value |
| - | - |
|Type|nvarchar|

### Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Product_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Product_Id_Text

| Property | Value |
| - | - |
|Type|nvarchar|

### Invoice_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Line_Discount_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Payment_Transaction_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|


