# Finance.Payments.PaymentOrders

Each payment order contains a receivable or payable amount. Entity: Cash_Payment_Orders

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Finance.Payments.PaymentOrders.md#Id) | guid |  
| [CompleteTime](Finance.Payments.PaymentOrders.md#CompleteTime) | datetime (nullable) | Exact time, when the document was last completed[Filter(ge;le)] 
| [CreationTime](Finance.Payments.PaymentOrders.md#CreationTime) | datetime | Date/Time when the document was created [Required][Filter(ge;le)] 
| [CreationUser](Finance.Payments.PaymentOrders.md#CreationUser) | string | The login name of the user, who created the document [Required][Filter(like)] 
| [DocumentDate](Finance.Payments.PaymentOrders.md#DocumentDate) | datetime | The date on which the document was issued [Required][Filter(eq;ge;le)][ORD] 
| [DocumentNo](Finance.Payments.PaymentOrders.md#DocumentNo) | string | Document number, unique within Document_Type_Id [Required][Filter(eq;like)][ORD] 
| [DocumentVersion](Finance.Payments.PaymentOrders.md#DocumentVersion) | int32 | [Filter(eq;ge;le)] 
| [DocumentNotes](Finance.Payments.PaymentOrders.md#DocumentNotes) | string (nullable) | Notes for this Document 
| [ParentDocumentRelationshipType](Finance.Payments.PaymentOrders.md#ParentDocumentRelationshipType) | [General.ParentDocumentRelationshipType](Finance.Payments.PaymentOrders.md#ParentDocumentRelationshipType) (nullable) | Type of relationship between the current document and the parent document(s). Affects the constraints for execution/completion for the documents. Possible values: 'S' = 'Subtask', 'N' = 'Next task'. 
| [PlanningOnly](Finance.Payments.PaymentOrders.md#PlanningOnly) | boolean (nullable) | Indicates that the document is used only for planning (and as consequence its state cannot be greater than Planned) [Required] 
| [ReadOnly](Finance.Payments.PaymentOrders.md#ReadOnly) | boolean | True - the document is read only; false - the document is not read only [Required] 
| [ReferenceDate](Finance.Payments.PaymentOrders.md#ReferenceDate) | datetime (nullable) | The date to which this document refers, i.e. when the action really occurred. If null, Document_Date is taken [Filter(ge;le)] 
| [ReferenceDocumentNo](Finance.Payments.PaymentOrders.md#ReferenceDocumentNo) | string (nullable) | The number of the document (issued by the other party), which was the reason for the creation of the current document. The numebr should be unique within the party documents [Filter(eq;like)] 
| [ReleaseTime](Finance.Payments.PaymentOrders.md#ReleaseTime) | datetime (nullable) | Exact time, when the document was first released [Filter(ge;le)] 
| [State](Finance.Payments.PaymentOrders.md#State) | [General.DocumentState](Finance.Payments.PaymentOrders.md#State) | 0=New;5=Corrective;10=Computer Planned;20=Human Planned;30=Released;40=Completed;50=Closed [Required][Filter(eq;ge;le)] 
| [Void](Finance.Payments.PaymentOrders.md#Void) | boolean | True if the document is null and void [Required][Filter(eq)] 
| [VoidReason](Finance.Payments.PaymentOrders.md#VoidReason) | string (nullable) | Reason for voiding the document, entered by the user 
| [VoidTime](Finance.Payments.PaymentOrders.md#VoidTime) | datetime (nullable) | Date/time when the document has become void 
| [VoidUser](Finance.Payments.PaymentOrders.md#VoidUser) | string (nullable) | The user who voided the document 
| [EntityName](Finance.Payments.PaymentOrders.md#EntityName) | string | The entity name of the document equal to the entity name of the document type.[Filter(eq)] [ORD] 
| [AllowCloseNotPaid](Finance.Payments.PaymentOrders.md#AllowCloseNotPaid) | boolean | True to allow closing of payment orders, that are not fully paid. [Required] [Default(false)] [Filter(eq)] 
| [BillTo](Finance.Payments.PaymentOrders.md#BillTo) | [Finance.Payments.PaymentOrdersRepository.BillTo](Finance.Payments.PaymentOrders.md#BillTo) (nullable) | If filled indicates which party is billed for the total amount. Possible values: 'C' = Company (means the Party_Id), 'L' = Company location (the Location_Party_Id), null = unidentified. [Filter(eq)] 
| [Direction](Finance.Payments.PaymentOrders.md#Direction) | [Finance.Payments.PaymentOrdersRepository.Direction](Finance.Payments.PaymentOrders.md#Direction) | I for Payment issue, R for payment receipt. [Required] [Default("I")] [Filter(eq)] 
| [DueDate](Finance.Payments.PaymentOrders.md#DueDate) | datetime (nullable) | The due date of the payment. null means there is no due date. [Filter(eq;ge;le)] 
| [DueStartDate](Finance.Payments.PaymentOrders.md#DueStartDate) | date (nullable) | The date at which the payment becomes executable. null means the payment is executable at all times. [Filter(eq;ge;le)] [ORD] 
| [InstallmentNumber](Finance.Payments.PaymentOrders.md#InstallmentNumber) | int32 (nullable) | Consequtive installment number. Used for identifying the payment when using payment plans. null means that the payment is not part of a payment plan. [Filter(eq)] 
| [InvoiceAmount](Finance.Payments.PaymentOrders.md#InvoiceAmount) | [Amount](../data-types/Amount.md) (nullable) | The invoice amount that is specified in this payment order. (the invoice amount converted to the Total_Amount_Currency_Id must be equal to the Total_Amount). [Currency: InvoiceAmountCurrency] 
| [IsAmountWithVAT](Finance.Payments.PaymentOrders.md#IsAmountWithVAT) | boolean | Is_Amount_With_VAT=true if the requested amount includes VAT. [Required] [Default(true)] [Filter(eq)] 
| [IsReleased](Finance.Payments.PaymentOrders.md#IsReleased) | boolean | True if the document is not void and its state is released or greater. [Required] [Default(false)] [Filter(eq)] [ReadOnly] 
| [IsSingleExecution](Finance.Payments.PaymentOrders.md#IsSingleExecution) | boolean | Specifies whether the document is a single execution of its order document. [Required] [Default(false)] [Filter(eq)] [ReadOnly] 
| [Notes](Finance.Payments.PaymentOrders.md#Notes) | string (nullable) | Notes for this PaymentOrder. 
| [RefDocumentDate](Finance.Payments.PaymentOrders.md#RefDocumentDate) | datetime (nullable) | The date of the original document. null means that it is unknown. [Filter(eq)] 
| [RefDocumentNo](Finance.Payments.PaymentOrders.md#RefDocumentNo) | string | The number of the document which has created the payment order and is the basis for the payment. [Required] [Filter(eq)] 
| [RefInvoiceApplyDate](Finance.Payments.PaymentOrders.md#RefInvoiceApplyDate) | datetime (nullable) | The apply date of the related invoice. Not specified when the payment order isn't related to any invoice or the apply date is unknown. [Filter(eq;ge;le)] 
| [RefInvoiceDocumentDate](Finance.Payments.PaymentOrders.md#RefInvoiceDocumentDate) | datetime (nullable) | The date of the related invoice. null means that the payment order isn't related to any invoice or the date is unknown. [Filter(eq;ge;le)] 
| [RefInvoiceDocumentNo](Finance.Payments.PaymentOrders.md#RefInvoiceDocumentNo) | string (nullable) | The number of the invoice which has created or is related to the payment order and is the basis for the payment. null means that the payment order isn't created or related to any invoice. [Filter(eq)] 
| [TotalAmount](Finance.Payments.PaymentOrders.md#TotalAmount) | [Amount](../data-types/Amount.md) | Total amount that should be payed. [Currency: TotalAmountCurrency] [Required] [Default(0)] [Filter(eq;ge;le)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [AccessKey](Finance.Payments.PaymentOrders.md#AccessKey) | [Systems.Security.AccessKeys](Systems.Security.AccessKeys.md) (nullable) | The access key, containing the user permissions for this document. null means that all users have unlimited permissions |
| [AdjustedDocument](Finance.Payments.PaymentOrders.md#AdjustedDocument) | [General.Documents](General.Documents.md) (nullable) | The primary document, which the current document adjusts. null when this is not an adjustment document |
| [AssignedToUser](Finance.Payments.PaymentOrders.md#AssignedToUser) | [Systems.Security.Users](Systems.Security.Users.md) (nullable) | The user to which this document is assigned for handling. null means that the document is not assigned to specific user |
| [CurrencyDirectory](Finance.Payments.PaymentOrders.md#CurrencyDirectory) | [General.CurrencyDirectories](General.CurrencyDirectories.md) (nullable) | The currency directory, containing all the convertion rates, used by the document. null means that the document does not need currency convertions |
| [DocumentType](Finance.Payments.PaymentOrders.md#DocumentType) | [General.DocumentTypes](General.DocumentTypes.md) | The user defined type of the document. Determines document behaviour, properties, additional amounts, validation, generations, etc. [Required] |
| [EnterpriseCompany](Finance.Payments.PaymentOrders.md#EnterpriseCompany) | [General.EnterpriseCompanies](General.EnterpriseCompanies.md) | The enterprise company which issued the document [Required] |
| [EnterpriseCompanyLocation](Finance.Payments.PaymentOrders.md#EnterpriseCompanyLocation) | [General.Contacts.CompanyLocations](General.Contacts.CompanyLocations.md) (nullable) | The enterprise company location which issued the document. null means that there is only one location within the enterprise company and locations are not used |
| [FromCompanyDivision](Finance.Payments.PaymentOrders.md#FromCompanyDivision) | [General.Contacts.CompanyDivisions](General.Contacts.CompanyDivisions.md) (nullable) | The division of the company, issuing the document. null when the document is not issued by any specific division |
| [FromParty](Finance.Payments.PaymentOrders.md#FromParty) | [General.Contacts.Parties](General.Contacts.Parties.md) | The party which issued the document [Required] |
| [MasterDocument](Finance.Payments.PaymentOrders.md#MasterDocument) | [General.Documents](General.Documents.md) | In a multi-document tree, this is the root document, that created the whole tree. If this is the root it is equal to Id [Required] |
| [Parent](Finance.Payments.PaymentOrders.md#Parent) | [General.Documents](General.Documents.md) (nullable) | In a multi-document tree, this is the direct parent document. If this is the root it is null |
| [PrimeCauseDocument](Finance.Payments.PaymentOrders.md#PrimeCauseDocument) | [General.Documents](General.Documents.md) (nullable) | The document that is the prime cause for creation of the current document |
| [ResponsiblePerson](Finance.Payments.PaymentOrders.md#ResponsiblePerson) | [General.Contacts.Persons](General.Contacts.Persons.md) (nullable) | The person that is responsible for this order or transaction. It could be the sales person, the orderer, etc. |
| [ReverseOfDocument](Finance.Payments.PaymentOrders.md#ReverseOfDocument) | [General.Documents](General.Documents.md) (nullable) | The document which the current document is reverse of |
| [Sequence](Finance.Payments.PaymentOrders.md#Sequence) | [General.Sequences](General.Sequences.md) (nullable) | The sequence that will be used to give new numbers to the documents of this type |
| [ToCompanyDivision](Finance.Payments.PaymentOrders.md#ToCompanyDivision) | [General.Contacts.CompanyDivisions](General.Contacts.CompanyDivisions.md) | The division of the company, receiving the document. null when the document is not received by any specific division |
| [ToParty](Finance.Payments.PaymentOrders.md#ToParty) | [General.Contacts.Parties](General.Contacts.Parties.md) (nullable) | The party which should receive the document |
| [UserStatus](Finance.Payments.PaymentOrders.md#UserStatus) | [General.DocumentTypeUserStatuses](General.DocumentTypeUserStatuses.md) (nullable) | The user status of this document if applicable for this document type. null means unknown or not yet set |
| [FiscalPrinterPosDevice](Finance.Payments.PaymentOrders.md#FiscalPrinterPosDevice) | [Crm.Pos.Devices](Crm.Pos.Devices.md) (nullable) | When not null, contains suggested fiscal printer for printing fiscal notes upon payment. [Filter(multi eq)] (Introduced in version 19.1.100.0) |
| [InvoiceAmountCurrency](Finance.Payments.PaymentOrders.md#InvoiceAmountCurrency) | [General.Currencies](General.Currencies.md) (nullable) | The currency of Invoice Amount. [Filter(multi eq)] |
| [LocationParty](Finance.Payments.PaymentOrders.md#LocationParty) | [General.Contacts.Parties](General.Contacts.Parties.md) (nullable) | Location or sub-party of the Party_Id in the order. [Filter(multi eq)] |
| [Party](Finance.Payments.PaymentOrders.md#Party) | [General.Contacts.Parties](General.Contacts.Parties.md) | The party which is to pay or receive the amount. [Required] [Filter(multi eq)] |
| [PaymentAccount](Finance.Payments.PaymentOrders.md#PaymentAccount) | [Finance.Payments.PaymentAccounts](Finance.Payments.PaymentAccounts.md) (nullable) | When not null, specifies the payment account that is expected or will be used by the payment transaction. [Filter(multi eq)] |
| [PaymentType](Finance.Payments.PaymentOrders.md#PaymentType) | [Finance.Payments.PaymentTypes](Finance.Payments.PaymentTypes.md) (nullable) | Expected payment type. Null when there is no expectation. Can also specify default payment account. [Filter(multi eq)] |
| [RefDocument](Finance.Payments.PaymentOrders.md#RefDocument) | [General.Documents](General.Documents.md) (nullable) | The document which has created the payment order and is the basis for the payment. If this column is filled then Ref_Document_Type_Id, Ref_Document_No and Ref_Document_Date must be equal to the type, number and date of the specified document. [Filter(multi eq)] |
| [RefDocumentType](Finance.Payments.PaymentOrders.md#RefDocumentType) | [General.DocumentTypes](General.DocumentTypes.md) | The type of the document which has created the payment order and is the basis for the payment. [Required] [Filter(multi eq)] |
| [RefInvoiceDocument](Finance.Payments.PaymentOrders.md#RefInvoiceDocument) | [General.Documents](General.Documents.md) (nullable) | The invoice document which has created or is related to the payment order and is the basis for the payment. null means that the payment order isn't created or related to any invoice or the invoice isn't present in the database. If this column is filled then Ref_Invoice_Document_Type_Id, Ref_Invoice_Document_No and Ref_Invoice_Document_Date must be equal to the type, number and date of the specified invoice document. [Filter(multi eq)] |
| [RefInvoiceDocumentType](Finance.Payments.PaymentOrders.md#RefInvoiceDocumentType) | [General.DocumentTypes](General.DocumentTypes.md) (nullable) | The document type of the invoice which has created or is related to the payment order and is the basis for the payment. null means that the payment order isn't created or related to any invoice. [Filter(multi eq)] |
| [TotalAmountCurrency](Finance.Payments.PaymentOrders.md#TotalAmountCurrency) | [General.Currencies](General.Currencies.md) | The currency of Total Amount. [Required] [Filter(multi eq)] |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| DocumentAmounts | [General.DocumentAmounts](General.DocumentAmounts.md) |  
| Comments | [General.DocumentComments](General.DocumentComments.md) | List of [DocumentComment](General.DocumentComments.md) child objects, based on the [DocumentComment.Document](General.DocumentComments.md#Document) back reference 
| DistributedAmounts | [General.DocumentDistributedAmounts](General.DocumentDistributedAmounts.md) | List of [DocumentDistributedAmount](General.DocumentDistributedAmounts.md) child objects, based on the [DocumentDistributedAmount.Document](General.DocumentDistributedAmounts.md#Document) back reference 
| FileAttachments | [General.DocumentFileAttachments](General.DocumentFileAttachments.md) | List of [DocumentFileAttachment](General.DocumentFileAttachments.md) child objects, based on the [DocumentFileAttachment.Document](General.DocumentFileAttachments.md#Document) back reference 
| LineAmounts | [General.DocumentLineAmounts](General.DocumentLineAmounts.md) | List of [DocumentLineAmount](General.DocumentLineAmounts.md) child objects, based on the [DocumentLineAmount.Document](General.DocumentLineAmounts.md#Document) back reference 
| Prints | [General.DocumentPrints](General.DocumentPrints.md) | List of [DocumentPrint](General.DocumentPrints.md) child objects, based on the [DocumentPrint.Document](General.DocumentPrints.md#Document) back reference 
| StateChanges | [General.DocumentStateChanges](General.DocumentStateChanges.md) | List of [DocumentStateChange](General.DocumentStateChanges.md) child objects, based on the [DocumentStateChange.Document](General.DocumentStateChanges.md#Document) back reference 
| Versions | [General.DocumentVersions](General.DocumentVersions.md) | List of [DocumentVersion](General.Documents.md#DocumentVersion) child objects, based on the [DocumentVersion.Document](General.DocumentVersions.md#Document) back reference 


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

_Type_: **[General.ParentDocumentRelationshipType](Finance.Payments.PaymentOrders.md#ParentDocumentRelationshipType) (nullable)**  
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

_Type_: **[General.DocumentState](Finance.Payments.PaymentOrders.md#State)**  
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

### AllowCloseNotPaid

> True to allow closing of payment orders, that are not fully paid. [Required] [Default(false)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### BillTo

> If filled indicates which party is billed for the total amount. Possible values: 'C' = Company (means the Party_Id), 'L' = Company location (the Location_Party_Id), null = unidentified. [Filter(eq)]

_Type_: **[Finance.Payments.PaymentOrdersRepository.BillTo](Finance.Payments.PaymentOrders.md#BillTo) (nullable)**  
Allowed values for the [BillTo](Finance.Payments.PaymentOrders.md#BillTo) data attribute  
_Allowed Values (Enum Members)_  

| Value | Description |
| ---- | --- |
| Company | Company value. Stored as 'C'. <br /> _Database Value:_ 'C' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Company' |
| CompanyLocation | CompanyLocation value. Stored as 'L'. <br /> _Database Value:_ 'L' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'CompanyLocation' |

_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

### Direction

> I for Payment issue, R for payment receipt. [Required] [Default("I")] [Filter(eq)]

_Type_: **[Finance.Payments.PaymentOrdersRepository.Direction](Finance.Payments.PaymentOrders.md#Direction)**  
Allowed values for the [Direction](Finance.Payments.PaymentOrders.md#Direction) data attribute  
_Allowed Values (Enum Members)_  

| Value | Description |
| ---- | --- |
| Expense | Expense value. Stored as 'I'. <br /> _Database Value:_ 'I' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Expense' |
| Income | Income value. Stored as 'R'. <br /> _Database Value:_ 'R' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'Income' |

_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **Expense**  

### DueDate

> The due date of the payment. null means there is no due date. [Filter(eq;ge;le)]

_Type_: **datetime (nullable)**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### DueStartDate

> The date at which the payment becomes executable. null means the payment is executable at all times. [Filter(eq;ge;le)] [ORD]

_Type_: **date (nullable)**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **True**  

### InstallmentNumber

> Consequtive installment number. Used for identifying the payment when using payment plans. null means that the payment is not part of a payment plan. [Filter(eq)]

_Type_: **int32 (nullable)**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

### InvoiceAmount

> The invoice amount that is specified in this payment order. (the invoice amount converted to the Total_Amount_Currency_Id must be equal to the Total_Amount). [Currency: InvoiceAmountCurrency]

_Type_: **[Amount](../data-types/Amount.md) (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### IsAmountWithVAT

> Is_Amount_With_VAT=true if the requested amount includes VAT. [Required] [Default(true)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **True**  

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

> Notes for this PaymentOrder.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### RefDocumentDate

> The date of the original document. null means that it is unknown. [Filter(eq)]

_Type_: **datetime (nullable)**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`obj.RefDocument.DocumentDate`

_Front-End Recalc Expressions:_  
`obj.RefDocument.DocumentDate`
### RefDocumentNo

> The number of the document which has created the payment order and is the basis for the payment. [Required] [Filter(eq)]

_Type_: **string**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`obj.RefDocument.DocumentNo`

_Front-End Recalc Expressions:_  
`obj.RefDocument.DocumentNo`
### RefInvoiceApplyDate

> The apply date of the related invoice. Not specified when the payment order isn't related to any invoice or the apply date is unknown. [Filter(eq;ge;le)]

_Type_: **datetime (nullable)**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`Convert(obj.RefInvoiceDocument, IInvoiceDocument).ApplyDate`

_Front-End Recalc Expressions:_  
`Convert(obj.RefInvoiceDocument, IInvoiceDocument).ApplyDate`
### RefInvoiceDocumentDate

> The date of the related invoice. null means that the payment order isn't related to any invoice or the date is unknown. [Filter(eq;ge;le)]

_Type_: **datetime (nullable)**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`obj.RefInvoiceDocument.DocumentDate`

_Front-End Recalc Expressions:_  
`obj.RefInvoiceDocument.DocumentDate`
### RefInvoiceDocumentNo

> The number of the invoice which has created or is related to the payment order and is the basis for the payment. null means that the payment order isn't created or related to any invoice. [Filter(eq)]

_Type_: **string (nullable)**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`obj.RefInvoiceDocument.DocumentNo`

_Front-End Recalc Expressions:_  
`obj.RefInvoiceDocument.DocumentNo`
### TotalAmount

> Total amount that should be payed. [Currency: TotalAmountCurrency] [Required] [Default(0)] [Filter(eq;ge;le)]

_Type_: **[Amount](../data-types/Amount.md)**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  


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

### FiscalPrinterPosDevice

> When not null, contains suggested fiscal printer for printing fiscal notes upon payment. [Filter(multi eq)] (Introduced in version 19.1.100.0)

_Type_: **[Crm.Pos.Devices](Crm.Pos.Devices.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### InvoiceAmountCurrency

> The currency of Invoice Amount. [Filter(multi eq)]

_Type_: **[General.Currencies](General.Currencies.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### LocationParty

> Location or sub-party of the Party_Id in the order. [Filter(multi eq)]

_Type_: **[General.Contacts.Parties](General.Contacts.Parties.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Party

> The party which is to pay or receive the amount. [Required] [Filter(multi eq)]

_Type_: **[General.Contacts.Parties](General.Contacts.Parties.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`obj.LocationParty.ParentParty`

### PaymentAccount

> When not null, specifies the payment account that is expected or will be used by the payment transaction. [Filter(multi eq)]

_Type_: **[Finance.Payments.PaymentAccounts](Finance.Payments.PaymentAccounts.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`obj.PaymentType.GetDefaultPaymentAccount().IfNullThen(obj.PaymentAccount)`
### PaymentType

> Expected payment type. Null when there is no expectation. Can also specify default payment account. [Filter(multi eq)]

_Type_: **[Finance.Payments.PaymentTypes](Finance.Payments.PaymentTypes.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### RefDocument

> The document which has created the payment order and is the basis for the payment. If this column is filled then Ref_Document_Type_Id, Ref_Document_No and Ref_Document_Date must be equal to the type, number and date of the specified document. [Filter(multi eq)]

_Type_: **[General.Documents](General.Documents.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### RefDocumentType

> The type of the document which has created the payment order and is the basis for the payment. [Required] [Filter(multi eq)]

_Type_: **[General.DocumentTypes](General.DocumentTypes.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`obj.RefDocument.DocumentType`

_Front-End Recalc Expressions:_  
`obj.RefDocument.DocumentType`
### RefInvoiceDocument

> The invoice document which has created or is related to the payment order and is the basis for the payment. null means that the payment order isn't created or related to any invoice or the invoice isn't present in the database. If this column is filled then Ref_Invoice_Document_Type_Id, Ref_Invoice_Document_No and Ref_Invoice_Document_Date must be equal to the type, number and date of the specified invoice document. [Filter(multi eq)]

_Type_: **[General.Documents](General.Documents.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### RefInvoiceDocumentType

> The document type of the invoice which has created or is related to the payment order and is the basis for the payment. null means that the payment order isn't created or related to any invoice. [Filter(multi eq)]

_Type_: **[General.DocumentTypes](General.DocumentTypes.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`obj.RefInvoiceDocument.DocumentType`

_Front-End Recalc Expressions:_  
`obj.RefInvoiceDocument.DocumentType`
### TotalAmountCurrency

> The currency of Total Amount. [Required] [Filter(multi eq)]

_Type_: **[General.Currencies](General.Currencies.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`obj.PaymentAccount.Currency`



## Business Rules

[!list erp.entity=Finance.Payments.PaymentOrders erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Finance.Payments.PaymentOrders erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Finance.Payments.PaymentOrders erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Payments_PaymentOrders?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Payments_PaymentOrders?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Cash_Payment_Orders?$top=10>

