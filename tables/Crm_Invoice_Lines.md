# Table Crm_Invoice_Lines

Detail records (lines) of the invoices. Entity: Crm_Invoice_Lines

## Owner Tables Hierarchy

* [Crm_Invoices](Crm_Invoices.md)
* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Line_No](#line_no)|`int` |Consecutive line number, unique within the invoice. Usually is increasing in steps of 10, like in 10, 20, 30, etc.|
|[Product_Id](#product_id)|`uniqueidentifier` |The invoiced product. When NULL, although rarely used, the invoice line is still valid and the Product Description contains the invoiced item.|
|[Product_Description](#product_description)|`nvarchar(254)` `ML`|The description of the invoiced product. Initially copied from the name of the invoiced Product or from the generating document|
|[Unit_Price](#unit_price)|`decimal(14, 5)` |The unit selling price of Quantity|
|[Quantity](#quantity)|`decimal(12, 3)` |The quantity of the invoiced product|
|[Quantity_Unit_Id](#quantity_unit_id)|`uniqueidentifier` |The measurement unit of Quantity|
|[Serial_Number_Id](#serial_number_id)|`uniqueidentifier` |Which serial number to receive/issue. NULL means that serial number is unknown or not applicable|
|[Line_Amount](#line_amount)|`decimal(14, 2)` |Amount for the line in the currency of the parent document. Usually equals Quantity * Unit_Price. When Quantity = 0, Unit Price is undefined and this contains the total line amount.|
|[Line_Custom_Discount_Percent](#line_custom_discount_percent)|`decimal(7, 6)` |User-defined discount for the line|
|[Line_Discount_Id](#line_discount_id)|`uniqueidentifier` |The line discount type used to form the Line_Standard_Discount_Percent|
|[Line_Standard_Discount_Percent](#line_standard_discount_percent)|`decimal(7, 6)` |Standard discount for the line. This is automatically computed according to discount conditions|
|[Quantity_Base](#quantity_base)|`decimal(12, 3)` |The equivalent of Quantity in the base measurement unit of the Product|
|[Transaction_Line_Id](#transaction_line_id)|`uniqueidentifier` |The store transaction line that is invoiced by this line, for Business Reason = S|
|[Notes](#notes)|`nvarchar(254)` ||
|[Delivery_Terms_Code](#delivery_terms_code)|`nvarchar(3)` Allowed: `EXW`, `FCA`, `FAS`, `FOB`, `CFR`, `CIF`, `CPT`, `CIP`, `DAP`, `DAT`, `DDP`, `DPU`|Mode of delivery, like CIF, FOB, etc. Used also in Intrastat reporting|
|[Intrastat_Transport_Mode_Code](#intrastat_transport_mode_code)|`nvarchar(1)` Allowed: `1`, `2`, `3`, `4`, `5`, `6`, `7`, `8`|Transport mode; used for Intrastat reporting|
|[Intrastat_Transport_Country_Id](#intrastat_transport_country_id)|`uniqueidentifier` |Country of origin of the transport company; used for Intrastat reporting|
|[Intrastat_Transaction_Nature_Code](#intrastat_transaction_nature_code)|`nvarchar(2)` Allowed: `11`, `12`, `13`, `14`, `19`, `21`, `22`, `23`, `29`, `60`, `70`, `80`, `91`, `99`, `30`, `41`, `42`, `51`, `52`|Transaction nature; used for Intrastat reporting|
|[Payment_Transaction_Id](#payment_transaction_id)|`uniqueidentifier` |The payment transaction, which is invoiced by this line, when Business Reason = P. Used to reconcile the invoice with the payments in the case of advance payment.|
|[Parent_Sales_Order_Line_Id](#parent_sales_order_line_id)|`uniqueidentifier` |When not NULL specifies the Sales Order line that is invoiced by this invoice line|
|[Invoice_Id](#invoice_id)|`uniqueidentifier` ||
|[Invoice_Line_Id](#invoice_line_id)|`uniqueidentifier` `PK`||
|[Line_Deal_Type_Id](#line_deal_type_id)|`uniqueidentifier` |Deal type for this line. If deal type in the line is different from deal type in the header another VAT entry is created.|
|[Sales_Order_Id](#sales_order_id)|`uniqueidentifier` |When not NULL specifies the Sales Order that is invoiced by this line|
|[Business_Reason](#business_reason)|`nvarchar(1)` Allowed: `P`, `S`|Business reason for invoicing of this product or service. S=Shipment, P=Payment|
|[Invoice_Order_Line_Id](#invoice_order_line_id)|`uniqueidentifier` |Invoice order line which is invoiced by this line|
|[Sales_Order_Amount](#sales_order_amount)|`decimal(14, 2)` |Specifies what portion of the amount of the sales order is invoiced with this line. The amount is calculated with respect to the trade conditions (prices, discounts, etc.) from the sales order. Can be different from the total amount of the line when the trade conditions from the sales order have changed before invoicing|
|[Row_Version](#row_version)|`timestamp` ||
|[Standard_Quantity_Base](#standard_quantity_base)|`decimal(12, 3)` Readonly|The theoretical quantity in base measurement unit according to the current measurement dimensions for the product. Used to measure the execution.|
|[Parent_Line_No](#parent_line_no)|`int` |The number of the line within the parent document, which the current line executes. NULL when the current line does not execute line.|
|[Parent_Document_Id](#parent_document_id)|`uniqueidentifier` |The document, which the current line executes. NULL when the current line does not execute another line.|

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
|Type|nvarchar(254)|

### Unit_Price

| Property | Value |
| - | - |
|Type|decimal(14, 5)|

### Quantity

| Property | Value |
| - | - |
|Type|decimal(12, 3)|

### Quantity_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Serial_Number_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Line_Amount

| Property | Value |
| - | - |
|Type|decimal(14, 2)|

### Line_Custom_Discount_Percent

| Property | Value |
| - | - |
|Type|decimal(7, 6)|

### Line_Discount_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Line_Standard_Discount_Percent

| Property | Value |
| - | - |
|Type|decimal(7, 6)|

### Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(12, 3)|

### Transaction_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Delivery_Terms_Code

| Property | Value |
| - | - |
|Type|nvarchar(3)|

### Intrastat_Transport_Mode_Code

| Property | Value |
| - | - |
|Type|nvarchar(1)|

### Intrastat_Transport_Country_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Intrastat_Transaction_Nature_Code

| Property | Value |
| - | - |
|Type|nvarchar(2)|

### Payment_Transaction_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Parent_Sales_Order_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Invoice_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Invoice_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Line_Deal_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Sales_Order_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Business_Reason

| Property | Value |
| - | - |
|Type|nvarchar(1)|

### Invoice_Order_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Sales_Order_Amount

| Property | Value |
| - | - |
|Type|decimal(14, 2)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|

### Standard_Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(12, 3)|

### Parent_Line_No

| Property | Value |
| - | - |
|Type|int|

### Parent_Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|


