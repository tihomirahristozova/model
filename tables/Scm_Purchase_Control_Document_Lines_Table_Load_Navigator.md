# Query Scm_Purchase_Control_Document_Lines_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Id](#id)|`uniqueidentifier` `PK`||
|[From_Party_Id](#from_party_id)|`uniqueidentifier` |The party which issued the document|
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` |The enterprise company which issued the document|
|[Document_Type_Id](#document_type_id)|`uniqueidentifier` |The user defined type of the document. Determines document behaviour, properties, additional amounts, validation, generations, etc.|
|[Document_No](#document_no)|`nvarchar` |Document number, unique within Document_Type_Id|
|[Document_Date](#document_date)|`date` |The date on which the document was issued|
|[Reference_Date](#reference_date)|`datetime` |The date to which this document refers, i.e. when the action really occurred. If NULL, Document_Date is taken|
|[State](#state)|`smallint` Allowed: `0`, `5`, `10`, `20`, `30`, `40`, `50`, Readonly|The current system state of the document. Allowed values: 0=New;5=Corrective;10=Computer Planned;20=Human Planned;30=Released;40=Completed;50=Closed.|
|[Void](#void)|`bit` Readonly|1 if the document is null and void|
|[To_Party_Id](#to_party_id)|`uniqueidentifier` |The party which should receive the document|
|[Currency_Directory_Id](#currency_directory_id)|`uniqueidentifier` |The currency directory, containing all the convertion rates, used by the document. NULL means that the document does not need currency convertions|
|[Master_Document_Id](#master_document_id)|`uniqueidentifier` |In a multi-document tree, this is the root document, that created the whole tree. If this is the root it is equal to Id|
|[Parent_Document_Id](#parent_document_id)|`uniqueidentifier` |In a multi-document tree, this is the direct parent document. If this is the root it is NULL|
|[Adjusted_Document_Id](#adjusted_document_id)|`uniqueidentifier` Readonly|The primary document, which the current document adjusts. NULL when this is not an adjustment document|
|[Adjustment_Number](#adjustment_number)|`int` Readonly|Consecutive number of the correction that this document is applying to the adjusted document.|
|[Creation_Time](#creation_time)|`datetime` Readonly|Date/Time when the document was created|
|[Creation_User](#creation_user)|`nvarchar` Readonly|The login name of the user, who created the document|
|[Void_Time](#void_time)|`datetime` Readonly|Date/time when the document has become void|
|[Void_User](#void_user)|`nvarchar` Readonly|The user who voided the document|
|[Adjustment_Time](#adjustment_time)|`datetime` Readonly|Date/time when the document last has been adjusted by corrective document|
|[Adjustment_User](#adjustment_user)|`nvarchar` Readonly|The user who adjusted the document|
|[Read_Only](#read_only)|`bit` Readonly|1 - the document is read only; 0 - the document is not read only|
|[Document_Notes](#document_notes)|`nvarchar` ||
|[Document_Version](#document_version)|`int` Readonly|Consecutive version number, starting with 1. Each update produces a new version of the document.|
|[Responsible_Person_Id](#responsible_person_id)|`uniqueidentifier` |The person that is responsible for this order or transaction. It could be the sales person, the orderer, etc.|
|[Void_Reason](#void_reason)|`nvarchar` Readonly|Reason for voiding the document, entered by the user|
|[Reverse_Of_Document_Id](#reverse_of_document_id)|`uniqueidentifier` Readonly|The document which the current document is reverse of|
|[Enterprise_Company_Location_Id](#enterprise_company_location_id)|`uniqueidentifier` |The enterprise company location which issued the document. NULL means that there is only one location within the enterprise company and locations are not used|
|[Planning_Only](#planning_only)|`bit` Readonly|Indicates that the document is used only for planning (and as consequence its state cannot be greater than Planned)|
|[Prime_Cause_Document_Id](#prime_cause_document_id)|`uniqueidentifier` |The document that is the prime cause for creation of the current document|
|[Release_Time](#release_time)|`datetime` Readonly|Date and time when the document was released (State set to Released).|
|[Complete_Time](#complete_time)|`datetime` Readonly|Date and time when the document was completed (State set to Completed).|
|[Parent_Document_Relationship_Type](#parent_document_relationship_type)|`nvarchar` Allowed: `S`, `N`, Readonly|Type of relationship between the current document and the parent document(s). Affects the constraints for execution/completion for the documents. Possible values: 'S' = 'Subtask', 'N' = 'Next task'.|
|[Reference_Document_No](#reference_document_no)|`nvarchar` |The number of the document (issued by the other party), which was the reason for the creation of the current document. The numebr should be unique within the party documents|
|[User_Status_Id](#user_status_id)|`uniqueidentifier` Readonly|The user status of this document if applicable for this document type. NULL means unknown or not yet set|
|[From_Company_Division_Id](#from_company_division_id)|`uniqueidentifier` |The division of the company, issuing the document. NULL when the document is not issued by any specific division|
|[To_Company_Division_Id](#to_company_division_id)|`uniqueidentifier` |The division of the company, receiving the document. NULL when the document is not received by any specific division|
|[Entity_Name](#entity_name)|`nvarchar` |The entity name of the document header.|
|[Document_Id](#document_id)|`uniqueidentifier` ||
|[Document_Purchase_Requisition_Id](#document_purchase_requisition_id)|`uniqueidentifier` |The purchase requisition, when it is the same for all lines. NULL when it is null for the lines or the lines have different values.|
|[Document_Purchase_Order_Id](#document_purchase_order_id)|`uniqueidentifier` |The purchase order, when it is the same for all lines. NULL when it is null for the lines or the lines have different values.|
|[Document_Receiving_Order_Id](#document_receiving_order_id)|`uniqueidentifier` |The receiving order, when it is the same for all lines. NULL when it is null for the lines or the lines have different values.|
|[Purchase_Invoice_Id](#purchase_invoice_id)|`uniqueidentifier` |The purchase invoice, when it is the same for all lines. NULL when it is null for the lines or the lines have different values.|
|[Document_Purchase_Invoice_Id](#document_purchase_invoice_id)|`uniqueidentifier` |The purchase invoice, when it is the same for all lines. NULL when it is null for the lines or the lines have different values.|
|[Purchase_Control_Document_Line_Id](#purchase_control_document_line_id)|`uniqueidentifier` `PK`||
|[Purchase_Control_Document_Id](#purchase_control_document_id)|`uniqueidentifier` ||
|[Line_No](#line_no)|`int` |The consecutive line number within the control document.|
|[Purchase_Operation_Type_Id](#purchase_operation_type_id)|`uniqueidentifier` |The user-defined operation type, which is being recorded by the current line. Used for better grouping of the control entries. NULL when the operation type was not specified by the user.|
|[Requested_Standard_Quantity_Base](#requested_standard_quantity_base)|`decimal(0, 0)` |The standard quantity of the requested items (usually with Purchase Requisition) in base measurement unit. Null when the logged operation did not involve requesting items.|
|[Ordered_Standard_Quantity_Base](#ordered_standard_quantity_base)|`decimal(0, 0)` |The standard quantity of the ordered items (usually with Purchase Order) in base measurement unit. Null when the logged operation did not involve ordering items.|
|[Confirmed_Standard_Quantity_Base](#confirmed_standard_quantity_base)|`decimal(0, 0)` |The standard quantity of the ordered items, confirmed by the supplier (usually with Purchase Order or Purchase Confirmation) in base measurement unit. Null when the logged operation did not involve confirming ordered items.|
|[Received_Standard_Quantity_Base](#received_standard_quantity_base)|`decimal(0, 0)` |The standard quantity of the received items (usually with Receiving Order) in base measurement unit. Null when the logged operation did not involve receiving items.|
|[Invoiced_Standard_Quantity_Base](#invoiced_standard_quantity_base)|`decimal(0, 0)` |The standard quantity of the invoiced items (usually with Purchase Invoice) in base measurement unit. Null when the logged operation did not involve invoicing items.|
|[Requested_Amount_Base](#requested_amount_base)|`decimal(0, 0)` |The amount (in base currency) of the requested items (usually with Purchase Requisition). Null when the logged operation did not involve requesting items.|
|[Ordered_Amount_Base](#ordered_amount_base)|`decimal(0, 0)` |The amount (in base currency) of the ordered items (usually with Purchase Order). Null when the logged operation did not involve ordering items.|
|[Confirmed_Amount_Base](#confirmed_amount_base)|`decimal(0, 0)` |The amount (in base currency) of the ordered items, confirmed by the supplier (usually with Purchase Order or Purchase Confirmation). Null when the logged operation did not involve confirming ordered items.|
|[Received_Amount_Base](#received_amount_base)|`decimal(0, 0)` |The amount (in base currency) of the received items (usually with Receiving Order). Null when the logged operation did not involve receiving items.|
|[Invoiced_Amount_Base](#invoiced_amount_base)|`decimal(0, 0)` |The amount (in base currency) of the invoiced items (usually with Purchase Invoice). Null when the logged operation did not involve invoicing items.|
|[Purchase_Requisition_Id](#purchase_requisition_id)|`uniqueidentifier` |The purchase requisition which is to be or was executed. Null when the data is unknown.|
|[Purchase_Requisition_Line_Id](#purchase_requisition_line_id)|`uniqueidentifier` |The purchase requisition line which is to be or was executed. Null when the data is unknown.|
|[Purchase_Order_Id](#purchase_order_id)|`uniqueidentifier` |The purchase order which is to be or was executed. Null when the data is unknown.|
|[Purchase_Order_Line_Id](#purchase_order_line_id)|`uniqueidentifier` |The purchase order line which is to be or was executed. Null when the data is unknown.|
|[Receiving_Order_Id](#receiving_order_id)|`uniqueidentifier` |The receiving order which is to be or was executed. Null when the data is unknown.|
|[Receiving_Order_Line_Id](#receiving_order_line_id)|`uniqueidentifier` |The receiving order line which is to be or was executed. Null when the data is unknown.|
|[Purchase_Invoice_Line_Id](#purchase_invoice_line_id)|`uniqueidentifier` |The purchase invoice line which is to be or was executed. Null when the data is unknown.|
|[Notes](#notes)|`nvarchar` ||
|[Purchase_Invoice_Document_No](#purchase_invoice_document_no)|`nvarchar` ||
|[Receiving_Order_Document_Date](#receiving_order_document_date)|`date` ||
|[Receiving_Order_Document_Type_Id](#receiving_order_document_type_id)|`uniqueidentifier` ||
|[Receiving_Order_Document_No](#receiving_order_document_no)|`nvarchar` ||
|[Purchase_Order_Document_Date](#purchase_order_document_date)|`date` ||
|[Requisition_Document_Date](#requisition_document_date)|`date` ||
|[Purchase_Order_Document_No](#purchase_order_document_no)|`nvarchar` ||
|[Requisition_Document_Type_Id](#requisition_document_type_id)|`uniqueidentifier` ||
|[Requisition_Document_No](#requisition_document_no)|`nvarchar` ||
|[Purchase_Invoice_Document_Type_Id](#purchase_invoice_document_type_id)|`uniqueidentifier` ||
|[Purchase_Order_Document_Type_Id](#purchase_order_document_type_id)|`uniqueidentifier` ||
|[Purchase_Invoice_Document_Date](#purchase_invoice_document_date)|`date` ||

## Columns

### Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### From_Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_No

| Property | Value |
| - | - |
|Type|nvarchar|

### Document_Date

| Property | Value |
| - | - |
|Type|date|

### Reference_Date

| Property | Value |
| - | - |
|Type|datetime|

### State

| Property | Value |
| - | - |
|Type|smallint|

### Void

| Property | Value |
| - | - |
|Type|bit|

### To_Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Currency_Directory_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Master_Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Parent_Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Adjusted_Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Adjustment_Number

| Property | Value |
| - | - |
|Type|int|

### Creation_Time

| Property | Value |
| - | - |
|Type|datetime|

### Creation_User

| Property | Value |
| - | - |
|Type|nvarchar|

### Void_Time

| Property | Value |
| - | - |
|Type|datetime|

### Void_User

| Property | Value |
| - | - |
|Type|nvarchar|

### Adjustment_Time

| Property | Value |
| - | - |
|Type|datetime|

### Adjustment_User

| Property | Value |
| - | - |
|Type|nvarchar|

### Read_Only

| Property | Value |
| - | - |
|Type|bit|

### Document_Notes

| Property | Value |
| - | - |
|Type|nvarchar|

### Document_Version

| Property | Value |
| - | - |
|Type|int|

### Responsible_Person_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Void_Reason

| Property | Value |
| - | - |
|Type|nvarchar|

### Reverse_Of_Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Enterprise_Company_Location_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Planning_Only

| Property | Value |
| - | - |
|Type|bit|

### Prime_Cause_Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Release_Time

| Property | Value |
| - | - |
|Type|datetime|

### Complete_Time

| Property | Value |
| - | - |
|Type|datetime|

### Parent_Document_Relationship_Type

| Property | Value |
| - | - |
|Type|nvarchar|

### Reference_Document_No

| Property | Value |
| - | - |
|Type|nvarchar|

### User_Status_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### From_Company_Division_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### To_Company_Division_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Entity_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Purchase_Requisition_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Purchase_Order_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Receiving_Order_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Purchase_Invoice_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Purchase_Invoice_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

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
|Type|decimal(0, 0)|

### Ordered_Standard_Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Confirmed_Standard_Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Received_Standard_Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Invoiced_Standard_Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Requested_Amount_Base

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Ordered_Amount_Base

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Confirmed_Amount_Base

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Received_Amount_Base

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Invoiced_Amount_Base

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

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

### Purchase_Invoice_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar|

### Purchase_Invoice_Document_No

| Property | Value |
| - | - |
|Type|nvarchar|

### Receiving_Order_Document_Date

| Property | Value |
| - | - |
|Type|date|

### Receiving_Order_Document_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Receiving_Order_Document_No

| Property | Value |
| - | - |
|Type|nvarchar|

### Purchase_Order_Document_Date

| Property | Value |
| - | - |
|Type|date|

### Requisition_Document_Date

| Property | Value |
| - | - |
|Type|date|

### Purchase_Order_Document_No

| Property | Value |
| - | - |
|Type|nvarchar|

### Requisition_Document_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Requisition_Document_No

| Property | Value |
| - | - |
|Type|nvarchar|

### Purchase_Invoice_Document_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Purchase_Order_Document_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Purchase_Invoice_Document_Date

| Property | Value |
| - | - |
|Type|date|


