---
uid: Finance.Vat.Entries
---
# Finance.Vat.Entries Entity

Contains the entries in the VAT sales and purchase ledgers. Entity: VAT_Entries

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [AdjustmentNumber](Finance.Vat.Entries.md#adjustmentnumber) | int32 | Consecutive number of the correction that this document is applying to the adjusted document. [Required] [Default(0)] [ReadOnly] 
| [AdjustmentTime](Finance.Vat.Entries.md#adjustmenttime) | datetime (nullable) | Date/time when the document last has been adjusted by corrective document. [ReadOnly] 
| [AdjustmentUser](Finance.Vat.Entries.md#adjustmentuser) | string (nullable) | The user who adjusted the document. [ReadOnly] 
| [AmountBase](Finance.Vat.Entries.md#amountbase) | [Amount](../data-types.md#amount) | Amount of the operation without the tax in base currency. [Currency: EnterpriseCompany.BaseCurrency] [Required] 
| [ApplyDate](Finance.Vat.Entries.md#applydate) | date | Specifies the date on which the entry should be applied in the reporting. Usually equal to the document date with exception for documents that are late to be applied in the correct period. [Required] [Filter(ge;le)] 
| [CashReportingMode](Finance.Vat.Entries.md#cashreportingmode) | boolean | When true, specifies, that the special cash reporting mode should be used for VAT reporting. When false, the normal (classic) VAT reporting is used. [Required] [Default(false)] 
| [CompleteTime](Finance.Vat.Entries.md#completetime) | datetime (nullable) | Date and time when the document was completed (State set to Completed). [Filter(ge;le)] [ReadOnly] 
| [CreationTime](Finance.Vat.Entries.md#creationtime) | datetime | Date/Time when the document was created. [Required] [Default(Now)] [Filter(ge;le)] [ReadOnly] 
| [CreationUser](Finance.Vat.Entries.md#creationuser) | string | The login name of the user, who created the document. [Required] [Filter(like)] [ReadOnly] 
| [DocumentDate](Finance.Vat.Entries.md#documentdate) | date | The date on which the document was issued. [Required] [Default(Today)] [Filter(eq;ge;le)] [ORD] 
| [DocumentNo](Finance.Vat.Entries.md#documentno) | string | Document number, unique within Document_Type_Id. [Required] [Filter(eq;like)] [ORD] 
| [DocumentNotes](Finance.Vat.Entries.md#documentnotes) | string (nullable) | Notes for this Document. 
| [DocumentVersion](Finance.Vat.Entries.md#documentversion) | int32 | Consecutive version number, starting with 1. Each update produces a new version of the document. [Required] [Default(1)] [Filter(eq;ge;le)] [ReadOnly] 
| [EntityName](Finance.Vat.Entries.md#entityname) | string | The entity name of the document header. [Required] [Filter(eq)] [ORD] [ReadOnly] 
| [EntryType](Finance.Vat.Entries.md#entrytype) | [EntryType](Finance.Vat.Entries.md#entrytype) | Type of the VAT entry. S=Sales, P=Purchases. [Required] [Filter(eq)] [ORD] 
| [Id](Finance.Vat.Entries.md#id) | guid |  
| [IsReleased](Finance.Vat.Entries.md#isreleased) | boolean | True if the document is not void and its state is released or greater. [Required] [Default(false)] [Filter(eq)] [ReadOnly] 
| [IsSingleExecution](Finance.Vat.Entries.md#issingleexecution) | boolean | Specifies whether the document is a single execution of its order document. [Required] [Default(false)] [Filter(eq)] [ReadOnly] 
| [ParentDocument<br />RelationshipType](Finance.Vat.Entries.md#parentdocumentrelationshiptype) | [ParentDocument<br />RelationshipType](Finance.Vat.Entries.md#parentdocumentrelationshiptype) (nullable) | Type of relationship between the current document and the parent document(s). Affects the constraints for execution/completion for the documents. Possible values: 'S' = 'Subtask', 'N' = 'Next task'. [ReadOnly] 
| [PlanningOnly](Finance.Vat.Entries.md#planningonly) | boolean | Indicates that the document is used only for planning (and as consequence its state cannot be greater than Planned). [Required] [Default(false)] [ReadOnly] 
| [ReadOnly](Finance.Vat.Entries.md#readonly) | boolean | True - the document is read only; false - the document is not read only. [Required] [Default(false)] [ReadOnly] 
| [ReferenceDate](Finance.Vat.Entries.md#referencedate) | datetime (nullable) | The date to which this document refers, i.e. when the action really occurred. If null, Document_Date is taken. [Default(Today)] [Filter(ge;le)] 
| [ReferencedDocumentNo](Finance.Vat.Entries.md#referenceddocumentno) | string | Number of the document that represents the operation that caused this entry. [Required] [Filter(eq)] 
| [ReferenceDocumentNo](Finance.Vat.Entries.md#referencedocumentno) | string (nullable) | The number of the document (issued by the other party), which was the reason for the creation of the current document. The numebr should be unique within the party documents. [Filter(eq;like)] 
| [RegistrationNumber](Finance.Vat.Entries.md#registrationnumber) | string (nullable) | Identification code (IC) for the party specified by Party_Id. 
| [RegistrationVATNumber](Finance.Vat.Entries.md#registrationvatnumber) | string | VAT number by registration (or national number) for the party specified by Party_Id. [Required] [Filter(eq)] 
| [ReleaseTime](Finance.Vat.Entries.md#releasetime) | datetime (nullable) | Date and time when the document was released (State set to Released). [Filter(ge;le)] [ReadOnly] 
| [State](Finance.Vat.Entries.md#state) | [DocumentState](Finance.Vat.Entries.md#state) | The current system state of the document. Allowed values: 0=New;5=Corrective;10=Computer Planned;20=Human Planned;30=Released;40=Completed;50=Closed. [Required] [Default(0)] [Filter(multi eq;ge;le)] [ReadOnly] 
| [VATAmountBase](Finance.Vat.Entries.md#vatamountbase) | [Amount](../data-types.md#amount) | The amount of the tax for the operation in base currency. [Currency: EnterpriseCompany.BaseCurrency] [Required] 
| [Void](Finance.Vat.Entries.md#void) | boolean | True if the document is null and void. [Required] [Default(false)] [Filter(eq)] [ReadOnly] 
| [VoidReason](Finance.Vat.Entries.md#voidreason) | string (nullable) | Reason for voiding the document, entered by the user. [ReadOnly] 
| [VoidTime](Finance.Vat.Entries.md#voidtime) | datetime (nullable) | Date/time when the document has become void. [ReadOnly] 
| [VoidUser](Finance.Vat.Entries.md#voiduser) | string (nullable) | The user who voided the document. [ReadOnly] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [AccessKey](Finance.Vat.Entries.md#accesskey) | [AccessKeys](Systems.Security.AccessKeys.md) (nullable) | The access key, containing the user permissions for this document. null means that all users have unlimited permissions. [Filter(multi eq)] |
| [AdjustedDocument](Finance.Vat.Entries.md#adjusteddocument) | [Documents](General.Documents.md) (nullable) | The primary document, which the current document adjusts. null when this is not an adjustment document. [Filter(multi eq)] [ReadOnly] |
| [AssignedToUser](Finance.Vat.Entries.md#assignedtouser) | [Users](Systems.Security.Users.md) (nullable) | The user to which this document is assigned for handling. null means that the document is not assigned to specific user. [Filter(multi eq)] |
| [CurrencyDirectory](Finance.Vat.Entries.md#currencydirectory) | [CurrencyDirectories](General.CurrencyDirectories.md) (nullable) | The currency directory, containing all the convertion rates, used by the document. null means that the document does not need currency convertions. [Filter(multi eq)] |
| [DealType](Finance.Vat.Entries.md#dealtype) | [DealTypes](Finance.Vat.DealTypes.md) | Deal type that caused this entry. [Required] [Filter(multi eq)] |
| [DocumentType](Finance.Vat.Entries.md#documenttype) | [DocumentTypes](General.DocumentTypes.md) | The user defined type of the document. Determines document behaviour, properties, additional amounts, validation, generations, etc. [Required] [Filter(multi eq)] |
| [EnterpriseCompany](Finance.Vat.Entries.md#enterprisecompany) | [EnterpriseCompanies](General.EnterpriseCompanies.md) | The enterprise company which issued the document. [Required] [Filter(multi eq)] |
| [EnterpriseCompanyLocation](Finance.Vat.Entries.md#enterprisecompanylocation) | [CompanyLocations](General.Contacts.CompanyLocations.md) (nullable) | The enterprise company location which issued the document. null means that there is only one location within the enterprise company and locations are not used. [Filter(multi eq)] |
| [FromCompanyDivision](Finance.Vat.Entries.md#fromcompanydivision) | [CompanyDivisions](General.Contacts.CompanyDivisions.md) (nullable) | The division of the company, issuing the document. null when the document is not issued by any specific division. [Filter(multi eq)] |
| [FromParty](Finance.Vat.Entries.md#fromparty) | [Parties](General.Contacts.Parties.md) | The party which issued the document. [Required] [Filter(multi eq)] |
| [MasterDocument](Finance.Vat.Entries.md#masterdocument) | [Documents](General.Documents.md) | In a multi-document tree, this is the root document, that created the whole tree. If this is the root it is equal to Id. [Required] [Filter(multi eq)] |
| [Parent](Finance.Vat.Entries.md#parent) | [Documents](General.Documents.md) (nullable) | In a multi-document tree, this is the direct parent document. If this is the root it is null. [Filter(multi eq)] |
| [Party](Finance.Vat.Entries.md#party) | [Parties](General.Contacts.Parties.md) | The corresponding party that is involved in the operation that caused this entry. [Required] [Filter(multi eq)] |
| [PrimeCauseDocument](Finance.Vat.Entries.md#primecausedocument) | [Documents](General.Documents.md) (nullable) | The document that is the prime cause for creation of the current document. [Filter(multi eq)] |
| [ReferencedDocumentType](Finance.Vat.Entries.md#referenceddocumenttype) | [DocumentTypes](General.DocumentTypes.md) | Type of the document that represents the operation that caused this entry. [Required] [Filter(multi eq)] |
| [ResponsiblePerson](Finance.Vat.Entries.md#responsibleperson) | [Persons](General.Contacts.Persons.md) (nullable) | The person that is responsible for this order or transaction. It could be the sales person, the orderer, etc. [Filter(multi eq)] |
| [ReverseOfDocument](Finance.Vat.Entries.md#reverseofdocument) | [Documents](General.Documents.md) (nullable) | The document which the current document is reverse of. [Filter(multi eq)] [ReadOnly] |
| [Sequence](Finance.Vat.Entries.md#sequence) | [Sequences](General.Sequences.md) (nullable) | The sequence that will be used to give new numbers to the documents of this type. [Filter(multi eq)] [ReadOnly] |
| [ToCompanyDivision](Finance.Vat.Entries.md#tocompanydivision) | [CompanyDivisions](General.Contacts.CompanyDivisions.md) (nullable) | The division of the company, receiving the document. null when the document is not received by any specific division. [Filter(multi eq)] |
| [ToParty](Finance.Vat.Entries.md#toparty) | [Parties](General.Contacts.Parties.md) (nullable) | The party which should receive the document. [Filter(multi eq)] |
| [UserStatus](Finance.Vat.Entries.md#userstatus) | [DocumentTypeUserStatuses](General.DocumentTypeUserStatuses.md) (nullable) | The user status of this document if applicable for this document type. null means unknown or not yet set. [Filter(multi eq)] [ReadOnly] |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Comments | [DocumentComments](General.DocumentComments.md) | List of [DocumentComment](General.DocumentComments.md) child objects, based on the [General.DocumentComment.Document](General.DocumentComments.md#document) back reference 
| DistributedAmounts | [DocumentDistributedAmounts](General.DocumentDistributedAmounts.md) | List of [DocumentDistributed<br />Amount](General.DocumentDistributedAmounts.md) child objects, based on the [General.DocumentDistributedAmount.Document](General.DocumentDistributedAmounts.md#document) back reference 
| DocumentAmounts | [DocumentAmounts](General.DocumentAmounts.md) | List of [DocumentAmount](General.DocumentAmounts.md) child objects, based on the [General.DocumentAmount.Document](General.DocumentAmounts.md#document) back reference 
| FileAttachments | [DocumentFileAttachments](General.DocumentFileAttachments.md) | List of [DocumentFileAttachment](General.DocumentFileAttachments.md) child objects, based on the [General.DocumentFileAttachment.Document](General.DocumentFileAttachments.md#document) back reference 
| LineAmounts | [DocumentLineAmounts](General.DocumentLineAmounts.md) | List of [DocumentLineAmount](General.DocumentLineAmounts.md) child objects, based on the [General.DocumentLineAmount.Document](General.DocumentLineAmounts.md#document) back reference 
| Prints | [DocumentPrints](General.DocumentPrints.md) | List of [DocumentPrint](General.DocumentPrints.md) child objects, based on the [General.DocumentPrint.Document](General.DocumentPrints.md#document) back reference 
| StateChanges | [DocumentStateChanges](General.DocumentStateChanges.md) | List of [DocumentStateChange](General.DocumentStateChanges.md) child objects, based on the [General.DocumentStateChange.Document](General.DocumentStateChanges.md#document) back reference 
| Versions | [DocumentVersions](General.DocumentVersions.md) | List of [DocumentVersion](General.DocumentVersions.md) child objects, based on the [General.DocumentVersion.Document](General.DocumentVersions.md#document) back reference 


## Attribute Details

### AdjustmentNumber

Consecutive number of the correction that this document is applying to the adjusted document. [Required] [Default(0)] [ReadOnly]

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### AdjustmentTime

Date/time when the document last has been adjusted by corrective document. [ReadOnly]

_Type_: **datetime (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### AdjustmentUser

The user who adjusted the document. [ReadOnly]

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### AmountBase

Amount of the operation without the tax in base currency. [Currency: EnterpriseCompany.BaseCurrency] [Required]

_Type_: **[Amount](../data-types.md#amount)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ApplyDate

Specifies the date on which the entry should be applied in the reporting. Usually equal to the document date with exception for documents that are late to be applied in the correct period. [Required] [Filter(ge;le)]

_Type_: **date**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`obj.DocumentDate`
### CashReportingMode

When true, specifies, that the special cash reporting mode should be used for VAT reporting. When false, the normal (classic) VAT reporting is used. [Required] [Default(false)]

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### CompleteTime

Date and time when the document was completed (State set to Completed). [Filter(ge;le)] [ReadOnly]

_Type_: **datetime (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### CreationTime

Date/Time when the document was created. [Required] [Default(Now)] [Filter(ge;le)] [ReadOnly]

_Type_: **datetime**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **CurrentDateTime**  

### CreationUser

The login name of the user, who created the document. [Required] [Filter(like)] [ReadOnly]

_Type_: **string**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### DocumentDate

The date on which the document was issued. [Required] [Default(Today)] [Filter(eq;ge;le)] [ORD]

_Type_: **date**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **True**  
_Default Value_: **CurrentDate**  

### DocumentNo

Document number, unique within Document_Type_Id. [Required] [Filter(eq;like)] [ORD]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  

### DocumentNotes

Notes for this Document.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### DocumentVersion

Consecutive version number, starting with 1. Each update produces a new version of the document. [Required] [Default(1)] [Filter(eq;ge;le)] [ReadOnly]

_Type_: **int32**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **1**  

### EntityName

The entity name of the document header. [Required] [Filter(eq)] [ORD] [ReadOnly]

_Type_: **string**  
_Supported Filters_: **Equals**  
_Supports Order By_: **True**  

### EntryType

Type of the VAT entry. S=Sales, P=Purchases. [Required] [Filter(eq)] [ORD]

_Type_: **[EntryType](Finance.Vat.Entries.md#entrytype)**  
Allowed values for the [EntryType](Finance.Vat.Entries.md#entrytype) data attribute  
_Allowed Values (Finance.Vat.EntriesRepository.EntryType Enum Members)_  

| Value | Description |
| ---- | --- |
| Purchases | Purchases value. Stored as 'P'. <br /> _Database Value:_ 'P' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Purchases' |
| Sales | Sales value. Stored as 'S'. <br /> _Database Value:_ 'S' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'Sales' |

_Supported Filters_: **Equals**  
_Supports Order By_: **True**  

_Front-End Recalc Expressions:_  
`obj.DealType.EntryType`
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

### ParentDocumentRelationshipType

Type of relationship between the current document and the parent document(s). Affects the constraints for execution/completion for the documents. Possible values: 'S' = 'Subtask', 'N' = 'Next task'. [ReadOnly]

_Type_: **[ParentDocument<br />RelationshipType](Finance.Vat.Entries.md#parentdocumentrelationshiptype) (nullable)**  
Relationship between parent and child documents  
_Allowed Values (General.ParentDocumentRelationshipType Enum Members)_  

| Value | Description |
| ---- | --- |
| Subtask | The child document is a sub-task of the parent document. (Complete child to complete parent) <br /> _Database Value:_ 'S' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Subtask' |
| NextTask | The child document is next task of the parent document. (Complete parent to complete child) <br /> _Database Value:_ 'N' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'NextTask' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### PlanningOnly

Indicates that the document is used only for planning (and as consequence its state cannot be greater than Planned). [Required] [Default(false)] [ReadOnly]

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### ReadOnly

True - the document is read only; false - the document is not read only. [Required] [Default(false)] [ReadOnly]

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### ReferenceDate

The date to which this document refers, i.e. when the action really occurred. If null, Document_Date is taken. [Default(Today)] [Filter(ge;le)]

_Type_: **datetime (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **CurrentDate**  

### ReferencedDocumentNo

Number of the document that represents the operation that caused this entry. [Required] [Filter(eq)]

_Type_: **string**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`IIF( obj.Parent.IsDocumentTypeEntityInvoice( ), obj.Parent.DocumentNo, obj.ReferencedDocumentNo)`
### ReferenceDocumentNo

The number of the document (issued by the other party), which was the reason for the creation of the current document. The numebr should be unique within the party documents. [Filter(eq;like)]

_Type_: **string (nullable)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### RegistrationNumber

Identification code (IC) for the party specified by Party_Id.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### RegistrationVATNumber

VAT number by registration (or national number) for the party specified by Party_Id. [Required] [Filter(eq)]

_Type_: **string**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`obj.Party.GetPartyCompany( ).RegistrationVATNumber`
### ReleaseTime

Date and time when the document was released (State set to Released). [Filter(ge;le)] [ReadOnly]

_Type_: **datetime (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### State

The current system state of the document. Allowed values: 0=New;5=Corrective;10=Computer Planned;20=Human Planned;30=Released;40=Completed;50=Closed. [Required] [Default(0)] [Filter(multi eq;ge;le)] [ReadOnly]

_Type_: **[DocumentState](Finance.Vat.Entries.md#state)**  
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

### VATAmountBase

The amount of the tax for the operation in base currency. [Currency: EnterpriseCompany.BaseCurrency] [Required]

_Type_: **[Amount](../data-types.md#amount)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Void

True if the document is null and void. [Required] [Default(false)] [Filter(eq)] [ReadOnly]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### VoidReason

Reason for voiding the document, entered by the user. [ReadOnly]

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### VoidTime

Date/time when the document has become void. [ReadOnly]

_Type_: **datetime (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### VoidUser

The user who voided the document. [ReadOnly]

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### AccessKey

The access key, containing the user permissions for this document. null means that all users have unlimited permissions. [Filter(multi eq)]

_Type_: **[AccessKeys](Systems.Security.AccessKeys.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### AdjustedDocument

The primary document, which the current document adjusts. null when this is not an adjustment document. [Filter(multi eq)] [ReadOnly]

_Type_: **[Documents](General.Documents.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### AssignedToUser

The user to which this document is assigned for handling. null means that the document is not assigned to specific user. [Filter(multi eq)]

_Type_: **[Users](Systems.Security.Users.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### CurrencyDirectory

The currency directory, containing all the convertion rates, used by the document. null means that the document does not need currency convertions. [Filter(multi eq)]

_Type_: **[CurrencyDirectories](General.CurrencyDirectories.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### DealType

Deal type that caused this entry. [Required] [Filter(multi eq)]

_Type_: **[DealTypes](Finance.Vat.DealTypes.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### DocumentType

The user defined type of the document. Determines document behaviour, properties, additional amounts, validation, generations, etc. [Required] [Filter(multi eq)]

_Type_: **[DocumentTypes](General.DocumentTypes.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### EnterpriseCompany

The enterprise company which issued the document. [Required] [Filter(multi eq)]

_Type_: **[EnterpriseCompanies](General.EnterpriseCompanies.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### EnterpriseCompanyLocation

The enterprise company location which issued the document. null means that there is only one location within the enterprise company and locations are not used. [Filter(multi eq)]

_Type_: **[CompanyLocations](General.Contacts.CompanyLocations.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### FromCompanyDivision

The division of the company, issuing the document. null when the document is not issued by any specific division. [Filter(multi eq)]

_Type_: **[CompanyDivisions](General.Contacts.CompanyDivisions.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### FromParty

The party which issued the document. [Required] [Filter(multi eq)]

_Type_: **[Parties](General.Contacts.Parties.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### MasterDocument

In a multi-document tree, this is the root document, that created the whole tree. If this is the root it is equal to Id. [Required] [Filter(multi eq)]

_Type_: **[Documents](General.Documents.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### Parent

In a multi-document tree, this is the direct parent document. If this is the root it is null. [Filter(multi eq)]

_Type_: **[Documents](General.Documents.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### Party

The corresponding party that is involved in the operation that caused this entry. [Required] [Filter(multi eq)]

_Type_: **[Parties](General.Contacts.Parties.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### PrimeCauseDocument

The document that is the prime cause for creation of the current document. [Filter(multi eq)]

_Type_: **[Documents](General.Documents.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### ReferencedDocumentType

Type of the document that represents the operation that caused this entry. [Required] [Filter(multi eq)]

_Type_: **[DocumentTypes](General.DocumentTypes.md)**  
_Supported Filters_: **Equals, EqualsIn**  

_Front-End Recalc Expressions:_  
`IIF( obj.Parent.IsDocumentTypeEntityInvoice( ), obj.Parent.DocumentType, obj.ReferencedDocumentType)`
### ResponsiblePerson

The person that is responsible for this order or transaction. It could be the sales person, the orderer, etc. [Filter(multi eq)]

_Type_: **[Persons](General.Contacts.Persons.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### ReverseOfDocument

The document which the current document is reverse of. [Filter(multi eq)] [ReadOnly]

_Type_: **[Documents](General.Documents.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### Sequence

The sequence that will be used to give new numbers to the documents of this type. [Filter(multi eq)] [ReadOnly]

_Type_: **[Sequences](General.Sequences.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### ToCompanyDivision

The division of the company, receiving the document. null when the document is not received by any specific division. [Filter(multi eq)]

_Type_: **[CompanyDivisions](General.Contacts.CompanyDivisions.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### ToParty

The party which should receive the document. [Filter(multi eq)]

_Type_: **[Parties](General.Contacts.Parties.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### UserStatus

The user status of this document if applicable for this document type. null means unknown or not yet set. [Filter(multi eq)] [ReadOnly]

_Type_: **[DocumentTypeUserStatuses](General.DocumentTypeUserStatuses.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  


## API Methods

Methods that can be invoked in public APIs.

### ChangeState

Changes the document state to the specified new state  
_Return Type_: **void**  
_Declaring Type_: **[Documents](General.Documents.md)**  
_Domain API Request_: **POST**  

**Parameters**  
  * **newState**  
    The desired new state of the document  
    _Type_: General.DocumentState  
    Enumeration of document system states  
    _Allowed Values (General.DocumentState Enum Members)_  

    | Value | Description |
    | ---- | --- |
    | New | New document, just created. Can be edited. (Stored as 0). <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'New' |
    | Adjustment | Document which adjusts other released documents. (Stored as 5). <br /> _Model Value:_ 5 <br /> _Domain API Value:_ 'Adjustment' |
    | Planned | Planned by the system for future releasing. (Stored as 10). <br /> _Model Value:_ 10 <br /> _Domain API Value:_ 'Planned' |
    | FirmPlanned | Planned by operator for future releasing. (Stored as 20). <br /> _Model Value:_ 20 <br /> _Domain API Value:_ 'FirmPlanned' |
    | Released | Released document. Changes can be applied only through adjustment documents. (Stored as 30). <br /> _Model Value:_ 30 <br /> _Domain API Value:_ 'Released' |
    | Completed | Work has completed. (Stored as 40). <br /> _Model Value:_ 40 <br /> _Domain API Value:_ 'Completed' |
    | Closed | The document is audited and closed. Adjustments are not allowed, but reopening is allowed. (Stored as 50). <br /> _Model Value:_ 50 <br /> _Domain API Value:_ 'Closed' |


  * **userStatus**  
    The desired new user status of the document. Can be null.  
    _Type_: [DocumentTypeUserStatuses](General.DocumentTypeUserStatuses.md)  
     _Optional_: True  
    _Default Value_: null  


The process of changing the document state is very labor intensive and includes              validation, generation of sub-documents and some other document-specific tasks.                          The state changing process might be very time-consuming, usually ranging              from 500 to 5000 milliseconds.                          Document states usually can only be advanced to higher states, but there are              exceptions from this rule. Database settings and configuration options might affect             the allowed state changes.                          Numerous kinds of document-specific and generic exceptions can be thrown during the             process.

### Complete

Changes the document state to Completed with all Release-ed sub-documents  
_Return Type_: **void**  
_Declaring Type_: **[Documents](General.Documents.md)**  
_Domain API Request_: **POST**  

**Parameters**  
  * **completion**  
    How the sub-documents will be completed, if at all  
    _Type_: General.DocumentCompletion  
    Determines how [Document](General.Documents.md) will be completed  
    _Allowed Values (General.DocumentCompletion Enum Members)_  

    | Value | Description |
    | ---- | --- |
    | OnlyDocument | Only the document will be completed <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'OnlyDocument' |
    | WithAllChildren | The document, along with is sub-documents, will be completed <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'WithAllChildren' |
    | WithReleasedChildren | The document, along with its Release-ed sub-documents, will be completed <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'WithReleasedChildren' |



The process of changing the document state is very labor intensive and includes              validation, generation of sub-documents and some other document-specific tasks.                          The state changing process might be very time-consuming, usually ranging              from 500 to 5000 milliseconds.                          Document states usually can only be advanced to higher states, but there are              exceptions from this rule. Database settings and configuration options might affect             the allowed state changes.                          Numerous kinds of document-specific and generic exceptions can be thrown during the             process.

### MakeVoid

Makes the document void. The operation is irreversible.  
_Return Type_: **void**  
_Declaring Type_: **[Documents](General.Documents.md)**  
_Domain API Request_: **POST**  

**Parameters**  
  * **reason**  
    The reason for voiding the document.  
    _Type_: string  

  * **voidType**  
    The type of void operation to execute.  
    _Type_: General.DocumentsRepositoryBase.VoidType  
    Specifies the type of void operation  
    _Allowed Values (General.DocumentsRepositoryBase.VoidType Enum Members)_  

    | Value | Description |
    | ---- | --- |
    | VoidDocument | Void only the document. If there are sub-documents, the operation might fail. <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'VoidDocument' |
    | VoidWithSubDocuments | Void the document and its non-released sub-documents. If there are released sub-documents, the operation might fail. <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'VoidWithSubDocuments' |
    | VoidWithReleased<br />SubDocuments | Void the document and all of its sub-documents, even the released ones. <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'VoidWithReleased<br />SubDocuments' |

     _Optional_: True  
    _Default Value_: VoidDocument  


### GetPrintout

Gets a document printout as a file. The returned value is Base64 string representation of the file contents.  
_Return Type_: **string**  
_Declaring Type_: **[Documents](General.Documents.md)**  
_Domain API Request_: **POST**  

**Parameters**  
  * **fileFormat**  
    The file format: pdf, html, xlsx, xls, docx, txt and png. The default format is 'pdf'.  
    _Type_: string  
     _Optional_: True  
    _Default Value_: pdf  

  * **printout**  
    The printout defined for the document type of the document. If null the default printout of the document type is used.  
    _Type_: [Printouts](General.Printouts.md)  
     _Optional_: True  
    _Default Value_: null  


### Recalculate

The document and all of its owned objects will be altered to become valid.  
_Return Type_: **void**  
_Declaring Type_: **[Documents](General.Documents.md)**  
_Domain API Request_: **POST**  

In some cases the objects in child collection of the document depend on values from other child objects.             This method ensures that all child objects are properly validated.             The changes are only in memory and are not committed to the server.

### GetAllParentDocuments

Gets all parent documents, traversing the parent document chain by using the [Parent](General.Documents.md#parent) property.  
_Return Type_: **Collection Of [Documents](General.Documents.md)**  
_Declaring Type_: **[Documents](General.Documents.md)**  
_Domain API Request_: **GET**  

**Parameters**  
  * **includeSelf**  
    if set to true the current document is included.  
    _Type_: boolean  
     _Optional_: True  
    _Default Value_: False  



## Business Rules

[!list erp.entity=Finance.Vat.Entries erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Finance.Vat.Entries erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Finance.Vat.Entries erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Vat_Entries?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Vat_Entries?$top=10>

