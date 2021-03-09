# Table Scm_Purchase_Control_Documents

The main document for purchase control data. The purchase control is used to tally all orders and execuctions in the purchasing module. Entity: Scm_Purchase_Control_Documents (Introduced in version 18.2)

## Owner Tables Hierarchy

* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Purchase_Control_Document_Id](#purchase_control_document_id)|`uniqueidentifier` `PK`||
|[Document_Id](#document_id)|`uniqueidentifier` ||
|[Purchase_Requisition_Id](#purchase_requisition_id)|`uniqueidentifier` |The purchase requisition, when it is the same for all lines. NULL when it is null for the lines or the lines have different values.|
|[Purchase_Order_Id](#purchase_order_id)|`uniqueidentifier` |The purchase order, when it is the same for all lines. NULL when it is null for the lines or the lines have different values.|
|[Receiving_Order_Id](#receiving_order_id)|`uniqueidentifier` |The receiving order, when it is the same for all lines. NULL when it is null for the lines or the lines have different values.|
|[Purchase_Invoice_Id](#purchase_invoice_id)|`uniqueidentifier` |The purchase invoice, when it is the same for all lines. NULL when it is null for the lines or the lines have different values.|

## Columns

### Purchase_Control_Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Purchase_Requisition_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Purchase_Order_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Receiving_Order_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Purchase_Invoice_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|


