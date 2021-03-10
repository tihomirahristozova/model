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


Purchase_Control_Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|yes|
|Order in Primary Key|1|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|NewGuid|
|Derived From|[Scm_Purchase_Control_Documents](Scm_Purchase_Control_Documents.md).[Purchase_Control_Document_Id](Scm_Purchase_Control_Documents.md#purchase_control_document_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Document_Id


Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|yes|
|Referenced Table|[Gen_Documents](Gen_Documents.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Scm_Purchase_Control_Documents](Scm_Purchase_Control_Documents.md).[Document_Id](Scm_Purchase_Control_Documents.md#document_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Purchase_Requisition_Id


Purchase_Requisition_Id


The purchase requisition, when it is the same for all lines. NULL when it is null for the lines or the lines have different values.


The purchase requisition, when it is the same for all lines. NULL when it is null for the lines or the lines have different values.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Scm_Requisitions](Scm_Requisitions.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Scm_Purchase_Control_Documents](Scm_Purchase_Control_Documents.md).[Purchase_Requisition_Id](Scm_Purchase_Control_Documents.md#purchase_requisition_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Purchase_Order_Id


Purchase_Order_Id


The purchase order, when it is the same for all lines. NULL when it is null for the lines or the lines have different values.


The purchase order, when it is the same for all lines. NULL when it is null for the lines or the lines have different values.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Scm_Purchase_Orders](Scm_Purchase_Orders.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Scm_Purchase_Control_Documents](Scm_Purchase_Control_Documents.md).[Purchase_Order_Id](Scm_Purchase_Control_Documents.md#purchase_order_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Receiving_Order_Id


Receiving_Order_Id


The receiving order, when it is the same for all lines. NULL when it is null for the lines or the lines have different values.


The receiving order, when it is the same for all lines. NULL when it is null for the lines or the lines have different values.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Scm_Receiving_Orders](Scm_Receiving_Orders.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Scm_Purchase_Control_Documents](Scm_Purchase_Control_Documents.md).[Receiving_Order_Id](Scm_Purchase_Control_Documents.md#receiving_order_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Purchase_Invoice_Id


Purchase_Invoice_Id


The purchase invoice, when it is the same for all lines. NULL when it is null for the lines or the lines have different values.


The purchase invoice, when it is the same for all lines. NULL when it is null for the lines or the lines have different values.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Scm_Purchase_Invoices](Scm_Purchase_Invoices.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Scm_Purchase_Control_Documents](Scm_Purchase_Control_Documents.md).[Purchase_Invoice_Id](Scm_Purchase_Control_Documents.md#purchase_invoice_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|


