# Table Scm_Purchase_Control_Document_Lines

The detail line of purchase control data. The purchase control is used to tally all orders and execuctions in the purchasing module. Entity: Scm_Purchase_Control_Document_Lines (Introduced in version 18.2)

## Owner Tables Hierarchy

* [Scm_Purchase_Control_Documents](Scm_Purchase_Control_Documents.md)
* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Purchase_Control_Document_Line_Id](#purchase_control_document_line_id)|`uniqueidentifier` `PK`||
|[Purchase_Control_Document_Id](#purchase_control_document_id)|`uniqueidentifier` ||
|[Line_No](#line_no)|`int` |The consecutive line number within the control document.|
|[Purchase_Operation_Type_Id](#purchase_operation_type_id)|`uniqueidentifier` |The user-defined operation type, which is being recorded by the current line. Used for better grouping of the control entries. NULL when the operation type was not specified by the user.|
|[Requested_Standard_Quantity_Base](#requested_standard_quantity_base)|`decimal(12, 3)` |The standard quantity of the requested items (usually with Purchase Requisition) in base measurement unit. Null when the logged operation did not involve requesting items.|
|[Ordered_Standard_Quantity_Base](#ordered_standard_quantity_base)|`decimal(12, 3)` |The standard quantity of the ordered items (usually with Purchase Order) in base measurement unit. Null when the logged operation did not involve ordering items.|
|[Confirmed_Standard_Quantity_Base](#confirmed_standard_quantity_base)|`decimal(12, 3)` |The standard quantity of the ordered items, confirmed by the supplier (usually with Purchase Confirmation) in base measurement unit. Null when the logged operation did not involve confirming ordered items.|
|[Received_Standard_Quantity_Base](#received_standard_quantity_base)|`decimal(12, 3)` |The standard quantity of the received items (usually with Receiving Order) in base measurement unit. Null when the logged operation did not involve receiving items.|
|[Invoiced_Standard_Quantity_Base](#invoiced_standard_quantity_base)|`decimal(12, 3)` |The standard quantity of the invoiced items (usually with Purchase Invoice) in base measurement unit. Null when the logged operation did not involve invoicing items.|
|[Requested_Amount_Base](#requested_amount_base)|`decimal(14, 2)` |The amount (in base currency) of the requested items (usually with Purchase Requisition). Null when the logged operation did not involve requesting items.|
|[Ordered_Amount_Base](#ordered_amount_base)|`decimal(14, 2)` |The amount (in base currency) of the ordered items (usually with Purchase Order). Null when the logged operation did not involve ordering items.|
|[Confirmed_Amount_Base](#confirmed_amount_base)|`decimal(14, 2)` |The amount (in base currency) of the ordered items, confirmed by the supplier (usually with Purchase Confirmation). Null when the logged operation did not involve confirming ordered items.|
|[Received_Amount_Base](#received_amount_base)|`decimal(14, 2)` |The amount (in base currency) of the received items (usually with Receiving Order). Null when the logged operation did not involve receiving items.|
|[Invoiced_Amount_Base](#invoiced_amount_base)|`decimal(14, 2)` |The amount (in base currency) of the invoiced items (usually with Purchase Invoice). Null when the logged operation did not involve invoicing items.|
|[Purchase_Requisition_Id](#purchase_requisition_id)|`uniqueidentifier` |The purchase requisition which is to be or was executed. Null when the data is unknown.|
|[Purchase_Requisition_Line_Id](#purchase_requisition_line_id)|`uniqueidentifier` |The purchase requisition line which is to be or was executed. Null when the data is unknown.|
|[Purchase_Order_Id](#purchase_order_id)|`uniqueidentifier` |The purchase order which is to be or was executed. Null when the data is unknown.|
|[Purchase_Order_Line_Id](#purchase_order_line_id)|`uniqueidentifier` |The purchase order line which is to be or was executed. Null when the data is unknown.|
|[Receiving_Order_Id](#receiving_order_id)|`uniqueidentifier` |The receiving order which is to be or was executed. Null when the data is unknown.|
|[Receiving_Order_Line_Id](#receiving_order_line_id)|`uniqueidentifier` |The receiving order line which is to be or was executed. Null when the data is unknown.|
|[Purchase_Invoice_Id](#purchase_invoice_id)|`uniqueidentifier` |The purchase invoice which is to be or was executed. Null when the data is unknown.|
|[Purchase_Invoice_Line_Id](#purchase_invoice_line_id)|`uniqueidentifier` |The purchase invoice line which is to be or was executed. Null when the data is unknown.|
|[Notes](#notes)|`nvarchar(2147483647)` ||

## Columns

### Purchase_Control_Document_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Purchase_Control_Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Line_No

| Property | Value |
| - | - |
|Type|int|

### Purchase_Operation_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Requested_Standard_Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(12, 3)|

### Ordered_Standard_Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(12, 3)|

### Confirmed_Standard_Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(12, 3)|

### Received_Standard_Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(12, 3)|

### Invoiced_Standard_Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(12, 3)|

### Requested_Amount_Base

| Property | Value |
| - | - |
|Type|decimal(14, 2)|

### Ordered_Amount_Base

| Property | Value |
| - | - |
|Type|decimal(14, 2)|

### Confirmed_Amount_Base

| Property | Value |
| - | - |
|Type|decimal(14, 2)|

### Received_Amount_Base

| Property | Value |
| - | - |
|Type|decimal(14, 2)|

### Invoiced_Amount_Base

| Property | Value |
| - | - |
|Type|decimal(14, 2)|

### Purchase_Requisition_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Purchase_Requisition_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Purchase_Order_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Purchase_Order_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Receiving_Order_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Receiving_Order_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Purchase_Invoice_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Purchase_Invoice_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|


