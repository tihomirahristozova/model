---
uid: Logistics.Procurement.PurchaseControlDocumentLines
---
# Logistics.Procurement.PurchaseControlDocumentLines

The detail line of purchase control data. The purchase control is used to tally all orders and execuctions in the purchasing module. Entity: Scm_Purchase_Control_Document_Lines (Introduced in version 18.2.100.0)

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Logistics.Procurement.PurchaseControlDocumentLines.md#Id) | guid |  
| [ConfirmedAmountBase](Logistics.Procurement.PurchaseControlDocumentLines.md#ConfirmedAmountBase) | decimal (nullable) | The amount (in base currency) of the ordered items, confirmed by the supplier (usually with Purchase Confirmation). Null when the logged operation did not involve confirming ordered items. 
| [ConfirmedStandardQuantityBase](Logistics.Procurement.PurchaseControlDocumentLines.md#ConfirmedStandardQuantityBase) | decimal (nullable) | The standard quantity of the ordered items, confirmed by the supplier (usually with Purchase Confirmation) in base measurement unit. Null when the logged operation did not involve confirming ordered items. 
| [InvoicedAmountBase](Logistics.Procurement.PurchaseControlDocumentLines.md#InvoicedAmountBase) | decimal (nullable) | The amount (in base currency) of the invoiced items (usually with Purchase Invoice). Null when the logged operation did not involve invoicing items. 
| [InvoicedStandardQuantityBase](Logistics.Procurement.PurchaseControlDocumentLines.md#InvoicedStandardQuantityBase) | decimal (nullable) | The standard quantity of the invoiced items (usually with Purchase Invoice) in base measurement unit. Null when the logged operation did not involve invoicing items. 
| [LineNo](Logistics.Procurement.PurchaseControlDocumentLines.md#LineNo) | int32 | The consecutive line number within the control document. [Required] 
| [Notes](Logistics.Procurement.PurchaseControlDocumentLines.md#Notes) | string (nullable) | Notes for this PurchaseControlDocumentLine. 
| [OrderedAmountBase](Logistics.Procurement.PurchaseControlDocumentLines.md#OrderedAmountBase) | decimal (nullable) | The amount (in base currency) of the ordered items (usually with Purchase Order). Null when the logged operation did not involve ordering items. 
| [OrderedStandardQuantityBase](Logistics.Procurement.PurchaseControlDocumentLines.md#OrderedStandardQuantityBase) | decimal (nullable) | The standard quantity of the ordered items (usually with Purchase Order) in base measurement unit. Null when the logged operation did not involve ordering items. 
| [ReceivedAmountBase](Logistics.Procurement.PurchaseControlDocumentLines.md#ReceivedAmountBase) | decimal (nullable) | The amount (in base currency) of the received items (usually with Receiving Order). Null when the logged operation did not involve receiving items. 
| [ReceivedStandardQuantityBase](Logistics.Procurement.PurchaseControlDocumentLines.md#ReceivedStandardQuantityBase) | decimal (nullable) | The standard quantity of the received items (usually with Receiving Order) in base measurement unit. Null when the logged operation did not involve receiving items. 
| [RequestedAmountBase](Logistics.Procurement.PurchaseControlDocumentLines.md#RequestedAmountBase) | decimal (nullable) | The amount (in base currency) of the requested items (usually with Purchase Requisition). Null when the logged operation did not involve requesting items. 
| [RequestedStandardQuantityBase](Logistics.Procurement.PurchaseControlDocumentLines.md#RequestedStandardQuantityBase) | decimal (nullable) | The standard quantity of the requested items (usually with Purchase Requisition) in base measurement unit. Null when the logged operation did not involve requesting items. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [PurchaseControlDocument](Logistics.Procurement.PurchaseControlDocumentLines.md#PurchaseControlDocument) | [Logistics.Procurement.PurchaseControlDocuments](Logistics.Procurement.PurchaseControlDocuments.md) | The [PurchaseControlDocument](Logistics.Procurement.PurchaseControlDocumentLines.md#PurchaseControlDocument) to which this PurchaseControlDocumentLine belongs. [Required] [Filter(multi eq)] [Owner] |
| [PurchaseInvoice](Logistics.Procurement.PurchaseControlDocumentLines.md#PurchaseInvoice) | [Logistics.Procurement.PurchaseInvoices](Logistics.Procurement.PurchaseInvoices.md) (nullable) | The purchase invoice which is to be or was executed. Null when the data is unknown. [Filter(multi eq)] |
| [PurchaseInvoiceLine](Logistics.Procurement.PurchaseControlDocumentLines.md#PurchaseInvoiceLine) | [Logistics.Procurement.PurchaseInvoiceLines](Logistics.Procurement.PurchaseInvoiceLines.md) (nullable) | The purchase invoice line which is to be or was executed. Null when the data is unknown. [Filter(multi eq)] |
| [PurchaseOperationType](Logistics.Procurement.PurchaseControlDocumentLines.md#PurchaseOperationType) | [Logistics.Procurement.PurchaseOperationTypes](Logistics.Procurement.PurchaseOperationTypes.md) (nullable) | The user-defined operation type, which is being recorded by the current line. Used for better grouping of the control entries. null when the operation type was not specified by the user. [Filter(multi eq)] |
| [PurchaseOrder](Logistics.Procurement.PurchaseControlDocumentLines.md#PurchaseOrder) | [Logistics.Procurement.PurchaseOrders](Logistics.Procurement.PurchaseOrders.md) (nullable) | The purchase order which is to be or was executed. Null when the data is unknown. [Filter(multi eq)] |
| [PurchaseOrderLine](Logistics.Procurement.PurchaseControlDocumentLines.md#PurchaseOrderLine) | [Logistics.Procurement.PurchaseOrderLines](Logistics.Procurement.PurchaseOrderLines.md) (nullable) | The purchase order line which is to be or was executed. Null when the data is unknown. [Filter(multi eq)] |
| [PurchaseRequisition](Logistics.Procurement.PurchaseControlDocumentLines.md#PurchaseRequisition) | [Logistics.Procurement.Requisitions](Logistics.Procurement.Requisitions.md) (nullable) | The purchase requisition which is to be or was executed. Null when the data is unknown. [Filter(multi eq)] |
| [PurchaseRequisitionLine](Logistics.Procurement.PurchaseControlDocumentLines.md#PurchaseRequisitionLine) | [Logistics.Procurement.RequisitionLines](Logistics.Procurement.RequisitionLines.md) (nullable) | The purchase requisition line which is to be or was executed. Null when the data is unknown. [Filter(multi eq)] |
| [ReceivingOrder](Logistics.Procurement.PurchaseControlDocumentLines.md#ReceivingOrder) | [Logistics.Procurement.ReceivingOrders](Logistics.Procurement.ReceivingOrders.md) (nullable) | The receiving order which is to be or was executed. Null when the data is unknown. [Filter(multi eq)] |
| [ReceivingOrderLine](Logistics.Procurement.PurchaseControlDocumentLines.md#ReceivingOrderLine) | [Logistics.Procurement.ReceivingOrderLines](Logistics.Procurement.ReceivingOrderLines.md) (nullable) | The receiving order line which is to be or was executed. Null when the data is unknown. [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### ConfirmedAmountBase

> The amount (in base currency) of the ordered items, confirmed by the supplier (usually with Purchase Confirmation). Null when the logged operation did not involve confirming ordered items.

_Type_: **decimal (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ConfirmedStandardQuantityBase

> The standard quantity of the ordered items, confirmed by the supplier (usually with Purchase Confirmation) in base measurement unit. Null when the logged operation did not involve confirming ordered items.

_Type_: **decimal (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### InvoicedAmountBase

> The amount (in base currency) of the invoiced items (usually with Purchase Invoice). Null when the logged operation did not involve invoicing items.

_Type_: **decimal (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### InvoicedStandardQuantityBase

> The standard quantity of the invoiced items (usually with Purchase Invoice) in base measurement unit. Null when the logged operation did not involve invoicing items.

_Type_: **decimal (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### LineNo

> The consecutive line number within the control document. [Required]

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Notes

> Notes for this PurchaseControlDocumentLine.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### OrderedAmountBase

> The amount (in base currency) of the ordered items (usually with Purchase Order). Null when the logged operation did not involve ordering items.

_Type_: **decimal (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### OrderedStandardQuantityBase

> The standard quantity of the ordered items (usually with Purchase Order) in base measurement unit. Null when the logged operation did not involve ordering items.

_Type_: **decimal (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ReceivedAmountBase

> The amount (in base currency) of the received items (usually with Receiving Order). Null when the logged operation did not involve receiving items.

_Type_: **decimal (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ReceivedStandardQuantityBase

> The standard quantity of the received items (usually with Receiving Order) in base measurement unit. Null when the logged operation did not involve receiving items.

_Type_: **decimal (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### RequestedAmountBase

> The amount (in base currency) of the requested items (usually with Purchase Requisition). Null when the logged operation did not involve requesting items.

_Type_: **decimal (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### RequestedStandardQuantityBase

> The standard quantity of the requested items (usually with Purchase Requisition) in base measurement unit. Null when the logged operation did not involve requesting items.

_Type_: **decimal (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### PurchaseControlDocument

> The [PurchaseControlDocument](Logistics.Procurement.PurchaseControlDocumentLines.md#PurchaseControlDocument) to which this PurchaseControlDocumentLine belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Logistics.Procurement.PurchaseControlDocuments](Logistics.Procurement.PurchaseControlDocuments.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### PurchaseInvoice

> The purchase invoice which is to be or was executed. Null when the data is unknown. [Filter(multi eq)]

_Type_: **[Logistics.Procurement.PurchaseInvoices](Logistics.Procurement.PurchaseInvoices.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### PurchaseInvoiceLine

> The purchase invoice line which is to be or was executed. Null when the data is unknown. [Filter(multi eq)]

_Type_: **[Logistics.Procurement.PurchaseInvoiceLines](Logistics.Procurement.PurchaseInvoiceLines.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### PurchaseOperationType

> The user-defined operation type, which is being recorded by the current line. Used for better grouping of the control entries. null when the operation type was not specified by the user. [Filter(multi eq)]

_Type_: **[Logistics.Procurement.PurchaseOperationTypes](Logistics.Procurement.PurchaseOperationTypes.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### PurchaseOrder

> The purchase order which is to be or was executed. Null when the data is unknown. [Filter(multi eq)]

_Type_: **[Logistics.Procurement.PurchaseOrders](Logistics.Procurement.PurchaseOrders.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### PurchaseOrderLine

> The purchase order line which is to be or was executed. Null when the data is unknown. [Filter(multi eq)]

_Type_: **[Logistics.Procurement.PurchaseOrderLines](Logistics.Procurement.PurchaseOrderLines.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### PurchaseRequisition

> The purchase requisition which is to be or was executed. Null when the data is unknown. [Filter(multi eq)]

_Type_: **[Logistics.Procurement.Requisitions](Logistics.Procurement.Requisitions.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### PurchaseRequisitionLine

> The purchase requisition line which is to be or was executed. Null when the data is unknown. [Filter(multi eq)]

_Type_: **[Logistics.Procurement.RequisitionLines](Logistics.Procurement.RequisitionLines.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### ReceivingOrder

> The receiving order which is to be or was executed. Null when the data is unknown. [Filter(multi eq)]

_Type_: **[Logistics.Procurement.ReceivingOrders](Logistics.Procurement.ReceivingOrders.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### ReceivingOrderLine

> The receiving order line which is to be or was executed. Null when the data is unknown. [Filter(multi eq)]

_Type_: **[Logistics.Procurement.ReceivingOrderLines](Logistics.Procurement.ReceivingOrderLines.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Logistics.Procurement.PurchaseControlDocumentLines erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Logistics.Procurement.PurchaseControlDocumentLines erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Logistics.Procurement.PurchaseControlDocumentLines erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_Procurement_PurchaseControlDocumentLines?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_Procurement_PurchaseControlDocumentLines?$top=10>

