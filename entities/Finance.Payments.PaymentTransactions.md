---
uid: Finance.Payments.PaymentTransactions
---
# Finance.Payments.PaymentTransactions Entity

Represents actual payments, which increase or decrease the balance of a payment account. Entity: Cash_Payment_Transactions

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [CompleteTime](Finance.Payments.PaymentTransactions.md#completetime) | datetime (nullable) | Exact time, when the document was last completed[Filter(ge;le)] 
| [CreationTime](Finance.Payments.PaymentTransactions.md#creationtime) | datetime | Date/Time when the document was created [Required][Filter(ge;le)] 
| [CreationUser](Finance.Payments.PaymentTransactions.md#creationuser) | string | The login name of the user, who created the document [Required][Filter(like)] 
| [Direction](Finance.Payments.PaymentTransactions.md#direction) | [Direction](Finance.Payments.PaymentTransactions.md#direction) | I for Payment issue, R for payment receipt. [Required] [Default("R")] [Filter(eq)] 
| [DocumentDate](Finance.Payments.PaymentTransactions.md#documentdate) | datetime | The date on which the document was issued [Required][Filter(eq;ge;le)][ORD] 
| [DocumentNo](Finance.Payments.PaymentTransactions.md#documentno) | string | Document number, unique within Document_Type_Id [Required][Filter(eq;like)][ORD] 
| [DocumentNotes](Finance.Payments.PaymentTransactions.md#documentnotes) | string (nullable) | Notes for this Document 
| [DocumentVersion](Finance.Payments.PaymentTransactions.md#documentversion) | int32 | [Filter(eq;ge;le)] 
| [EntityName](Finance.Payments.PaymentTransactions.md#entityname) | string | The entity name of the document equal to the entity name of the document type.[Filter(eq)] [ORD] 
| [Id](Finance.Payments.PaymentTransactions.md#id) | guid |  
| [IsReleased](Finance.Payments.PaymentTransactions.md#isreleased) | boolean | True if the document is not void and its state is released or greater. [Required] [Default(false)] [Filter(eq)] [ReadOnly] 
| [IsSingleExecution](Finance.Payments.PaymentTransactions.md#issingleexecution) | boolean | Specifies whether the document is a single execution of its order document. [Required] [Default(false)] [Filter(eq)] [ReadOnly] 
| [Notes](Finance.Payments.PaymentTransactions.md#notes) | string (nullable) | Notes for this PaymentTransaction. 
| [ParentDocument<br />RelationshipType](Finance.Payments.PaymentTransactions.md#parentdocumentrelationshiptype) | [ParentDocument<br />RelationshipType](Finance.Payments.PaymentTransactions.md#parentdocumentrelationshiptype) (nullable) | Type of relationship between the current document and the parent document(s). Affects the constraints for execution/completion for the documents. Possible values: 'S' = 'Subtask', 'N' = 'Next task'. 
| [PaymentSlipNo](Finance.Payments.PaymentTransactions.md#paymentslipno) | string (nullable) | The number of the payment slip. Can be used to directly indicate the number without referring to Payment_Slips. [Filter(eq)] 
| [PlanningOnly](Finance.Payments.PaymentTransactions.md#planningonly) | boolean (nullable) | Indicates that the document is used only for planning (and as consequence its state cannot be greater than Planned) [Required] 
| [ReadOnly](Finance.Payments.PaymentTransactions.md#readonly) | boolean | True - the document is read only; false - the document is not read only [Required] 
| [ReferenceDate](Finance.Payments.PaymentTransactions.md#referencedate) | datetime (nullable) | The date to which this document refers, i.e. when the action really occurred. If null, Document_Date is taken [Filter(ge;le)] 
| [ReferenceDocumentNo](Finance.Payments.PaymentTransactions.md#referencedocumentno) | string (nullable) | The number of the document (issued by the other party), which was the reason for the creation of the current document. The numebr should be unique within the party documents [Filter(eq;like)] 
| [ReleaseTime](Finance.Payments.PaymentTransactions.md#releasetime) | datetime (nullable) | Exact time, when the document was first released [Filter(ge;le)] 
| [RequiresAllocation](Finance.Payments.PaymentTransactions.md#requiresallocation) | boolean | True=The total amount should be allocated to payment orders; false=Payment orders are not required. [Required] [Default(true)] [Filter(eq)] 
| [ReversalReason](Finance.Payments.PaymentTransactions.md#reversalreason) | [ReversalReason](Finance.Payments.PaymentTransactions.md#reversalreason) (nullable) | The reason for the reversal of the payment. [Introduced in version 20.1] 
| [State](Finance.Payments.PaymentTransactions.md#state) | [DocumentState](Finance.Payments.PaymentTransactions.md#state) | 0=New;5=Corrective;10=Computer Planned;20=Human Planned;30=Released;40=Completed;50=Closed [Required][Filter(eq;ge;le)] 
| [TotalAmount](Finance.Payments.PaymentTransactions.md#totalamount) | [Amount](../data-types.md#amount) | The total amount payed. The distribution of the amount among source orders is specified with payment transacion lines. [Currency: TotalAmountCurrency] [Required] [Default(0)] 
| [Void](Finance.Payments.PaymentTransactions.md#void) | boolean | True if the document is null and void [Required][Filter(eq)] 
| [VoidReason](Finance.Payments.PaymentTransactions.md#voidreason) | string (nullable) | Reason for voiding the document, entered by the user 
| [VoidTime](Finance.Payments.PaymentTransactions.md#voidtime) | datetime (nullable) | Date/time when the document has become void 
| [VoidUser](Finance.Payments.PaymentTransactions.md#voiduser) | string (nullable) | The user who voided the document 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [AccessKey](Finance.Payments.PaymentTransactions.md#accesskey) | [AccessKeys](Systems.Security.AccessKeys.md) (nullable) | The access key, containing the user permissions for this document. null means that all users have unlimited permissions |
| [AdjustedDocument](Finance.Payments.PaymentTransactions.md#adjusteddocument) | [Documents](General.Documents.md) (nullable) | The primary document, which the current document adjusts. null when this is not an adjustment document |
| [AssignedToUser](Finance.Payments.PaymentTransactions.md#assignedtouser) | [Users](Systems.Security.Users.md) (nullable) | The user to which this document is assigned for handling. null means that the document is not assigned to specific user |
| [CurrencyDirectory](Finance.Payments.PaymentTransactions.md#currencydirectory) | [CurrencyDirectories](General.CurrencyDirectories.md) (nullable) | The currency directory, containing all the convertion rates, used by the document. null means that the document does not need currency convertions |
| [DocumentType](Finance.Payments.PaymentTransactions.md#documenttype) | [DocumentTypes](General.DocumentTypes.md) | The user defined type of the document. Determines document behaviour, properties, additional amounts, validation, generations, etc. [Required] |
| [EnterpriseCompany](Finance.Payments.PaymentTransactions.md#enterprisecompany) | [EnterpriseCompanies](General.EnterpriseCompanies.md) | The enterprise company which issued the document [Required] |
| [EnterpriseCompanyLocation](Finance.Payments.PaymentTransactions.md#enterprisecompanylocation) | [CompanyLocations](General.Contacts.CompanyLocations.md) (nullable) | The enterprise company location which issued the document. null means that there is only one location within the enterprise company and locations are not used |
| [FiscalPrinterPosDevice](Finance.Payments.PaymentTransactions.md#fiscalprinterposdevice) | [Devices](Crm.Pos.Devices.md) (nullable) | For POS Sales Order payments. Specifies the POS Device from fiscal printer type on which the receipt is printed. Null when the payment transaction is not created for a POS Sale Order. [Filter(multi eq)] [Introduced in version 19.1] |
| [FromCompanyDivision](Finance.Payments.PaymentTransactions.md#fromcompanydivision) | [CompanyDivisions](General.Contacts.CompanyDivisions.md) (nullable) | The division of the company, issuing the document. null when the document is not issued by any specific division |
| [FromParty](Finance.Payments.PaymentTransactions.md#fromparty) | [Parties](General.Contacts.Parties.md) | The party which issued the document [Required] |
| [MasterDocument](Finance.Payments.PaymentTransactions.md#masterdocument) | [Documents](General.Documents.md) | In a multi-document tree, this is the root document, that created the whole tree. If this is the root it is equal to Id [Required] |
| [OriginalPaymentTransaction](Finance.Payments.PaymentTransactions.md#originalpaymenttransaction) | [PaymentTransactions](Finance.Payments.PaymentTransactions.md) (nullable) | Original Payment Transaction. [Filter(multi eq)] [Introduced in version 20.1] |
| [Parent](Finance.Payments.PaymentTransactions.md#parent) | [Documents](General.Documents.md) (nullable) | In a multi-document tree, this is the direct parent document. If this is the root it is null |
| [ParentPaymentSlipAmount](Finance.Payments.PaymentTransactions.md#parentpaymentslipamount) | [PaymentSlipAmounts](Finance.Payments.PaymentSlipAmounts.md) (nullable) | The Payment Slip Amount, which the current payment transaction fulfills . null when the current document does not execute any Payment Slip Amount. [Filter(multi eq)] [Introduced in version 19.1] |
| [Party](Finance.Payments.PaymentTransactions.md#party) | [Parties](General.Contacts.Parties.md) | The party that is paying or receiving the money. [Required] [Filter(multi eq)] |
| [PaymentAccount](Finance.Payments.PaymentTransactions.md#paymentaccount) | [PaymentAccounts](Finance.Payments.PaymentAccounts.md) (nullable) | The account towards which the payment was effected. [Filter(multi eq)] |
| [PaymentReason](Finance.Payments.PaymentTransactions.md#paymentreason) | [PaymentReasons](Finance.Payments.PaymentReasons.md) (nullable) | The payment reason, as defined in Payment Reasons. [Filter(multi eq)] |
| [PaymentSlip](Finance.Payments.PaymentTransactions.md#paymentslip) | [PaymentSlips](Finance.Payments.PaymentSlips.md) (nullable) | When not null specifies that this payment was part of a payment slip. [Filter(multi eq)] |
| [PaymentType](Finance.Payments.PaymentTransactions.md#paymenttype) | [PaymentTypes](Finance.Payments.PaymentTypes.md) (nullable) | Specifies the payment type used to pay, when using this payment account. null when the payment type is unknown or unspecified. [Filter(multi eq)] |
| [PosLocation](Finance.Payments.PaymentTransactions.md#poslocation) | [Locations](Crm.Pos.Locations.md) (nullable) | For POS Sales Order payments. Specifies the POS Location, in which the payment is performed. Null when the payment transaction is not created for a POS Sale Order. [Filter(multi eq)] [Introduced in version 19.1] |
| [PosOperator](Finance.Payments.PaymentTransactions.md#posoperator) | [Operators](Crm.Pos.Operators.md) (nullable) | For POS Sales Order payments. Specifies the POS Operator, who created the payment order. Null when the payment transaction is not created for a POS Sale Order. [Filter(multi eq)] [Introduced in version 19.1] |
| [PrimeCauseDocument](Finance.Payments.PaymentTransactions.md#primecausedocument) | [Documents](General.Documents.md) (nullable) | The document that is the prime cause for creation of the current document |
| [ResponsiblePerson](Finance.Payments.PaymentTransactions.md#responsibleperson) | [Persons](General.Contacts.Persons.md) (nullable) | The person that is responsible for this order or transaction. It could be the sales person, the orderer, etc. |
| [ReverseOfDocument](Finance.Payments.PaymentTransactions.md#reverseofdocument) | [Documents](General.Documents.md) (nullable) | The document which the current document is reverse of |
| [Sequence](Finance.Payments.PaymentTransactions.md#sequence) | [Sequences](General.Sequences.md) (nullable) | The sequence that will be used to give new numbers to the documents of this type |
| [ToCompanyDivision](Finance.Payments.PaymentTransactions.md#tocompanydivision) | [CompanyDivisions](General.Contacts.CompanyDivisions.md) | The division of the company, receiving the document. null when the document is not received by any specific division |
| [ToParty](Finance.Payments.PaymentTransactions.md#toparty) | [Parties](General.Contacts.Parties.md) (nullable) | The party which should receive the document |
| [TotalAmountCurrency](Finance.Payments.PaymentTransactions.md#totalamountcurrency) | [Currencies](General.Currencies.md) | The currency of the total amount. [Required] [Filter(multi eq)] |
| [UserStatus](Finance.Payments.PaymentTransactions.md#userstatus) | [DocumentTypeUserStatuses](General.DocumentTypeUserStatuses.md) (nullable) | The user status of this document if applicable for this document type. null means unknown or not yet set |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Comments | [DocumentComments](General.DocumentComments.md) | List of [DocumentComment](General.DocumentComments.md) child objects, based on the [DocumentComment.Document](General.DocumentComments.md#document) back reference 
| DistributedAmounts | [DocumentDistributedAmounts](General.DocumentDistributedAmounts.md) | List of [DocumentDistributed<br />Amount](General.DocumentDistributedAmounts.md) child objects, based on the [DocumentDistributedAmount.Document](General.DocumentDistributedAmounts.md#document) back reference 
| DocumentAmounts | [DocumentAmounts](General.DocumentAmounts.md) |  
| FileAttachments | [DocumentFileAttachments](General.DocumentFileAttachments.md) | List of [DocumentFileAttachment](General.DocumentFileAttachments.md) child objects, based on the [DocumentFileAttachment.Document](General.DocumentFileAttachments.md#document) back reference 
| LineAmounts | [DocumentLineAmounts](General.DocumentLineAmounts.md) | List of [DocumentLineAmount](General.DocumentLineAmounts.md) child objects, based on the [DocumentLineAmount.Document](General.DocumentLineAmounts.md#document) back reference 
| Lines | [PaymentTransactionLines](Finance.Payments.PaymentTransactionLines.md) | List of [PaymentTransactionLine](Finance.Payments.PaymentTransactionLines.md) child objects, based on the [Finance.Payments.PaymentTransactionLine.PaymentTransaction](Finance.Payments.PaymentTransactionLines.md#paymenttransaction) back reference 
| Prints | [DocumentPrints](General.DocumentPrints.md) | List of [DocumentPrint](General.DocumentPrints.md) child objects, based on the [DocumentPrint.Document](General.DocumentPrints.md#document) back reference 
| StateChanges | [DocumentStateChanges](General.DocumentStateChanges.md) | List of [DocumentStateChange](General.DocumentStateChanges.md) child objects, based on the [DocumentStateChange.Document](General.DocumentStateChanges.md#document) back reference 
| Versions | [DocumentVersions](General.DocumentVersions.md) | List of [DocumentVersion](General.Documents.md#documentversion) child objects, based on the [DocumentVersion.Document](General.DocumentVersions.md#document) back reference 


## Attribute Details

### CompleteTime

Exact time, when the document was last completed[Filter(ge;le)]

_Type_: **datetime (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### CreationTime

Date/Time when the document was created [Required][Filter(ge;le)]

_Type_: **datetime**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **CurrentDateTime**  

### CreationUser

The login name of the user, who created the document [Required][Filter(like)]

_Type_: **string**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### Direction

I for Payment issue, R for payment receipt. [Required] [Default("R")] [Filter(eq)]

_Type_: **[Direction](Finance.Payments.PaymentTransactions.md#direction)**  
Allowed values for the [Direction](Finance.Payments.PaymentOrders.md#direction) data attribute  
_Allowed Values (Finance.Payments.PaymentOrdersRepository.Direction Enum Members)_  

| Value | Description |
| ---- | --- |
| Expense | Expense value. Stored as 'I'. <br /> _Database Value:_ 'I' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Expense' |
| Income | Income value. Stored as 'R'. <br /> _Database Value:_ 'R' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'Income' |

_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **Income**  

### DocumentDate

The date on which the document was issued [Required][Filter(eq;ge;le)][ORD]

_Type_: **datetime**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **True**  
_Default Value_: **CurrentDate**  

### DocumentNo

Document number, unique within Document_Type_Id [Required][Filter(eq;like)][ORD]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  

### DocumentNotes

Notes for this Document

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### DocumentVersion

[Filter(eq;ge;le)]

_Type_: **int32**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **1**  

### EntityName

The entity name of the document equal to the entity name of the document type.[Filter(eq)] [ORD]

_Type_: **string**  
_Supported Filters_: **Equals**  
_Supports Order By_: **True**  

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### IsReleased

True if the document is not void and its state is released or greater. [Required] [Default(false)] [Filter(eq)] [ReadOnly]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### IsSingleExecution

Specifies whether the document is a single execution of its order document. [Required] [Default(false)] [Filter(eq)] [ReadOnly]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### Notes

Notes for this PaymentTransaction.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ParentDocumentRelationshipType

Type of relationship between the current document and the parent document(s). Affects the constraints for execution/completion for the documents. Possible values: 'S' = 'Subtask', 'N' = 'Next task'.

_Type_: **[ParentDocument<br />RelationshipType](Finance.Payments.PaymentTransactions.md#parentdocumentrelationshiptype) (nullable)**  
Relationship between parent and child documents  
_Allowed Values (General.ParentDocumentRelationshipType Enum Members)_  

| Value | Description |
| ---- | --- |
| Subtask | The child document is a sub-task of the parent document. (Complete child to complete parent) <br /> _Database Value:_ 'S' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Subtask' |
| NextTask | The child document is next task of the parent document. (Complete parent to complete child) <br /> _Database Value:_ 'N' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'NextTask' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### PaymentSlipNo

The number of the payment slip. Can be used to directly indicate the number without referring to Payment_Slips. [Filter(eq)]

_Type_: **string (nullable)**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

### PlanningOnly

Indicates that the document is used only for planning (and as consequence its state cannot be greater than Planned) [Required]

_Type_: **boolean (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### ReadOnly

True - the document is read only; false - the document is not read only [Required]

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### ReferenceDate

The date to which this document refers, i.e. when the action really occurred. If null, Document_Date is taken [Filter(ge;le)]

_Type_: **datetime (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### ReferenceDocumentNo

The number of the document (issued by the other party), which was the reason for the creation of the current document. The numebr should be unique within the party documents [Filter(eq;like)]

_Type_: **string (nullable)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### ReleaseTime

Exact time, when the document was first released [Filter(ge;le)]

_Type_: **datetime (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### RequiresAllocation

True=The total amount should be allocated to payment orders; false=Payment orders are not required. [Required] [Default(true)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### ReversalReason

The reason for the reversal of the payment. [Introduced in version 20.1]

_Type_: **[ReversalReason](Finance.Payments.PaymentTransactions.md#reversalreason) (nullable)**  
Allowed values for the [ReversalReason](Finance.Payments.PaymentTransactions.md#reversalreason) data attribute  
_Allowed Values (Finance.Payments.PaymentTransactionsRepository.ReversalReason Enum Members)_  

| Value | Description |
| ---- | --- |
| OperatorError | OperatorError value. Stored as 'OPE'. <br /> _Database Value:_ 'OPE' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'OperatorError' |
| TaxBaseReduction | TaxBaseReduction value. Stored as 'TBR'. <br /> _Database Value:_ 'TBR' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'TaxBaseReduction' |
| Refund | Refund value. Stored as 'REF'. <br /> _Database Value:_ 'REF' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'Refund' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### State

0=New;5=Corrective;10=Computer Planned;20=Human Planned;30=Released;40=Completed;50=Closed [Required][Filter(eq;ge;le)]

_Type_: **[DocumentState](Finance.Payments.PaymentTransactions.md#state)**  
Enumeration of document system states  
_Allowed Values (General.DocumentState Enum Members)_  

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

### TotalAmount

The total amount payed. The distribution of the amount among source orders is specified with payment transacion lines. [Currency: TotalAmountCurrency] [Required] [Default(0)]

_Type_: **[Amount](../data-types.md#amount)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

_Front-End Recalc Expressions:_  
`obj.CalculateTotalAmountFromLines( obj.Direction)`
### Void

True if the document is null and void [Required][Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### VoidReason

Reason for voiding the document, entered by the user

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### VoidTime

Date/time when the document has become void

_Type_: **datetime (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### VoidUser

The user who voided the document

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### AccessKey

The access key, containing the user permissions for this document. null means that all users have unlimited permissions

_Type_: **[AccessKeys](Systems.Security.AccessKeys.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### AdjustedDocument

The primary document, which the current document adjusts. null when this is not an adjustment document

_Type_: **[Documents](General.Documents.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### AssignedToUser

The user to which this document is assigned for handling. null means that the document is not assigned to specific user

_Type_: **[Users](Systems.Security.Users.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### CurrencyDirectory

The currency directory, containing all the convertion rates, used by the document. null means that the document does not need currency convertions

_Type_: **[CurrencyDirectories](General.CurrencyDirectories.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### DocumentType

The user defined type of the document. Determines document behaviour, properties, additional amounts, validation, generations, etc. [Required]

_Type_: **[DocumentTypes](General.DocumentTypes.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### EnterpriseCompany

The enterprise company which issued the document [Required]

_Type_: **[EnterpriseCompanies](General.EnterpriseCompanies.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### EnterpriseCompanyLocation

The enterprise company location which issued the document. null means that there is only one location within the enterprise company and locations are not used

_Type_: **[CompanyLocations](General.Contacts.CompanyLocations.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### FiscalPrinterPosDevice

For POS Sales Order payments. Specifies the POS Device from fiscal printer type on which the receipt is printed. Null when the payment transaction is not created for a POS Sale Order. [Filter(multi eq)] [Introduced in version 19.1]

_Type_: **[Devices](Crm.Pos.Devices.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

_Back-End Default Expression:_  
`IIF( ( ( ( obj.PosOperator != null) AndAlso ( obj.PosOperator.DefaultPosTerminal != null)) AndAlso ( obj.PosOperator.DefaultPosTerminal.DefaultFiscalPrinterPosDevice != null)), obj.PosOperator.DefaultPosTerminal.DefaultFiscalPrinterPosDevice, obj.Transaction.Query( ).FirstOrDefault( d => ( ( ( Convert( d.DeviceType, Int32) == 2) AndAlso ( d.PosTerminal == obj.PosOperator.DefaultPosTerminal)) AndAlso d.IsActive)))`

_Front-End Recalc Expressions:_  
`IIF( ( ( ( obj.PosOperator != null) AndAlso ( obj.PosOperator.DefaultPosTerminal != null)) AndAlso ( obj.PosOperator.DefaultPosTerminal.DefaultFiscalPrinterPosDevice != null)), obj.PosOperator.DefaultPosTerminal.DefaultFiscalPrinterPosDevice, obj.Transaction.Query( ).FirstOrDefault( d => ( ( ( Convert( d.DeviceType, Int32) == 2) AndAlso ( d.PosTerminal == obj.PosOperator.DefaultPosTerminal)) AndAlso d.IsActive)))`
### FromCompanyDivision

The division of the company, issuing the document. null when the document is not issued by any specific division

_Type_: **[CompanyDivisions](General.Contacts.CompanyDivisions.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### FromParty

The party which issued the document [Required]

_Type_: **[Parties](General.Contacts.Parties.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### MasterDocument

In a multi-document tree, this is the root document, that created the whole tree. If this is the root it is equal to Id [Required]

_Type_: **[Documents](General.Documents.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### OriginalPaymentTransaction

Original Payment Transaction. [Filter(multi eq)] [Introduced in version 20.1]

_Type_: **[PaymentTransactions](Finance.Payments.PaymentTransactions.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### Parent

In a multi-document tree, this is the direct parent document. If this is the root it is null

_Type_: **[Documents](General.Documents.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### ParentPaymentSlipAmount

The Payment Slip Amount, which the current payment transaction fulfills . null when the current document does not execute any Payment Slip Amount. [Filter(multi eq)] [Introduced in version 19.1]

_Type_: **[PaymentSlipAmounts](Finance.Payments.PaymentSlipAmounts.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### Party

The party that is paying or receiving the money. [Required] [Filter(multi eq)]

_Type_: **[Parties](General.Contacts.Parties.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### PaymentAccount

The account towards which the payment was effected. [Filter(multi eq)]

_Type_: **[PaymentAccounts](Finance.Payments.PaymentAccounts.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

_Front-End Recalc Expressions:_  
`obj.PaymentType.GetDefaultPaymentAccount( ).IfNullThen( obj.PaymentAccount)`
### PaymentReason

The payment reason, as defined in Payment Reasons. [Filter(multi eq)]

_Type_: **[PaymentReasons](Finance.Payments.PaymentReasons.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### PaymentSlip

When not null specifies that this payment was part of a payment slip. [Filter(multi eq)]

_Type_: **[PaymentSlips](Finance.Payments.PaymentSlips.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### PaymentType

Specifies the payment type used to pay, when using this payment account. null when the payment type is unknown or unspecified. [Filter(multi eq)]

_Type_: **[PaymentTypes](Finance.Payments.PaymentTypes.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### PosLocation

For POS Sales Order payments. Specifies the POS Location, in which the payment is performed. Null when the payment transaction is not created for a POS Sale Order. [Filter(multi eq)] [Introduced in version 19.1]

_Type_: **[Locations](Crm.Pos.Locations.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

_Back-End Default Expression:_  
`obj.Transaction.Query( ).OnlyIfSingle( l => ( ( l.EnterpriseCompanyLocation == obj.EnterpriseCompanyLocation) AndAlso l.IsActive))`

_Front-End Recalc Expressions:_  
`obj.Transaction.Query( ).OnlyIfSingle( l => ( ( l.EnterpriseCompanyLocation == obj.EnterpriseCompanyLocation) AndAlso l.IsActive))`
### PosOperator

For POS Sales Order payments. Specifies the POS Operator, who created the payment order. Null when the payment transaction is not created for a POS Sale Order. [Filter(multi eq)] [Introduced in version 19.1]

_Type_: **[Operators](Crm.Pos.Operators.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

_Back-End Default Expression:_  
`obj.Transaction.Query( ).OnlyIfSingle( op => ( ( ( ( ( op.PosLocation == obj.PosLocation) AndAlso ( op.User == obj.Transaction.CurrentUser)) AndAlso op.IsActive) AndAlso ( op.StartingDate <= DateTime.Today)) AndAlso Convert( op.TerminationDate, Object).GreaterEqualNull( Convert( DateTime.Today, Object))))`

_Front-End Recalc Expressions:_  
`obj.Transaction.Query( ).OnlyIfSingle( op => ( ( ( ( ( op.PosLocation == obj.PosLocation) AndAlso ( op.User == obj.Transaction.CurrentUser)) AndAlso op.IsActive) AndAlso ( op.StartingDate <= DateTime.Today)) AndAlso Convert( op.TerminationDate, Object).GreaterEqualNull( Convert( DateTime.Today, Object))))`
### PrimeCauseDocument

The document that is the prime cause for creation of the current document

_Type_: **[Documents](General.Documents.md) (nullable)**  
_Supported Filters_: **EqualsIn**  

### ResponsiblePerson

The person that is responsible for this order or transaction. It could be the sales person, the orderer, etc.

_Type_: **[Persons](General.Contacts.Persons.md) (nullable)**  
_Supported Filters_: **EqualsIn**  

### ReverseOfDocument

The document which the current document is reverse of

_Type_: **[Documents](General.Documents.md) (nullable)**  
_Supported Filters_: **EqualsIn**  

### Sequence

The sequence that will be used to give new numbers to the documents of this type

_Type_: **[Sequences](General.Sequences.md) (nullable)**  
_Supported Filters_: **EqualsIn**  

### ToCompanyDivision

The division of the company, receiving the document. null when the document is not received by any specific division

_Type_: **[CompanyDivisions](General.Contacts.CompanyDivisions.md)**  
_Supported Filters_: **NotFilterable**  

### ToParty

The party which should receive the document

_Type_: **[Parties](General.Contacts.Parties.md) (nullable)**  
_Supported Filters_: **EqualsIn**  

### TotalAmountCurrency

The currency of the total amount. [Required] [Filter(multi eq)]

_Type_: **[Currencies](General.Currencies.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### UserStatus

The user status of this document if applicable for this document type. null means unknown or not yet set

_Type_: **[DocumentTypeUserStatuses](General.DocumentTypeUserStatuses.md) (nullable)**  
_Supported Filters_: **EqualsIn**  


## API Methods

These are methods that can be invoked in public APIs.

### GetAllParentDocuments

_Return Type_: **Collection Of [Documents](General.Documents.md)**  
_Declaring Type_: **[Documents](General.Documents.md)**  
_Domain API Request_: **GET**  
Gets all parent documents, traversing the parent document chain by using the [Parent](General.Documents.md#parent) property.

**Parameters**  
  * **includeSelf**  
    _Type_: boolean  
     _Optional_: True  
    _Default Value_: False  
    if set to true the current document is included.

### ChangeState

_Return Type_: **void**  
_Declaring Type_: **[Documents](General.Documents.md)**  
_Domain API Request_: **POST**  
Changes the document state to the specified new state

**Parameters**  
  * **newState**  
    _Type_: General.DocumentState  
    The desired new state of the document
  * **userStatus**  
    _Type_: [DocumentTypeUserStatuses](General.DocumentTypeUserStatuses.md)  
     _Optional_: True  
    _Default Value_: null  
    The desired new user status of the document. Can be null.

### Complete

_Return Type_: **void**  
_Declaring Type_: **[Documents](General.Documents.md)**  
_Domain API Request_: **POST**  
Changes the document state to Completed with all Release-ed sub-documents

**Parameters**  
  * **completion**  
    _Type_: General.DocumentCompletion  
    How the sub-documents will be completed, if at all

### MakeVoid

_Return Type_: **void**  
_Declaring Type_: **[Documents](General.Documents.md)**  
_Domain API Request_: **POST**  
Makes the document void. The operation is irreversible.

**Parameters**  
  * **reason**  
    _Type_: string  
    The reason for voiding the document.
  * **voidType**  
    _Type_: General.DocumentsRepositoryBase.VoidType  
     _Optional_: True  
    _Default Value_: VoidDocument  
    The type of void operation to execute.

### GetPrintout

_Return Type_: **string**  
_Declaring Type_: **[Documents](General.Documents.md)**  
_Domain API Request_: **POST**  
Gets a document printout as a file. The returned value is Base64 string representation of the file contents.

**Parameters**  
  * **fileFormat**  
    _Type_: string  
     _Optional_: True  
    _Default Value_: pdf  
    The file format: pdf, html, xlsx, xls, docx, txt and png. The default format is 'pdf'.
  * **printout**  
    _Type_: [Printouts](General.Printouts.md)  
     _Optional_: True  
    _Default Value_: null  
    The printout defined for the document type of the document. If null the default printout of the document type is used.

### Recalculate

_Return Type_: **void**  
_Declaring Type_: **[Documents](General.Documents.md)**  
_Domain API Request_: **POST**  
The document and all of its owned objects will be altered to become valid.



## Business Rules

[!list erp.entity=Finance.Payments.PaymentTransactions erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Finance.Payments.PaymentTransactions erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Finance.Payments.PaymentTransactions erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Payments_PaymentTransactions?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Payments_PaymentTransactions?$top=10>

