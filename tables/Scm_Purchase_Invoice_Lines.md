# Table Scm_Purchase_Invoice_Lines

Contains detail lines for purchase invoice documents. Entity: Scm_Purchase_Invoice_Lines

## Owner Tables Hierarchy

* [Scm_Purchase_Invoices](Scm_Purchase_Invoices.md)
* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Purchase_Invoice_Line_Id](#purchase_invoice_line_id)|`uniqueidentifier` `PK`||
|[Purchase_Invoice_Id](#purchase_invoice_id)|`uniqueidentifier` ||
|[Line_No](#line_no)|`int` |Consecutive line number within the invoice.|
|[Product_Id](#product_id)|`uniqueidentifier` |The invoiced product.|
|[Product_Name](#product_name)|`nvarchar(254)` `ML`|The name of the invoiced product, initially copied from the name in the product definition. The field can be edited by the user.|
|[Quantity](#quantity)|`decimal(12, 3)` |The invoiced quantity.|
|[Quantity_Unit_Id](#quantity_unit_id)|`uniqueidentifier` |The measurement unit of Quantity.|
|[Unit_Price](#unit_price)|`decimal(14, 5)` |The unit price of the invoiced item in the document currency of the invoice.|
|[Line_Amount](#line_amount)|`decimal(14, 2)` |The total invoiced amount for this line in the document currency of the invoice.|
|[Line_Deal_Type_Id](#line_deal_type_id)|`uniqueidentifier` |Deal type for this line. If deal type in the line is different from deal type in the header another VAT entry is created.|
|[Line_Cost_Center_Id](#line_cost_center_id)|`uniqueidentifier` |Cost center for which the amount from this row will be accounted.|
|[Sale_Line_Deal_Type_Id](#sale_line_deal_type_id)|`uniqueidentifier` |Sale deal type for this line. If sale deal type in the line is different from sale deal type in the header another Sales VAT entry is created.|
|[Receiving_Order_Line_Id](#receiving_order_line_id)|`uniqueidentifier` |The receiving order line, which is invoiced by the current line. NULL means that this line is not directly related to receiving order line.|
|[Notes](#notes)|`nvarchar(254)` ||
|[Quantity_Base](#quantity_base)|`decimal(12, 3)` |The equivalence of Quantity in the base measurement category of the product.|
|[Delivery_Terms_Code](#delivery_terms_code)|`nvarchar(3)` Allowed: `EXW`, `FCA`, `FAS`, `FOB`, `CFR`, `CIF`, `CPT`, `CIP`, `DAP`, `DAT`, `DDP`, `DPU`|Mode of delivery, like CIF, FOB, etc. Used also in Intrastat reporting|
|[Intrastat_Transaction_Nature_Code](#intrastat_transaction_nature_code)|`nvarchar(2)` Allowed: `11`, `12`, `13`, `14`, `19`, `21`, `22`, `23`, `29`, `60`, `70`, `80`, `91`, `99`, `30`, `41`, `42`, `51`, `52`|Transaction nature; used for Intrastat reporting|
|[Intrastat_Transport_Mode_Code](#intrastat_transport_mode_code)|`nvarchar(1)` Allowed: `1`, `2`, `3`, `4`, `5`, `6`, `7`, `8`|Transport mode; used for Intrastat reporting|
|[Intrastat_Transport_Country_Id](#intrastat_transport_country_id)|`uniqueidentifier` |Country of origin of the transport company; used for Intrastat reporting|
|[Intrastat_Destination_Region_Id](#intrastat_destination_region_id)|`uniqueidentifier` |Region, which is the final destination of the goods. Used for Intrastat reporting.|
|[Origin_Country_Id](#origin_country_id)|`uniqueidentifier` |The country of origin of the invoiced product. Should be non-NULL only when this is different from the country of origin from the product definition.|
|[Intrastat_Apply_Date](#intrastat_apply_date)|`datetime` |Specifies in which period for Intrastat declaration must be included the current operation. Used only when the invoice is issued in different period than the one, that the operation must be included. If not set the document date is used.|
|[Row_Version](#row_version)|`timestamp` ||
|[Standard_Quantity_Base](#standard_quantity_base)|`decimal(12, 3)` Readonly|The theoretical quantity in base measurement unit according to the current measurement dimensions for the product. Used to measure the execution.|

## Columns

### Purchase_Invoice_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Purchase_Invoice_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Line_No

| Property | Value |
| - | - |
|Type|int|

### Product_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Name

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Quantity

| Property | Value |
| - | - |
|Type|decimal(12, 3)|

### Quantity_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Unit_Price

| Property | Value |
| - | - |
|Type|decimal(14, 5)|

### Line_Amount

| Property | Value |
| - | - |
|Type|decimal(14, 2)|

### Line_Deal_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Line_Cost_Center_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Sale_Line_Deal_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Receiving_Order_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(12, 3)|

### Delivery_Terms_Code

| Property | Value |
| - | - |
|Type|nvarchar(3)|

### Intrastat_Transaction_Nature_Code

| Property | Value |
| - | - |
|Type|nvarchar(2)|

### Intrastat_Transport_Mode_Code

| Property | Value |
| - | - |
|Type|nvarchar(1)|

### Intrastat_Transport_Country_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Intrastat_Destination_Region_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Origin_Country_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Intrastat_Apply_Date

| Property | Value |
| - | - |
|Type|datetime|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|

### Standard_Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(12, 3)|


