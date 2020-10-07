# Logistics.Procurement.ReceivingOrders

Contains the received quantities from a supplier. Entity: Scm_Receiving_Orders

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Logistics.Procurement.ReceivingOrders.md#Id) | guid |  
| [CompleteTime](Logistics.Procurement.ReceivingOrders.md#CompleteTime) | datetime (nullable) | Exact time, when the document was last completed[Filter(ge;le)] 
| [CreationTime](Logistics.Procurement.ReceivingOrders.md#CreationTime) | datetime | Date/Time when the document was created [Required][Filter(ge;le)] 
| [CreationUser](Logistics.Procurement.ReceivingOrders.md#CreationUser) | string | The login name of the user, who created the document [Required][Filter(like)] 
| [DocumentDate](Logistics.Procurement.ReceivingOrders.md#DocumentDate) | datetime | The date on which the document was issued [Required][Filter(eq;ge;le)][ORD] 
| [DocumentNo](Logistics.Procurement.ReceivingOrders.md#DocumentNo) | string | Document number, unique within Document_Type_Id [Required][Filter(eq;like)][ORD] 
| [DocumentVersion](Logistics.Procurement.ReceivingOrders.md#DocumentVersion) | int32 | [Filter(eq;ge;le)] 
| [DocumentNotes](Logistics.Procurement.ReceivingOrders.md#DocumentNotes) | string (nullable) | Notes for this Document 
| [ParentDocumentRelationshipType](Logistics.Procurement.ReceivingOrders.md#ParentDocumentRelationshipType) | [General.ParentDocumentRelationshipType](Logistics.Procurement.ReceivingOrders.md#ParentDocumentRelationshipType) (nullable) | Type of relationship between the current document and the parent document(s). Affects the constraints for execution/completion for the documents. Possible values: 'S' = 'Subtask', 'N' = 'Next task'. 
| [PlanningOnly](Logistics.Procurement.ReceivingOrders.md#PlanningOnly) | boolean (nullable) | Indicates that the document is used only for planning (and as consequence its state cannot be greater than Planned) [Required] 
| [ReadOnly](Logistics.Procurement.ReceivingOrders.md#ReadOnly) | boolean | True - the document is read only; false - the document is not read only [Required] 
| [ReferenceDate](Logistics.Procurement.ReceivingOrders.md#ReferenceDate) | datetime (nullable) | The date to which this document refers, i.e. when the action really occurred. If null, Document_Date is taken [Filter(ge;le)] 
| [ReferenceDocumentNo](Logistics.Procurement.ReceivingOrders.md#ReferenceDocumentNo) | string (nullable) | The number of the document (issued by the other party), which was the reason for the creation of the current document. The numebr should be unique within the party documents [Filter(eq;like)] 
| [ReleaseTime](Logistics.Procurement.ReceivingOrders.md#ReleaseTime) | datetime (nullable) | Exact time, when the document was first released [Filter(ge;le)] 
| [State](Logistics.Procurement.ReceivingOrders.md#State) | [General.DocumentState](Logistics.Procurement.ReceivingOrders.md#State) | 0=New;5=Corrective;10=Computer Planned;20=Human Planned;30=Released;40=Completed;50=Closed [Required][Filter(eq;ge;le)] 
| [Void](Logistics.Procurement.ReceivingOrders.md#Void) | boolean | True if the document is null and void [Required][Filter(eq)] 
| [VoidReason](Logistics.Procurement.ReceivingOrders.md#VoidReason) | string (nullable) | Reason for voiding the document, entered by the user 
| [VoidTime](Logistics.Procurement.ReceivingOrders.md#VoidTime) | datetime (nullable) | Date/time when the document has become void 
| [VoidUser](Logistics.Procurement.ReceivingOrders.md#VoidUser) | string (nullable) | The user who voided the document 
| [EntityName](Logistics.Procurement.ReceivingOrders.md#EntityName) | string | The entity name of the document equal to the entity name of the document type.[Filter(eq)] [ORD] 
| [InvoiceDocumentNo](Logistics.Procurement.ReceivingOrders.md#InvoiceDocumentNo) | string (nullable) | Contains the purchase invoice number when it is known in advance, null otherwise. [Filter(eq)] 
| [IsReleased](Logistics.Procurement.ReceivingOrders.md#IsReleased) | boolean | True if the document is not void and its state is released or greater. [Required] [Default(false)] [Filter(eq)] [ReadOnly] 
| [IsSingleExecution](Logistics.Procurement.ReceivingOrders.md#IsSingleExecution) | boolean | Specifies whether the document is a single execution of its order document. [Required] [Default(false)] [Filter(eq)] [ReadOnly] 
| [Notes](Logistics.Procurement.ReceivingOrders.md#Notes) | string (nullable) | Notes for this ReceivingOrder. 
| [PaymentDueDate](Logistics.Procurement.ReceivingOrders.md#PaymentDueDate) | datetime (nullable) | Due date for the payment. When null, the payment due date is the documents date. [Filter(ge;le)] 
| [PlannedDeliveryDate](Logistics.Procurement.ReceivingOrders.md#PlannedDeliveryDate) | datetime (nullable) | When not null, specifies the planned delivery date for all lines. [Filter(ge;le)] 
| [PlannedReleaseDate](Logistics.Procurement.ReceivingOrders.md#PlannedReleaseDate) | datetime (nullable) | The date, when the document is planned to be realeased. [Filter(ge;le)] 
| [PurchaseLotDescription](Logistics.Procurement.ReceivingOrders.md#PurchaseLotDescription) | string (nullable) | Description of the purchase lot for the whole document. It is set for the lots created by this receiving order. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [AccessKey](Logistics.Procurement.ReceivingOrders.md#AccessKey) | [Systems.Security.AccessKeys](Systems.Security.AccessKeys.md) (nullable) | The access key, containing the user permissions for this document. null means that all users have unlimited permissions |
| [AdjustedDocument](Logistics.Procurement.ReceivingOrders.md#AdjustedDocument) | [General.Documents](General.Documents.md) (nullable) | The primary document, which the current document adjusts. null when this is not an adjustment document |
| [AssignedToUser](Logistics.Procurement.ReceivingOrders.md#AssignedToUser) | [Systems.Security.Users](Systems.Security.Users.md) (nullable) | The user to which this document is assigned for handling. null means that the document is not assigned to specific user |
| [CurrencyDirectory](Logistics.Procurement.ReceivingOrders.md#CurrencyDirectory) | [General.CurrencyDirectories](General.CurrencyDirectories.md) (nullable) | The currency directory, containing all the convertion rates, used by the document. null means that the document does not need currency convertions |
| [DocumentType](Logistics.Procurement.ReceivingOrders.md#DocumentType) | [General.DocumentTypes](General.DocumentTypes.md) | The user defined type of the document. Determines document behaviour, properties, additional amounts, validation, generations, etc. [Required] |
| [EnterpriseCompany](Logistics.Procurement.ReceivingOrders.md#EnterpriseCompany) | [General.EnterpriseCompanies](General.EnterpriseCompanies.md) | The enterprise company which issued the document [Required] |
| [EnterpriseCompanyLocation](Logistics.Procurement.ReceivingOrders.md#EnterpriseCompanyLocation) | [General.Contacts.CompanyLocations](General.Contacts.CompanyLocations.md) (nullable) | The enterprise company location which issued the document. null means that there is only one location within the enterprise company and locations are not used |
| [FromCompanyDivision](Logistics.Procurement.ReceivingOrders.md#FromCompanyDivision) | [General.Contacts.CompanyDivisions](General.Contacts.CompanyDivisions.md) (nullable) | The division of the company, issuing the document. null when the document is not issued by any specific division |
| [FromParty](Logistics.Procurement.ReceivingOrders.md#FromParty) | [General.Contacts.Parties](General.Contacts.Parties.md) | The party which issued the document [Required] |
| [MasterDocument](Logistics.Procurement.ReceivingOrders.md#MasterDocument) | [General.Documents](General.Documents.md) | In a multi-document tree, this is the root document, that created the whole tree. If this is the root it is equal to Id [Required] |
| [Parent](Logistics.Procurement.ReceivingOrders.md#Parent) | [General.Documents](General.Documents.md) (nullable) | In a multi-document tree, this is the direct parent document. If this is the root it is null |
| [PrimeCauseDocument](Logistics.Procurement.ReceivingOrders.md#PrimeCauseDocument) | [General.Documents](General.Documents.md) (nullable) | The document that is the prime cause for creation of the current document |
| [ResponsiblePerson](Logistics.Procurement.ReceivingOrders.md#ResponsiblePerson) | [General.Contacts.Persons](General.Contacts.Persons.md) (nullable) | The person that is responsible for this order or transaction. It could be the sales person, the orderer, etc. |
| [ReverseOfDocument](Logistics.Procurement.ReceivingOrders.md#ReverseOfDocument) | [General.Documents](General.Documents.md) (nullable) | The document which the current document is reverse of |
| [Sequence](Logistics.Procurement.ReceivingOrders.md#Sequence) | [General.Sequences](General.Sequences.md) (nullable) | The sequence that will be used to give new numbers to the documents of this type |
| [ToCompanyDivision](Logistics.Procurement.ReceivingOrders.md#ToCompanyDivision) | [General.Contacts.CompanyDivisions](General.Contacts.CompanyDivisions.md) | The division of the company, receiving the document. null when the document is not received by any specific division |
| [ToParty](Logistics.Procurement.ReceivingOrders.md#ToParty) | [General.Contacts.Parties](General.Contacts.Parties.md) (nullable) | The party which should receive the document |
| [UserStatus](Logistics.Procurement.ReceivingOrders.md#UserStatus) | [General.DocumentTypeUserStatuses](General.DocumentTypeUserStatuses.md) (nullable) | The user status of this document if applicable for this document type. null means unknown or not yet set |
| [DocumentCurrency](Logistics.Procurement.ReceivingOrders.md#DocumentCurrency) | [General.Currencies](General.Currencies.md) | The currency of the unit prices and amounts in the document. [Required] [Filter(multi eq)] |
| [PaymentAccount](Logistics.Procurement.ReceivingOrders.md#PaymentAccount) | [Finance.Payments.PaymentAccounts](Finance.Payments.PaymentAccounts.md) (nullable) | Payment account that is used for the payments of this delivery. [Filter(multi eq)] |
| [PaymentType](Logistics.Procurement.ReceivingOrders.md#PaymentType) | [Finance.Payments.PaymentTypes](Finance.Payments.PaymentTypes.md) (nullable) | When not null specifies the payment type for the sales order. [Filter(multi eq)] |
| [PurchaseOrder](Logistics.Procurement.ReceivingOrders.md#PurchaseOrder) | [Logistics.Procurement.PurchaseOrders](Logistics.Procurement.PurchaseOrders.md) (nullable) | The purchase order which is received with this receiving order. [Filter(multi eq)] |
| [PurchasePriceList](Logistics.Procurement.ReceivingOrders.md#PurchasePriceList) | [Logistics.Procurement.PurchasePriceLists](Logistics.Procurement.PurchasePriceLists.md) (nullable) | The price list, which, when non-null, is used to automatically load unit prices of the products, when entering the invoice manually. [Filter(multi eq)] |
| [Store](Logistics.Procurement.ReceivingOrders.md#Store) | [Logistics.Inventory.Stores](Logistics.Inventory.Stores.md) (nullable) | The store in which the goods were received. [Filter(multi eq)] |
| [Supplier](Logistics.Procurement.ReceivingOrders.md#Supplier) | [Logistics.Procurement.Suppliers](Logistics.Procurement.Suppliers.md) | The supplier of the products for this receiving order. [Required] [Filter(multi eq)] |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| DocumentAmounts | [General.DocumentAmounts](General.DocumentAmounts.md) | List of [DocumentAmount](General.DocumentAmounts.md) child objects, based on the [DocumentAmount.Document](General.DocumentAmounts.md#Document) back reference 
| Comments | [General.DocumentComments](General.DocumentComments.md) | List of [DocumentComment](General.DocumentComments.md) child objects, based on the [DocumentComment.Document](General.DocumentComments.md#Document) back reference 
| DistributedAmounts | [General.DocumentDistributedAmounts](General.DocumentDistributedAmounts.md) | List of [DocumentDistributedAmount](General.DocumentDistributedAmounts.md) child objects, based on the [DocumentDistributedAmount.Document](General.DocumentDistributedAmounts.md#Document) back reference 
| FileAttachments | [General.DocumentFileAttachments](General.DocumentFileAttachments.md) | List of [DocumentFileAttachment](General.DocumentFileAttachments.md) child objects, based on the [DocumentFileAttachment.Document](General.DocumentFileAttachments.md#Document) back reference 
| LineAmounts | [General.DocumentLineAmounts](General.DocumentLineAmounts.md) | List of [DocumentLineAmount](General.DocumentLineAmounts.md) child objects, based on the [DocumentLineAmount.Document](General.DocumentLineAmounts.md#Document) back reference 
| Prints | [General.DocumentPrints](General.DocumentPrints.md) | List of [DocumentPrint](General.DocumentPrints.md) child objects, based on the [DocumentPrint.Document](General.DocumentPrints.md#Document) back reference 
| StateChanges | [General.DocumentStateChanges](General.DocumentStateChanges.md) | List of [DocumentStateChange](General.DocumentStateChanges.md) child objects, based on the [DocumentStateChange.Document](General.DocumentStateChanges.md#Document) back reference 
| Versions | [General.DocumentVersions](General.DocumentVersions.md) | List of [DocumentVersion](General.Documents.md#DocumentVersion) child objects, based on the [DocumentVersion.Document](General.DocumentVersions.md#Document) back reference 
| Lines | [Logistics.Procurement.ReceivingOrderLines](Logistics.Procurement.ReceivingOrderLines.md) | List of [ReceivingOrderLine](Logistics.Procurement.ReceivingOrderLines.md) child objects, based on the [Logistics.Procurement.ReceivingOrderLine.ReceivingOrder](Logistics.Procurement.ReceivingOrderLines.md#ReceivingOrder) back reference 


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### CompleteTime

> Exact time, when the document was last completed[Filter(ge;le)]

_Type_: **datetime (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### CreationTime

> Date/Time when the document was created [Required][Filter(ge;le)]

_Type_: **datetime**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **CurrentDateTime**  

### CreationUser

> The login name of the user, who created the document [Required][Filter(like)]

_Type_: **string**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### DocumentDate

> The date on which the document was issued [Required][Filter(eq;ge;le)][ORD]

_Type_: **datetime**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **True**  
_Default Value_: **CurrentDate**  

### DocumentNo

> Document number, unique within Document_Type_Id [Required][Filter(eq;like)][ORD]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  

### DocumentVersion

> [Filter(eq;ge;le)]

_Type_: **int32**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **1**  

### DocumentNotes

> Notes for this Document

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ParentDocumentRelationshipType

> Type of relationship between the current document and the parent document(s). Affects the constraints for execution/completion for the documents. Possible values: 'S' = 'Subtask', 'N' = 'Next task'.

_Type_: **[General.ParentDocumentRelationshipType](Logistics.Procurement.ReceivingOrders.md#ParentDocumentRelationshipType) (nullable)**  
Relationship between parent and child documents  
_Allowed Values (Enum Members)_  

| Value | Description |
| ---- | --- |
| Subtask | The child document is a sub-task of the parent document. (Complete child to complete parent) <br /> _Database Value:_ 'S' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Subtask' |
| NextTask | The child document is next task of the parent document. (Complete parent to complete child) <br /> _Database Value:_ 'N' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'NextTask' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### PlanningOnly

> Indicates that the document is used only for planning (and as consequence its state cannot be greater than Planned) [Required]

_Type_: **boolean (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### ReadOnly

> True - the document is read only; false - the document is not read only [Required]

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### ReferenceDate

> The date to which this document refers, i.e. when the action really occurred. If null, Document_Date is taken [Filter(ge;le)]

_Type_: **datetime (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### ReferenceDocumentNo

> The number of the document (issued by the other party), which was the reason for the creation of the current document. The numebr should be unique within the party documents [Filter(eq;like)]

_Type_: **string (nullable)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### ReleaseTime

> Exact time, when the document was first released [Filter(ge;le)]

_Type_: **datetime (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### State

> 0=New;5=Corrective;10=Computer Planned;20=Human Planned;30=Released;40=Completed;50=Closed [Required][Filter(eq;ge;le)]

_Type_: **[General.DocumentState](Logistics.Procurement.ReceivingOrders.md#State)**  
Enumeration of document system states  
_Allowed Values (Enum Members)_  

| Value | Description |
| ---- | --- |
| New | New document, just created. Can be edited. (Stored as 0). <br /> _Database Value:_ 0 <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'New' |
| Adjustment | Document which adjusts other released documents. (Stored as 5). <br /> _Database Value:_ 5 <br /> _Model Value:_ 5 <br /> _Domain API Value:_ 'Adjustment' |
| Planned | Planned by the system for future releasing. (Stored as 10). <br /> _Database Value:_ 10 <br /> _Model Value:_ 10 <br /> _Domain API Value:_ 'Planned' |
| FirmPlanned | Planned by operator for future releasing. (Stored as 20). <br /> _Database Value:_ 20 <br /> _Model Value:_ 20 <br /> _Domain API Value:_ 'FirmPlanned' |
| Released | Released document. Changes can be applied only through adjustment documents. (Stored as 30). <br /> _Database Value:_ 30 <br /> _Model Value:_ 30 <br /> _Domain API Value:_ 'Released' |
| Completed | Work has completed. (Stored as 40). <br /> _Database Value:_ 40 <br /> _Model Value:_ 40 <br /> _Domain API Value:_ 'Completed' |
| Closed | The document is audited and closed. Adjustments are not allowed, but reopening is allowed. (Stored as 50). <br /> _Database Value:_ 50 <br /> _Model Value:_ 50 <br /> _Domain API Value:_ 'Closed' |

_Supported Filters_: **Equals, GreaterThanOrLessThan, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### Void

> True if the document is null and void [Required][Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### VoidReason

> Reason for voiding the document, entered by the user

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### VoidTime

> Date/time when the document has become void

_Type_: **datetime (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### VoidUser

> The user who voided the document

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### EntityName

> The entity name of the document equal to the entity name of the document type.[Filter(eq)] [ORD]

_Type_: **string**  
_Supported Filters_: **Equals**  
_Supports Order By_: **True**  

### InvoiceDocumentNo

> Contains the purchase invoice number when it is known in advance, null otherwise. [Filter(eq)]

_Type_: **string (nullable)**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

### IsReleased

> True if the document is not void and its state is released or greater. [Required] [Default(false)] [Filter(eq)] [ReadOnly]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### IsSingleExecution

> Specifies whether the document is a single execution of its order document. [Required] [Default(false)] [Filter(eq)] [ReadOnly]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### Notes

> Notes for this ReceivingOrder.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### PaymentDueDate

> Due date for the payment. When null, the payment due date is the documents date. [Filter(ge;le)]

_Type_: **datetime (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`obj.DocumentDate.AddDays(Convert(obj.Supplier.DefaultPaymentTermDays, Double))`

_Front-End Recalc Expressions:_  
`obj.DocumentDate.AddDays(Convert(obj.Supplier.DefaultPaymentTermDays, Double))`
### PlannedDeliveryDate

> When not null, specifies the planned delivery date for all lines. [Filter(ge;le)]

_Type_: **datetime (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`obj.DocumentDate.AddDays(Convert(obj.Supplier.DefaultDeliveryTermDays, Double))`

_Front-End Recalc Expressions:_  
`obj.DocumentDate.AddDays(Convert(obj.Supplier.DefaultDeliveryTermDays, Double))`
### PlannedReleaseDate

> The date, when the document is planned to be realeased. [Filter(ge;le)]

_Type_: **datetime (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### PurchaseLotDescription

> Description of the purchase lot for the whole document. It is set for the lots created by this receiving order.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### AccessKey

> The access key, containing the user permissions for this document. null means that all users have unlimited permissions

_Type_: **[Systems.Security.AccessKeys](Systems.Security.AccessKeys.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### AdjustedDocument

> The primary document, which the current document adjusts. null when this is not an adjustment document

_Type_: **[General.Documents](General.Documents.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### AssignedToUser

> The user to which this document is assigned for handling. null means that the document is not assigned to specific user

_Type_: **[Systems.Security.Users](Systems.Security.Users.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### CurrencyDirectory

> The currency directory, containing all the convertion rates, used by the document. null means that the document does not need currency convertions

_Type_: **[General.CurrencyDirectories](General.CurrencyDirectories.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### DocumentType

> The user defined type of the document. Determines document behaviour, properties, additional amounts, validation, generations, etc. [Required]

_Type_: **[General.DocumentTypes](General.DocumentTypes.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### EnterpriseCompany

> The enterprise company which issued the document [Required]

_Type_: **[General.EnterpriseCompanies](General.EnterpriseCompanies.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### EnterpriseCompanyLocation

> The enterprise company location which issued the document. null means that there is only one location within the enterprise company and locations are not used

_Type_: **[General.Contacts.CompanyLocations](General.Contacts.CompanyLocations.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### FromCompanyDivision

> The division of the company, issuing the document. null when the document is not issued by any specific division

_Type_: **[General.Contacts.CompanyDivisions](General.Contacts.CompanyDivisions.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### FromParty

> The party which issued the document [Required]

_Type_: **[General.Contacts.Parties](General.Contacts.Parties.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### MasterDocument

> In a multi-document tree, this is the root document, that created the whole tree. If this is the root it is equal to Id [Required]

_Type_: **[General.Documents](General.Documents.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Parent

> In a multi-document tree, this is the direct parent document. If this is the root it is null

_Type_: **[General.Documents](General.Documents.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### PrimeCauseDocument

> The document that is the prime cause for creation of the current document

_Type_: **[General.Documents](General.Documents.md) (nullable)**  
_Supported Filters_: **EqualsIn**  
_Supports Order By_: **False**  

### ResponsiblePerson

> The person that is responsible for this order or transaction. It could be the sales person, the orderer, etc.

_Type_: **[General.Contacts.Persons](General.Contacts.Persons.md) (nullable)**  
_Supported Filters_: **EqualsIn**  
_Supports Order By_: **False**  

### ReverseOfDocument

> The document which the current document is reverse of

_Type_: **[General.Documents](General.Documents.md) (nullable)**  
_Supported Filters_: **EqualsIn**  
_Supports Order By_: **False**  

### Sequence

> The sequence that will be used to give new numbers to the documents of this type

_Type_: **[General.Sequences](General.Sequences.md) (nullable)**  
_Supported Filters_: **EqualsIn**  
_Supports Order By_: **False**  

### ToCompanyDivision

> The division of the company, receiving the document. null when the document is not received by any specific division

_Type_: **[General.Contacts.CompanyDivisions](General.Contacts.CompanyDivisions.md)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  

### ToParty

> The party which should receive the document

_Type_: **[General.Contacts.Parties](General.Contacts.Parties.md) (nullable)**  
_Supported Filters_: **EqualsIn**  
_Supports Order By_: **False**  

### UserStatus

> The user status of this document if applicable for this document type. null means unknown or not yet set

_Type_: **[General.DocumentTypeUserStatuses](General.DocumentTypeUserStatuses.md) (nullable)**  
_Supported Filters_: **EqualsIn**  
_Supports Order By_: **False**  

### DocumentCurrency

> The currency of the unit prices and amounts in the document. [Required] [Filter(multi eq)]

_Type_: **[General.Currencies](General.Currencies.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`obj.Supplier.DefaultCurrency.IfNullThen(obj.EnterpriseCompany.BaseCurrency).IfNullThen(obj.DocumentCurrency)`

_Front-End Recalc Expressions:_  
`obj.Supplier.DefaultCurrency.IfNullThen(obj.EnterpriseCompany.BaseCurrency).IfNullThen(obj.DocumentCurrency)`
### PaymentAccount

> Payment account that is used for the payments of this delivery. [Filter(multi eq)]

_Type_: **[Finance.Payments.PaymentAccounts](Finance.Payments.PaymentAccounts.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`obj.Supplier.DefaultPaymentAccount.IfNullThen(obj.PaymentType.GetDefaultPaymentAccount())`

_Front-End Recalc Expressions:_  
`obj.Supplier.DefaultPaymentAccount.IfNullThen(obj.PaymentType.GetDefaultPaymentAccount())`
### PaymentType

> When not null specifies the payment type for the sales order. [Filter(multi eq)]

_Type_: **[Finance.Payments.PaymentTypes](Finance.Payments.PaymentTypes.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`obj.Supplier.DefaultPaymentType`
### PurchaseOrder

> The purchase order which is received with this receiving order. [Filter(multi eq)]

_Type_: **[Logistics.Procurement.PurchaseOrders](Logistics.Procurement.PurchaseOrders.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### PurchasePriceList

> The price list, which, when non-null, is used to automatically load unit prices of the products, when entering the invoice manually. [Filter(multi eq)]

_Type_: **[Logistics.Procurement.PurchasePriceLists](Logistics.Procurement.PurchasePriceLists.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Store

> The store in which the goods were received. [Filter(multi eq)]

_Type_: **[Logistics.Inventory.Stores](Logistics.Inventory.Stores.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`obj.Lines.Select(c => c.LineStore).Distinct().OnlyIfSingle()`
### Supplier

> The supplier of the products for this receiving order. [Required] [Filter(multi eq)]

_Type_: **[Logistics.Procurement.Suppliers](Logistics.Procurement.Suppliers.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Logistics.Procurement.ReceivingOrders erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Logistics.Procurement.ReceivingOrders erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Logistics.Procurement.ReceivingOrders erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_Procurement_ReceivingOrders?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_Procurement_ReceivingOrders?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Scm_Receiving_Orders?$top=10>

