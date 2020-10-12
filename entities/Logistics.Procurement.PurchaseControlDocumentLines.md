---
uid: Logistics.Procurement.PurchaseControlDocumentLines
---
# Logistics.Procurement.PurchaseControlDocumentLines Entity

The detail line of purchase control data. The purchase control is used to tally all orders and execuctions in the purchasing module. Entity: Scm_Purchase_Control_Document_Lines (Introduced in version 18.2)

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [ConfirmedAmountBase](Logistics.Procurement.PurchaseControlDocumentLines.md#confirmedamountbase) | decimal (nullable) | The amount (in base currency) of the ordered items, confirmed by the supplier (usually with Purchase Confirmation). Null when the logged operation did not involve confirming ordered items. 
| [ConfirmedStandard<br />QuantityBase](Logistics.Procurement.PurchaseControlDocumentLines.md#confirmedstandardquantitybase) | decimal (nullable) | The standard quantity of the ordered items, confirmed by the supplier (usually with Purchase Confirmation) in base measurement unit. Null when the logged operation did not involve confirming ordered items. 
| [Id](Logistics.Procurement.PurchaseControlDocumentLines.md#id) | guid |  
| [InvoicedAmountBase](Logistics.Procurement.PurchaseControlDocumentLines.md#invoicedamountbase) | decimal (nullable) | The amount (in base currency) of the invoiced items (usually with Purchase Invoice). Null when the logged operation did not involve invoicing items. 
| [InvoicedStandard<br />QuantityBase](Logistics.Procurement.PurchaseControlDocumentLines.md#invoicedstandardquantitybase) | decimal (nullable) | The standard quantity of the invoiced items (usually with Purchase Invoice) in base measurement unit. Null when the logged operation did not involve invoicing items. 
| [LineNo](Logistics.Procurement.PurchaseControlDocumentLines.md#lineno) | int32 | The consecutive line number within the control document. [Required] 
| [Notes](Logistics.Procurement.PurchaseControlDocumentLines.md#notes) | string (nullable) | Notes for this PurchaseControl<br />DocumentLine. 
| [OrderedAmountBase](Logistics.Procurement.PurchaseControlDocumentLines.md#orderedamountbase) | decimal (nullable) | The amount (in base currency) of the ordered items (usually with Purchase Order). Null when the logged operation did not involve ordering items. 
| [OrderedStandard<br />QuantityBase](Logistics.Procurement.PurchaseControlDocumentLines.md#orderedstandardquantitybase) | decimal (nullable) | The standard quantity of the ordered items (usually with Purchase Order) in base measurement unit. Null when the logged operation did not involve ordering items. 
| [ReceivedAmountBase](Logistics.Procurement.PurchaseControlDocumentLines.md#receivedamountbase) | decimal (nullable) | The amount (in base currency) of the received items (usually with Receiving Order). Null when the logged operation did not involve receiving items. 
| [ReceivedStandard<br />QuantityBase](Logistics.Procurement.PurchaseControlDocumentLines.md#receivedstandardquantitybase) | decimal (nullable) | The standard quantity of the received items (usually with Receiving Order) in base measurement unit. Null when the logged operation did not involve receiving items. 
| [RequestedAmountBase](Logistics.Procurement.PurchaseControlDocumentLines.md#requestedamountbase) | decimal (nullable) | The amount (in base currency) of the requested items (usually with Purchase Requisition). Null when the logged operation did not involve requesting items. 
| [RequestedStandard<br />QuantityBase](Logistics.Procurement.PurchaseControlDocumentLines.md#requestedstandardquantitybase) | decimal (nullable) | The standard quantity of the requested items (usually with Purchase Requisition) in base measurement unit. Null when the logged operation did not involve requesting items. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [PurchaseControlDocument](Logistics.Procurement.PurchaseControlDocumentLines.md#purchasecontroldocument) | [PurchaseControlDocuments](Logistics.Procurement.PurchaseControlDocuments.md) | The [PurchaseControlDocument](Logistics.Procurement.PurchaseControl<br />DocumentLines.md#purchasecontroldocument) to which this PurchaseControl<br />DocumentLine belongs. [Required] [Filter(multi eq)]  |
| [PurchaseInvoice](Logistics.Procurement.PurchaseControlDocumentLines.md#purchaseinvoice) | [PurchaseInvoices](Logistics.Procurement.PurchaseInvoices.md) (nullable) | The purchase invoice which is to be or was executed. Null when the data is unknown. [Filter(multi eq)] |
| [PurchaseInvoiceLine](Logistics.Procurement.PurchaseControlDocumentLines.md#purchaseinvoiceline) | [PurchaseInvoiceLines](Logistics.Procurement.PurchaseInvoiceLines.md) (nullable) | The purchase invoice line which is to be or was executed. Null when the data is unknown. [Filter(multi eq)] |
| [PurchaseOperationType](Logistics.Procurement.PurchaseControlDocumentLines.md#purchaseoperationtype) | [PurchaseOperationTypes](Logistics.Procurement.PurchaseOperationTypes.md) (nullable) | The user-defined operation type, which is being recorded by the current line. Used for better grouping of the control entries. null when the operation type was not specified by the user. [Filter(multi eq)] |
| [PurchaseOrder](Logistics.Procurement.PurchaseControlDocumentLines.md#purchaseorder) | [PurchaseOrders](Logistics.Procurement.PurchaseOrders.md) (nullable) | The purchase order which is to be or was executed. Null when the data is unknown. [Filter(multi eq)] |
| [PurchaseOrderLine](Logistics.Procurement.PurchaseControlDocumentLines.md#purchaseorderline) | [PurchaseOrderLines](Logistics.Procurement.PurchaseOrderLines.md) (nullable) | The purchase order line which is to be or was executed. Null when the data is unknown. [Filter(multi eq)] |
| [PurchaseRequisition](Logistics.Procurement.PurchaseControlDocumentLines.md#purchaserequisition) | [Requisitions](Logistics.Procurement.Requisitions.md) (nullable) | The purchase requisition which is to be or was executed. Null when the data is unknown. [Filter(multi eq)] |
| [PurchaseRequisitionLine](Logistics.Procurement.PurchaseControlDocumentLines.md#purchaserequisitionline) | [RequisitionLines](Logistics.Procurement.RequisitionLines.md) (nullable) | The purchase requisition line which is to be or was executed. Null when the data is unknown. [Filter(multi eq)] |
| [ReceivingOrder](Logistics.Procurement.PurchaseControlDocumentLines.md#receivingorder) | [ReceivingOrders](Logistics.Procurement.ReceivingOrders.md) (nullable) | The receiving order which is to be or was executed. Null when the data is unknown. [Filter(multi eq)] |
| [ReceivingOrderLine](Logistics.Procurement.PurchaseControlDocumentLines.md#receivingorderline) | [ReceivingOrderLines](Logistics.Procurement.ReceivingOrderLines.md) (nullable) | The receiving order line which is to be or was executed. Null when the data is unknown. [Filter(multi eq)] |


## Attribute Details

### ConfirmedAmountBase

The amount (in base currency) of the ordered items, confirmed by the supplier (usually with Purchase Confirmation). Null when the logged operation did not involve confirming ordered items.

_Type_: **decimal (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ConfirmedStandardQuantityBase

The standard quantity of the ordered items, confirmed by the supplier (usually with Purchase Confirmation) in base measurement unit. Null when the logged operation did not involve confirming ordered items.

_Type_: **decimal (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### InvoicedAmountBase

The amount (in base currency) of the invoiced items (usually with Purchase Invoice). Null when the logged operation did not involve invoicing items.

_Type_: **decimal (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### InvoicedStandardQuantityBase

The standard quantity of the invoiced items (usually with Purchase Invoice) in base measurement unit. Null when the logged operation did not involve invoicing items.

_Type_: **decimal (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### LineNo

The consecutive line number within the control document. [Required]

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Notes

Notes for this PurchaseControlDocumentLine.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### OrderedAmountBase

The amount (in base currency) of the ordered items (usually with Purchase Order). Null when the logged operation did not involve ordering items.

_Type_: **decimal (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### OrderedStandardQuantityBase

The standard quantity of the ordered items (usually with Purchase Order) in base measurement unit. Null when the logged operation did not involve ordering items.

_Type_: **decimal (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ReceivedAmountBase

The amount (in base currency) of the received items (usually with Receiving Order). Null when the logged operation did not involve receiving items.

_Type_: **decimal (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ReceivedStandardQuantityBase

The standard quantity of the received items (usually with Receiving Order) in base measurement unit. Null when the logged operation did not involve receiving items.

_Type_: **decimal (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### RequestedAmountBase

The amount (in base currency) of the requested items (usually with Purchase Requisition). Null when the logged operation did not involve requesting items.

_Type_: **decimal (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### RequestedStandardQuantityBase

The standard quantity of the requested items (usually with Purchase Requisition) in base measurement unit. Null when the logged operation did not involve requesting items.

_Type_: **decimal (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### PurchaseControlDocument

The [PurchaseControlDocument](Logistics.Procurement.PurchaseControlDocumentLines.md#purchasecontroldocument) to which this PurchaseControlDocumentLine belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[PurchaseControlDocuments](Logistics.Procurement.PurchaseControlDocuments.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### PurchaseInvoice

The purchase invoice which is to be or was executed. Null when the data is unknown. [Filter(multi eq)]

_Type_: **[PurchaseInvoices](Logistics.Procurement.PurchaseInvoices.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### PurchaseInvoiceLine

The purchase invoice line which is to be or was executed. Null when the data is unknown. [Filter(multi eq)]

_Type_: **[PurchaseInvoiceLines](Logistics.Procurement.PurchaseInvoiceLines.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### PurchaseOperationType

The user-defined operation type, which is being recorded by the current line. Used for better grouping of the control entries. null when the operation type was not specified by the user. [Filter(multi eq)]

_Type_: **[PurchaseOperationTypes](Logistics.Procurement.PurchaseOperationTypes.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### PurchaseOrder

The purchase order which is to be or was executed. Null when the data is unknown. [Filter(multi eq)]

_Type_: **[PurchaseOrders](Logistics.Procurement.PurchaseOrders.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### PurchaseOrderLine

The purchase order line which is to be or was executed. Null when the data is unknown. [Filter(multi eq)]

_Type_: **[PurchaseOrderLines](Logistics.Procurement.PurchaseOrderLines.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### PurchaseRequisition

The purchase requisition which is to be or was executed. Null when the data is unknown. [Filter(multi eq)]

_Type_: **[Requisitions](Logistics.Procurement.Requisitions.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### PurchaseRequisitionLine

The purchase requisition line which is to be or was executed. Null when the data is unknown. [Filter(multi eq)]

_Type_: **[RequisitionLines](Logistics.Procurement.RequisitionLines.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### ReceivingOrder

The receiving order which is to be or was executed. Null when the data is unknown. [Filter(multi eq)]

_Type_: **[ReceivingOrders](Logistics.Procurement.ReceivingOrders.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### ReceivingOrderLine

The receiving order line which is to be or was executed. Null when the data is unknown. [Filter(multi eq)]

_Type_: **[ReceivingOrderLines](Logistics.Procurement.ReceivingOrderLines.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Logistics.Procurement.PurchaseControlDocumentLines erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Logistics.Procurement.PurchaseControlDocumentLines erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_Procurement_PurchaseControlDocumentLines?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_Procurement_PurchaseControlDocumentLines?$top=10>

