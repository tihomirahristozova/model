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


Purchase_Control_Document_Line_Id

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
|Derived From|[Scm_Purchase_Control_Document_Lines](Scm_Purchase_Control_Document_Lines.md).[Purchase_Control_Document_Line_Id](Scm_Purchase_Control_Document_Lines.md#purchase_control_document_line_id)|
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

### Purchase_Control_Document_Id


Purchase_Control_Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|yes|
|Referenced Table|[Scm_Purchase_Control_Documents](Scm_Purchase_Control_Documents.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Scm_Purchase_Control_Document_Lines](Scm_Purchase_Control_Document_Lines.md).[Purchase_Control_Document_Id](Scm_Purchase_Control_Document_Lines.md#purchase_control_document_id)|
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

### Line_No


Line_No


The consecutive line number within the control document.


The consecutive line number within the control document.

| Property | Value |
| - | - |
|Type|int|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Scm_Purchase_Control_Document_Lines](Scm_Purchase_Control_Document_Lines.md).[Line_No](Scm_Purchase_Control_Document_Lines.md#line_no)|
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
|Supports EQUALS_IN|no|

### Purchase_Operation_Type_Id


Purchase_Operation_Type_Id


The user-defined operation type, which is being recorded by the current line. Used for better grouping of the control entries. NULL when the operation type was not specified by the user.


The user-defined operation type, which is being recorded by the current line. Used for better grouping of the control entries. NULL when the operation type was not specified by the user.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Scm_Purchase_Operation_Types](Scm_Purchase_Operation_Types.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Scm_Purchase_Control_Document_Lines](Scm_Purchase_Control_Document_Lines.md).[Purchase_Operation_Type_Id](Scm_Purchase_Control_Document_Lines.md#purchase_operation_type_id)|
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

### Requested_Standard_Quantity_Base


Requested_Standard_Quantity_Base


The standard quantity of the requested items (usually with Purchase Requisition) in base measurement unit. Null when the logged operation did not involve requesting items.


The standard quantity of the requested items (usually with Purchase Requisition) in base measurement unit. Null when the logged operation did not involve requesting items.

| Property | Value |
| - | - |
|Type|decimal(12, 3)|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Scm_Purchase_Control_Document_Lines](Scm_Purchase_Control_Document_Lines.md).[Requested_Standard_Quantity_Base](Scm_Purchase_Control_Document_Lines.md#requested_standard_quantity_base)|
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
|Supports EQUALS_IN|no|

### Ordered_Standard_Quantity_Base


Ordered_Standard_Quantity_Base


The standard quantity of the ordered items (usually with Purchase Order) in base measurement unit. Null when the logged operation did not involve ordering items.


The standard quantity of the ordered items (usually with Purchase Order) in base measurement unit. Null when the logged operation did not involve ordering items.

| Property | Value |
| - | - |
|Type|decimal(12, 3)|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Scm_Purchase_Control_Document_Lines](Scm_Purchase_Control_Document_Lines.md).[Ordered_Standard_Quantity_Base](Scm_Purchase_Control_Document_Lines.md#ordered_standard_quantity_base)|
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
|Supports EQUALS_IN|no|

### Confirmed_Standard_Quantity_Base


Confirmed_Standard_Quantity_Base


The standard quantity of the ordered items, confirmed by the supplier (usually with Purchase Confirmation) in base measurement unit. Null when the logged operation did not involve confirming ordered items.


The standard quantity of the ordered items, confirmed by the supplier (usually with Purchase Confirmation) in base measurement unit. Null when the logged operation did not involve confirming ordered items.

| Property | Value |
| - | - |
|Type|decimal(12, 3)|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Scm_Purchase_Control_Document_Lines](Scm_Purchase_Control_Document_Lines.md).[Confirmed_Standard_Quantity_Base](Scm_Purchase_Control_Document_Lines.md#confirmed_standard_quantity_base)|
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
|Supports EQUALS_IN|no|

### Received_Standard_Quantity_Base


Received_Standard_Quantity_Base


The standard quantity of the received items (usually with Receiving Order) in base measurement unit. Null when the logged operation did not involve receiving items.


The standard quantity of the received items (usually with Receiving Order) in base measurement unit. Null when the logged operation did not involve receiving items.

| Property | Value |
| - | - |
|Type|decimal(12, 3)|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Scm_Purchase_Control_Document_Lines](Scm_Purchase_Control_Document_Lines.md).[Received_Standard_Quantity_Base](Scm_Purchase_Control_Document_Lines.md#received_standard_quantity_base)|
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
|Supports EQUALS_IN|no|

### Invoiced_Standard_Quantity_Base


Invoiced_Standard_Quantity_Base


The standard quantity of the invoiced items (usually with Purchase Invoice) in base measurement unit. Null when the logged operation did not involve invoicing items.


The standard quantity of the invoiced items (usually with Purchase Invoice) in base measurement unit. Null when the logged operation did not involve invoicing items.

| Property | Value |
| - | - |
|Type|decimal(12, 3)|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Scm_Purchase_Control_Document_Lines](Scm_Purchase_Control_Document_Lines.md).[Invoiced_Standard_Quantity_Base](Scm_Purchase_Control_Document_Lines.md#invoiced_standard_quantity_base)|
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
|Supports EQUALS_IN|no|

### Requested_Amount_Base


Requested_Amount_Base


The amount (in base currency) of the requested items (usually with Purchase Requisition). Null when the logged operation did not involve requesting items.


The amount (in base currency) of the requested items (usually with Purchase Requisition). Null when the logged operation did not involve requesting items.

| Property | Value |
| - | - |
|Type|decimal(14, 2)|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Scm_Purchase_Control_Document_Lines](Scm_Purchase_Control_Document_Lines.md).[Requested_Amount_Base](Scm_Purchase_Control_Document_Lines.md#requested_amount_base)|
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
|Supports EQUALS_IN|no|

### Ordered_Amount_Base


Ordered_Amount_Base


The amount (in base currency) of the ordered items (usually with Purchase Order). Null when the logged operation did not involve ordering items.


The amount (in base currency) of the ordered items (usually with Purchase Order). Null when the logged operation did not involve ordering items.

| Property | Value |
| - | - |
|Type|decimal(14, 2)|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Scm_Purchase_Control_Document_Lines](Scm_Purchase_Control_Document_Lines.md).[Ordered_Amount_Base](Scm_Purchase_Control_Document_Lines.md#ordered_amount_base)|
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
|Supports EQUALS_IN|no|

### Confirmed_Amount_Base


Confirmed_Amount_Base


The amount (in base currency) of the ordered items, confirmed by the supplier (usually with Purchase Confirmation). Null when the logged operation did not involve confirming ordered items.


The amount (in base currency) of the ordered items, confirmed by the supplier (usually with Purchase Confirmation). Null when the logged operation did not involve confirming ordered items.

| Property | Value |
| - | - |
|Type|decimal(14, 2)|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Scm_Purchase_Control_Document_Lines](Scm_Purchase_Control_Document_Lines.md).[Confirmed_Amount_Base](Scm_Purchase_Control_Document_Lines.md#confirmed_amount_base)|
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
|Supports EQUALS_IN|no|

### Received_Amount_Base


Received_Amount_Base


The amount (in base currency) of the received items (usually with Receiving Order). Null when the logged operation did not involve receiving items.


The amount (in base currency) of the received items (usually with Receiving Order). Null when the logged operation did not involve receiving items.

| Property | Value |
| - | - |
|Type|decimal(14, 2)|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Scm_Purchase_Control_Document_Lines](Scm_Purchase_Control_Document_Lines.md).[Received_Amount_Base](Scm_Purchase_Control_Document_Lines.md#received_amount_base)|
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
|Supports EQUALS_IN|no|

### Invoiced_Amount_Base


Invoiced_Amount_Base


The amount (in base currency) of the invoiced items (usually with Purchase Invoice). Null when the logged operation did not involve invoicing items.


The amount (in base currency) of the invoiced items (usually with Purchase Invoice). Null when the logged operation did not involve invoicing items.

| Property | Value |
| - | - |
|Type|decimal(14, 2)|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Scm_Purchase_Control_Document_Lines](Scm_Purchase_Control_Document_Lines.md).[Invoiced_Amount_Base](Scm_Purchase_Control_Document_Lines.md#invoiced_amount_base)|
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
|Supports EQUALS_IN|no|

### Purchase_Requisition_Id


Purchase_Requisition_Id


The purchase requisition which is to be or was executed. Null when the data is unknown.


The purchase requisition which is to be or was executed. Null when the data is unknown.

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
|Derived From|[Scm_Purchase_Control_Document_Lines](Scm_Purchase_Control_Document_Lines.md).[Purchase_Requisition_Id](Scm_Purchase_Control_Document_Lines.md#purchase_requisition_id)|
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

### Purchase_Requisition_Line_Id


Purchase_Requisition_Line_Id


The purchase requisition line which is to be or was executed. Null when the data is unknown.


The purchase requisition line which is to be or was executed. Null when the data is unknown.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Scm_Requisition_Lines](Scm_Requisition_Lines.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Scm_Purchase_Control_Document_Lines](Scm_Purchase_Control_Document_Lines.md).[Purchase_Requisition_Line_Id](Scm_Purchase_Control_Document_Lines.md#purchase_requisition_line_id)|
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


The purchase order which is to be or was executed. Null when the data is unknown.


The purchase order which is to be or was executed. Null when the data is unknown.

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
|Derived From|[Scm_Purchase_Control_Document_Lines](Scm_Purchase_Control_Document_Lines.md).[Purchase_Order_Id](Scm_Purchase_Control_Document_Lines.md#purchase_order_id)|
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

### Purchase_Order_Line_Id


Purchase_Order_Line_Id


The purchase order line which is to be or was executed. Null when the data is unknown.


The purchase order line which is to be or was executed. Null when the data is unknown.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Scm_Purchase_Order_Lines](Scm_Purchase_Order_Lines.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Scm_Purchase_Control_Document_Lines](Scm_Purchase_Control_Document_Lines.md).[Purchase_Order_Line_Id](Scm_Purchase_Control_Document_Lines.md#purchase_order_line_id)|
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


The receiving order which is to be or was executed. Null when the data is unknown.


The receiving order which is to be or was executed. Null when the data is unknown.

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
|Derived From|[Scm_Purchase_Control_Document_Lines](Scm_Purchase_Control_Document_Lines.md).[Receiving_Order_Id](Scm_Purchase_Control_Document_Lines.md#receiving_order_id)|
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

### Receiving_Order_Line_Id


Receiving_Order_Line_Id


The receiving order line which is to be or was executed. Null when the data is unknown.


The receiving order line which is to be or was executed. Null when the data is unknown.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Scm_Receiving_Order_Lines](Scm_Receiving_Order_Lines.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Scm_Purchase_Control_Document_Lines](Scm_Purchase_Control_Document_Lines.md).[Receiving_Order_Line_Id](Scm_Purchase_Control_Document_Lines.md#receiving_order_line_id)|
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


The purchase invoice which is to be or was executed. Null when the data is unknown.


The purchase invoice which is to be or was executed. Null when the data is unknown.

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
|Derived From|[Scm_Purchase_Control_Document_Lines](Scm_Purchase_Control_Document_Lines.md).[Purchase_Invoice_Id](Scm_Purchase_Control_Document_Lines.md#purchase_invoice_id)|
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

### Purchase_Invoice_Line_Id


Purchase_Invoice_Line_Id


The purchase invoice line which is to be or was executed. Null when the data is unknown.


The purchase invoice line which is to be or was executed. Null when the data is unknown.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Scm_Purchase_Invoice_Lines](Scm_Purchase_Invoice_Lines.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Scm_Purchase_Control_Document_Lines](Scm_Purchase_Control_Document_Lines.md).[Purchase_Invoice_Line_Id](Scm_Purchase_Control_Document_Lines.md#purchase_invoice_line_id)|
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

### Notes


Notes

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Scm_Purchase_Control_Document_Lines](Scm_Purchase_Control_Document_Lines.md).[Notes](Scm_Purchase_Control_Document_Lines.md#notes)|
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
|Max Length|2147483647|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|


