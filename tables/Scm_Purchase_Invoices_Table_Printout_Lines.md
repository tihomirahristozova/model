# Procedure Scm_Purchase_Invoices_Table_Printout_Lines


## Summary

| Name | Type | Description |
| - | - | --- |
|[Purchase_Invoice_Line_Id](#purchase_invoice_line_id)|`uniqueidentifier` `PK`||
|[Purchase_Invoice_Id](#purchase_invoice_id)|`uniqueidentifier` ||
|[Line_No](#line_no)|`int` |Consecutive line number within the invoice.|
|[Product_Id](#product_id)|`uniqueidentifier` |The invoiced product.|
|[Product_Name](#product_name)|`nvarchar` `ML`|The name of the invoiced product, initially copied from the name in the product definition. The field can be edited by the user.|
|[Quantity](#quantity)|`decimal(12, 3)` |The invoiced quantity.|
|[Quantity_Base](#quantity_base)|`decimal(0, 0)` Readonly||
|[Quantity_Unit_Id](#quantity_unit_id)|`uniqueidentifier` |The measurement unit of Quantity.|
|[Quantity_Unit_Id_Text](#quantity_unit_id_text)|`nvarchar` ||
|[Unit_Price](#unit_price)|`decimal(14, 5)` |The unit price of the invoiced item in the document currency of the invoice.|
|[Line_Amount](#line_amount)|`decimal(14, 2)` |The total invoiced amount for this line in the document currency of the invoice.|
|[Line_Deal_Type_Id](#line_deal_type_id)|`uniqueidentifier` |Deal type for this line. If deal type in the line is different from deal type in the header another VAT entry is created.|
|[Line_Cost_Center_Id](#line_cost_center_id)|`uniqueidentifier` |Cost center for which the amount from this row will be accounted.|
|[Sale_Line_Deal_Type_Id](#sale_line_deal_type_id)|`uniqueidentifier` |Sale deal type for this line. If sale deal type in the line is different from sale deal type in the header another Sales VAT entry is created.|
|[Receiving_Order_Line_Id](#receiving_order_line_id)|`uniqueidentifier` |The receiving order line, which is invoiced by the current line. NULL means that this line is not directly related to receiving order line.|

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
|Type|nvarchar|

### Quantity

| Property | Value |
| - | - |
|Type|decimal(12, 3)|

### Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Quantity_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Quantity_Unit_Id_Text

| Property | Value |
| - | - |
|Type|nvarchar|

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


