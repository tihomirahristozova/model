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


Id

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
|Derived From|[Gen_Documents](Gen_Documents.md).[Id](Gen_Documents.md#id)|
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
|Order|0|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|yes|

### From_Party_Id


From_Party_Id


The party which issued the document


The party which issued the document

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Parties](Gen_Parties.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Documents](Gen_Documents.md).[From_Party_Id](Gen_Documents.md#from_party_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|1|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|yes|

### Enterprise_Company_Id


Enterprise_Company_Id


The enterprise company which issued the document


The enterprise company which issued the document

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Enterprise_Companies](Gen_Enterprise_Companies.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Documents](Gen_Documents.md).[Enterprise_Company_Id](Gen_Documents.md#enterprise_company_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|yes|

### Document_Type_Id


Document_Type_Id


The user defined type of the document. Determines document behaviour, properties, additional amounts, validation, generations, etc.


The user defined type of the document. Determines document behaviour, properties, additional amounts, validation, generations, etc.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Document_Types](Gen_Document_Types.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Documents](Gen_Documents.md).[Document_Type_Id](Gen_Documents.md#document_type_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|3|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Document_No


Document_No


Document number, unique within Document_Type_Id


Document number, unique within Document_Type_Id

| Property | Value |
| - | - |
|Type|nvarchar|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Documents](Gen_Documents.md).[Document_No](Gen_Documents.md#document_no)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|4|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|yes|
|Like|None|no|no|

### Document_Date


Document_Date


The date on which the document was issued


The date on which the document was issued

| Property | Value |
| - | - |
|Type|date|
|DateTime Format|Date|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|CurrentDate|
|Derived From|[Gen_Documents](Gen_Documents.md).[Document_Date](Gen_Documents.md#document_date)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|5|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|yes|
|GreaterThanOrLessThan|None|yes|no|

### Reference_Date


Reference_Date


The date to which this document refers, i.e. when the action really occurred. If NULL, Document_Date is taken


The date to which this document refers, i.e. when the action really occurred. If NULL, Document_Date is taken

| Property | Value |
| - | - |
|Type|datetime|
|DateTime Format|DateTime|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|CurrentDate|
|Derived From|[Gen_Documents](Gen_Documents.md).[Reference_Date](Gen_Documents.md#reference_date)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|6|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|GreaterThanOrLessThan|None|yes|yes|

### State


State


The current system state of the document. Allowed values: 0=New;5=Corrective;10=Computer Planned;20=Human Planned;30=Released;40=Completed;50=Closed.


The current system state of the document. Allowed values: 0=New;5=Corrective;10=Computer Planned;20=Human Planned;30=Released;40=Completed;50=Closed.

| Property | Value |
| - | - |
|Type|smallint|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|yes|
|Sortable|no|
|Attributes|None|
|Allowed Values|`0`, `5`, `10`, `20`, `30`, `40`, `50`|
|Default Value|0|
|Derived From|[Gen_Documents](Gen_Documents.md).[State](Gen_Documents.md#state)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|7|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|
|GreaterThanOrLessThan|None|yes|yes|

### Void


Void


1 if the document is null and void


1 if the document is null and void

| Property | Value |
| - | - |
|Type|bit|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|yes|
|Sortable|no|
|Attributes|None|
|Default Value|False|
|Derived From|[Gen_Documents](Gen_Documents.md).[Void](Gen_Documents.md#void)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|8|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Short|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|False|no|no|

### To_Party_Id


To_Party_Id


The party which should receive the document


The party which should receive the document

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Parties](Gen_Parties.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Documents](Gen_Documents.md).[To_Party_Id](Gen_Documents.md#to_party_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|9|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|yes|

### Currency_Directory_Id


Currency_Directory_Id


The currency directory, containing all the convertion rates, used by the document. NULL means that the document does not need currency convertions


The currency directory, containing all the convertion rates, used by the document. NULL means that the document does not need currency convertions

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Currency_Directories](Gen_Currency_Directories.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Documents](Gen_Documents.md).[Currency_Directory_Id](Gen_Documents.md#currency_directory_id)|
|Format||
|Ignore for Insert Order|yes|
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
|Order|10|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|yes|

### Master_Document_Id


Master_Document_Id


In a multi-document tree, this is the root document, that created the whole tree. If this is the root it is equal to Id


In a multi-document tree, this is the root document, that created the whole tree. If this is the root it is equal to Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Documents](Gen_Documents.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Documents](Gen_Documents.md).[Master_Document_Id](Gen_Documents.md#master_document_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|11|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|yes|

### Parent_Document_Id


Parent_Document_Id


In a multi-document tree, this is the direct parent document. If this is the root it is NULL


In a multi-document tree, this is the direct parent document. If this is the root it is NULL

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Documents](Gen_Documents.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Documents](Gen_Documents.md).[Parent_Document_Id](Gen_Documents.md#parent_document_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|12|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|yes|

### Adjusted_Document_Id


Adjusted_Document_Id


The primary document, which the current document adjusts. NULL when this is not an adjustment document


The primary document, which the current document adjusts. NULL when this is not an adjustment document

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Documents](Gen_Documents.md)|
|Readonly|yes|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Documents](Gen_Documents.md).[Adjusted_Document_Id](Gen_Documents.md#adjusted_document_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|13|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|yes|

### Adjustment_Number


Adjustment_Number


Consecutive number of the correction that this document is applying to the adjusted document.


Consecutive number of the correction that this document is applying to the adjusted document.

| Property | Value |
| - | - |
|Type|int|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|yes|
|Sortable|no|
|Attributes|None|
|Default Value|0|
|Derived From|[Gen_Documents](Gen_Documents.md).[Adjustment_Number](Gen_Documents.md#adjustment_number)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|14|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Creation_Time


Creation_Time


Date/Time when the document was created


Date/Time when the document was created

| Property | Value |
| - | - |
|Type|datetime|
|DateTime Format|DateTime|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|yes|
|Sortable|no|
|Attributes|None|
|Default Value|CurrentDateTime|
|Derived From|[Gen_Documents](Gen_Documents.md).[Creation_Time](Gen_Documents.md#creation_time)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|15|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|GreaterThanOrLessThan|None|yes|yes|

### Creation_User


Creation_User


The login name of the user, who created the document


The login name of the user, who created the document

| Property | Value |
| - | - |
|Type|nvarchar|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|yes|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Documents](Gen_Documents.md).[Creation_User](Gen_Documents.md#creation_user)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|yes|
|Visible|no|
|Max Length|-1|
|Order|16|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Like|None|no|yes|

### Void_Time


Void_Time


Date/time when the document has become void


Date/time when the document has become void

| Property | Value |
| - | - |
|Type|datetime|
|DateTime Format|DateTime|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|yes|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Documents](Gen_Documents.md).[Void_Time](Gen_Documents.md#void_time)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|17|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Void_User


Void_User


The user who voided the document


The user who voided the document

| Property | Value |
| - | - |
|Type|nvarchar|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|yes|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Documents](Gen_Documents.md).[Void_User](Gen_Documents.md#void_user)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|yes|
|Visible|no|
|Max Length|-1|
|Order|18|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Adjustment_Time


Adjustment_Time


Date/time when the document last has been adjusted by corrective document


Date/time when the document last has been adjusted by corrective document

| Property | Value |
| - | - |
|Type|datetime|
|DateTime Format|DateTime|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|yes|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Documents](Gen_Documents.md).[Adjustment_Time](Gen_Documents.md#adjustment_time)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|19|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Adjustment_User


Adjustment_User


The user who adjusted the document


The user who adjusted the document

| Property | Value |
| - | - |
|Type|nvarchar|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|yes|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Documents](Gen_Documents.md).[Adjustment_User](Gen_Documents.md#adjustment_user)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|yes|
|Visible|no|
|Max Length|-1|
|Order|20|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Read_Only


Read_Only


1 - the document is read only; 0 - the document is not read only


1 - the document is read only; 0 - the document is not read only

| Property | Value |
| - | - |
|Type|bit|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|yes|
|Sortable|no|
|Attributes|None|
|Default Value|False|
|Derived From|[Gen_Documents](Gen_Documents.md).[Read_Only](Gen_Documents.md#read_only)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|21|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Short|
|Supports EQUALS_IN|no|

### Document_Notes


Document_Notes

| Property | Value |
| - | - |
|Type|nvarchar|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None, IsLongString|
|Default Value|None|
|Derived From|[Gen_Documents](Gen_Documents.md).[Notes](Gen_Documents.md#notes)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|22|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Document_Version


Document_Version


Consecutive version number, starting with 1. Each update produces a new version of the document.


Consecutive version number, starting with 1. Each update produces a new version of the document.

| Property | Value |
| - | - |
|Type|int|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|yes|
|Sortable|no|
|Attributes|None|
|Default Value|1|
|Derived From|[Gen_Documents](Gen_Documents.md).[Document_Version](Gen_Documents.md#document_version)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|23|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|yes|
|GreaterThanOrLessThan|None|yes|yes|

### Responsible_Person_Id


Responsible_Person_Id


The person that is responsible for this order or transaction. It could be the sales person, the orderer, etc.


The person that is responsible for this order or transaction. It could be the sales person, the orderer, etc.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Cm_Persons](Cm_Persons.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Documents](Gen_Documents.md).[Responsible_Person_Id](Gen_Documents.md#responsible_person_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|24|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Void_Reason


Void_Reason


Reason for voiding the document, entered by the user


Reason for voiding the document, entered by the user

| Property | Value |
| - | - |
|Type|nvarchar|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|yes|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Documents](Gen_Documents.md).[Void_Reason](Gen_Documents.md#void_reason)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|25|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
|Supports EQUALS_IN|no|

### Reverse_Of_Document_Id


Reverse_Of_Document_Id


The document which the current document is reverse of


The document which the current document is reverse of

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Documents](Gen_Documents.md)|
|Readonly|yes|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Documents](Gen_Documents.md).[Reverse_Of_Document_Id](Gen_Documents.md#reverse_of_document_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|26|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|yes|

### Enterprise_Company_Location_Id


Enterprise_Company_Location_Id


The enterprise company location which issued the document. NULL means that there is only one location within the enterprise company and locations are not used


The enterprise company location which issued the document. NULL means that there is only one location within the enterprise company and locations are not used

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Cm_Company_Locations](Cm_Company_Locations.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Documents](Gen_Documents.md).[Enterprise_Company_Location_Id](Gen_Documents.md#enterprise_company_location_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|27|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Planning_Only


Planning_Only


Indicates that the document is used only for planning (and as consequence its state cannot be greater than Planned)


Indicates that the document is used only for planning (and as consequence its state cannot be greater than Planned)

| Property | Value |
| - | - |
|Type|bit|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|yes|
|Sortable|no|
|Attributes|None|
|Default Value|False|
|Derived From|[Gen_Documents](Gen_Documents.md).[Planning_Only](Gen_Documents.md#planning_only)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|28|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Short|
|Supports EQUALS_IN|no|

### Prime_Cause_Document_Id


Prime_Cause_Document_Id


The document that is the prime cause for creation of the current document


The document that is the prime cause for creation of the current document

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Documents](Gen_Documents.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Documents](Gen_Documents.md).[Prime_Cause_Document_Id](Gen_Documents.md#prime_cause_document_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|29|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Release_Time


Release_Time


Date and time when the document was released (State set to Released).


Date and time when the document was released (State set to Released).

| Property | Value |
| - | - |
|Type|datetime|
|DateTime Format|DateTime|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|yes|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Documents](Gen_Documents.md).[Release_Time](Gen_Documents.md#release_time)|
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
|Order|30|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|GreaterThanOrLessThan|None|yes|yes|

### Complete_Time


Complete_Time


Date and time when the document was completed (State set to Completed).


Date and time when the document was completed (State set to Completed).

| Property | Value |
| - | - |
|Type|datetime|
|DateTime Format|DateTime|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|yes|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Documents](Gen_Documents.md).[Complete_Time](Gen_Documents.md#complete_time)|
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
|Order|31|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|GreaterThanOrLessThan|None|yes|yes|

### Parent_Document_Relationship_Type


Parent_Document_Relationship_Type


Type of relationship between the current document and the parent document(s). Affects the constraints for execution/completion for the documents. Possible values: 'S' = 'Subtask', 'N' = 'Next task'.


Type of relationship between the current document and the parent document(s). Affects the constraints for execution/completion for the documents. Possible values: 'S' = 'Subtask', 'N' = 'Next task'.

| Property | Value |
| - | - |
|Type|nvarchar|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|yes|
|Sortable|no|
|Attributes|None|
|Allowed Values|`S`, `N`|
|Default Value|None|
|Derived From|[Gen_Documents](Gen_Documents.md).[Parent_Document_Relationship_Type](Gen_Documents.md#parent_document_relationship_type)|
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
|Order|32|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Reference_Document_No


Reference_Document_No


The number of the document (issued by the other party), which was the reason for the creation of the current document. The numebr should be unique within the party documents


The number of the document (issued by the other party), which was the reason for the creation of the current document. The numebr should be unique within the party documents

| Property | Value |
| - | - |
|Type|nvarchar|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Documents](Gen_Documents.md).[Reference_Document_No](Gen_Documents.md#reference_document_no)|
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
|Order|33|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|yes|
|Like|None|no|no|

### User_Status_Id


User_Status_Id


The user status of this document if applicable for this document type. NULL means unknown or not yet set


The user status of this document if applicable for this document type. NULL means unknown or not yet set

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Document_Type_User_Statuses](Gen_Document_Type_User_Statuses.md)|
|Readonly|yes|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Documents](Gen_Documents.md).[User_Status_Id](Gen_Documents.md#user_status_id)|
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
|Order|34|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### From_Company_Division_Id


From_Company_Division_Id


The division of the company, issuing the document. NULL when the document is not issued by any specific division


The division of the company, issuing the document. NULL when the document is not issued by any specific division

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Cm_Company_Divisions](Cm_Company_Divisions.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Documents](Gen_Documents.md).[From_Company_Division_Id](Gen_Documents.md#from_company_division_id)|
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
|Order|35|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### To_Company_Division_Id


To_Company_Division_Id


The division of the company, receiving the document. NULL when the document is not received by any specific division


The division of the company, receiving the document. NULL when the document is not received by any specific division

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Cm_Company_Divisions](Cm_Company_Divisions.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Documents](Gen_Documents.md).[To_Company_Division_Id](Gen_Documents.md#to_company_division_id)|
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
|Order|36|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Entity_Name


Entity_Name


The entity name of the document header.


The entity name of the document header.

| Property | Value |
| - | - |
|Type|nvarchar|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Documents](Gen_Documents.md).[Entity_Name](Gen_Documents.md#entity_name)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|yes|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|37|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

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
|Ownership Reference|no|
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
|Visible|yes|
|Max Length|-1|
|Order|38|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Document_Purchase_Requisition_Id


Document_Purchase_Requisition_Id


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
|Order|39|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Document_Purchase_Order_Id


Document_Purchase_Order_Id


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
|Order|40|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Document_Receiving_Order_Id


Document_Receiving_Order_Id


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
|Order|41|
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
|Order|42|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Document_Purchase_Invoice_Id


Document_Purchase_Invoice_Id


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
|Order|42|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

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
|Visible|yes|
|Max Length|-1|
|Order|43|
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
|Ownership Reference|no|
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
|Visible|yes|
|Max Length|-1|
|Order|44|
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
|Order|45|
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
|Order|46|
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
|Type|decimal(0, 0)|
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
|Order|47|
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
|Type|decimal(0, 0)|
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
|Order|48|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Confirmed_Standard_Quantity_Base


Confirmed_Standard_Quantity_Base


The standard quantity of the ordered items, confirmed by the supplier (usually with Purchase Order or Purchase Confirmation) in base measurement unit. Null when the logged operation did not involve confirming ordered items.


The standard quantity of the ordered items, confirmed by the supplier (usually with Purchase Order or Purchase Confirmation) in base measurement unit. Null when the logged operation did not involve confirming ordered items.

| Property | Value |
| - | - |
|Type|decimal(0, 0)|
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
|Order|49|
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
|Type|decimal(0, 0)|
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
|Order|50|
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
|Type|decimal(0, 0)|
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
|Order|51|
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
|Type|decimal(0, 0)|
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
|Order|52|
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
|Type|decimal(0, 0)|
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
|Order|53|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Confirmed_Amount_Base


Confirmed_Amount_Base


The amount (in base currency) of the ordered items, confirmed by the supplier (usually with Purchase Order or Purchase Confirmation). Null when the logged operation did not involve confirming ordered items.


The amount (in base currency) of the ordered items, confirmed by the supplier (usually with Purchase Order or Purchase Confirmation). Null when the logged operation did not involve confirming ordered items.

| Property | Value |
| - | - |
|Type|decimal(0, 0)|
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
|Order|54|
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
|Type|decimal(0, 0)|
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
|Order|55|
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
|Type|decimal(0, 0)|
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
|Order|56|
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
|Order|57|
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
|Order|58|
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
|Order|59|
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
|Order|60|
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
|Order|61|
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
|Order|62|
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
|Order|64|
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
|Type|nvarchar|
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
|Max Length|-1|
|Order|65|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Purchase_Invoice_Document_No


Purchase_Invoice_Document_No

| Property | Value |
| - | - |
|Type|nvarchar|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Documents](Gen_Documents.md).[Document_No](Gen_Documents.md#document_no)|
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

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|yes|
|Like|None|no|no|

### Receiving_Order_Document_Date


Receiving_Order_Document_Date

| Property | Value |
| - | - |
|Type|date|
|DateTime Format|Date|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|CurrentDate|
|Derived From|[Gen_Documents](Gen_Documents.md).[Document_Date](Gen_Documents.md#document_date)|
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

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|yes|
|GreaterThanOrLessThan|None|yes|no|

### Receiving_Order_Document_Type_Id


Receiving_Order_Document_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Document_Types](Gen_Document_Types.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Documents](Gen_Documents.md).[Document_Type_Id](Gen_Documents.md#document_type_id)|
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
|Equals|NULL|no|no|

### Receiving_Order_Document_No


Receiving_Order_Document_No

| Property | Value |
| - | - |
|Type|nvarchar|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Documents](Gen_Documents.md).[Document_No](Gen_Documents.md#document_no)|
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

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|yes|
|Like|None|no|no|

### Purchase_Order_Document_Date


Purchase_Order_Document_Date

| Property | Value |
| - | - |
|Type|date|
|DateTime Format|Date|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|CurrentDate|
|Derived From|[Gen_Documents](Gen_Documents.md).[Document_Date](Gen_Documents.md#document_date)|
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

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|yes|
|GreaterThanOrLessThan|None|yes|no|

### Requisition_Document_Date


Requisition_Document_Date

| Property | Value |
| - | - |
|Type|date|
|DateTime Format|Date|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|CurrentDate|
|Derived From|[Gen_Documents](Gen_Documents.md).[Document_Date](Gen_Documents.md#document_date)|
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

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|yes|
|GreaterThanOrLessThan|None|yes|no|

### Purchase_Order_Document_No


Purchase_Order_Document_No

| Property | Value |
| - | - |
|Type|nvarchar|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Documents](Gen_Documents.md).[Document_No](Gen_Documents.md#document_no)|
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

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|yes|
|Like|None|no|no|

### Requisition_Document_Type_Id


Requisition_Document_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Document_Types](Gen_Document_Types.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Documents](Gen_Documents.md).[Document_Type_Id](Gen_Documents.md#document_type_id)|
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
|Equals|NULL|no|no|

### Requisition_Document_No


Requisition_Document_No

| Property | Value |
| - | - |
|Type|nvarchar|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Documents](Gen_Documents.md).[Document_No](Gen_Documents.md#document_no)|
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

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|yes|
|Like|None|no|no|

### Purchase_Invoice_Document_Type_Id


Purchase_Invoice_Document_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Document_Types](Gen_Document_Types.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Documents](Gen_Documents.md).[Document_Type_Id](Gen_Documents.md#document_type_id)|
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
|Equals|NULL|no|no|

### Purchase_Order_Document_Type_Id


Purchase_Order_Document_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Document_Types](Gen_Document_Types.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Documents](Gen_Documents.md).[Document_Type_Id](Gen_Documents.md#document_type_id)|
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
|Equals|NULL|no|no|

### Purchase_Invoice_Document_Date


Purchase_Invoice_Document_Date

| Property | Value |
| - | - |
|Type|date|
|DateTime Format|Date|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|CurrentDate|
|Derived From|[Gen_Documents](Gen_Documents.md).[Document_Date](Gen_Documents.md#document_date)|
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

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|yes|
|GreaterThanOrLessThan|None|yes|no|


