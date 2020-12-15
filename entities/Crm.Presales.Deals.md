---
uid: Crm.Presales.Deals
---
# Crm.Presales.Deals Entity

Potential deals (Opportunities). Entity: Crm_Deals

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [AdjustmentNumber](Crm.Presales.Deals.md#adjustmentnumber) | int32 | Consecutive number of the correction that this document is applying to the adjusted document. [Required] [Default(0)] [ReadOnly] 
| [AdjustmentTime](Crm.Presales.Deals.md#adjustmenttime) | datetime (nullable) | Date/time when the document last has been adjusted by corrective document. [ReadOnly] 
| [AdjustmentUser](Crm.Presales.Deals.md#adjustmentuser) | string (nullable) | The user who adjusted the document. [ReadOnly] 
| [CompleteTime](Crm.Presales.Deals.md#completetime) | datetime (nullable) | Date and time when the document was completed (State set to Completed). [Filter(ge;le)] [ReadOnly] 
| [CreationTime](Crm.Presales.Deals.md#creationtime) | datetime | Date/Time when the document was created. [Required] [Default(Now)] [Filter(ge;le)] [ReadOnly] 
| [CreationUser](Crm.Presales.Deals.md#creationuser) | string | The login name of the user, who created the document. [Required] [Filter(like)] [ReadOnly] 
| [DealStatus](Crm.Presales.Deals.md#dealstatus) | [DealStatus](Crm.Presales.Deals.md#dealstatus) | Current status of this deal. 'SUC' = Successful, 'UNS' = Unsuccessful, 'INP' = In progress. [Required] [Default("INP")] [Filter(multi eq)] 
| [DocumentDate](Crm.Presales.Deals.md#documentdate) | date | The date on which the document was issued. [Required] [Default(Today)] [Filter(eq;ge;le)] [ORD] 
| [DocumentNo](Crm.Presales.Deals.md#documentno) | string | Document number, unique within Document_Type_Id. [Required] [Filter(eq;like)] [ORD] 
| [DocumentNotes](Crm.Presales.Deals.md#documentnotes) | string (nullable) | Notes for this Document. 
| [DocumentVersion](Crm.Presales.Deals.md#documentversion) | int32 | Consecutive version number, starting with 1. Each update produces a new version of the document. [Required] [Default(1)] [Filter(eq;ge;le)] [ReadOnly] 
| [EntityName](Crm.Presales.Deals.md#entityname) | string | The entity name of the document header. [Required] [Filter(eq)] [ORD] [ReadOnly] 
| [ExpectedRevenue](Crm.Presales.Deals.md#expectedrevenue) | [Amount](../data-types.md#amount) | Expected total revenue. For automatically renewed contracts it's the amount until the first renewal. [Currency: ExpectedRevenueCurrency] [Required] [Default(0)] [Filter(ge;le)] 
| [Id](Crm.Presales.Deals.md#id) | guid |  
| [IsReleased](Crm.Presales.Deals.md#isreleased) | boolean | True if the document is not void and its state is released or greater. [Required] [Default(false)] [Filter(eq)] [ReadOnly] 
| [IsSingleExecution](Crm.Presales.Deals.md#issingleexecution) | boolean | Specifies whether the document is a single execution of its order document. [Required] [Default(false)] [Filter(eq)] [ReadOnly] 
| [ParentDocument<br />RelationshipType](Crm.Presales.Deals.md#parentdocumentrelationshiptype) | [ParentDocument<br />RelationshipType](Crm.Presales.Deals.md#parentdocumentrelationshiptype) (nullable) | Type of relationship between the current document and the parent document(s). Affects the constraints for execution/completion for the documents. Possible values: 'S' = 'Subtask', 'N' = 'Next task'. [ReadOnly] 
| [PlanningOnly](Crm.Presales.Deals.md#planningonly) | boolean | Indicates that the document is used only for planning (and as consequence its state cannot be greater than Planned). [Required] [Default(false)] [ReadOnly] 
| [ReadOnly](Crm.Presales.Deals.md#readonly) | boolean | True - the document is read only; false - the document is not read only. [Required] [Default(false)] [ReadOnly] 
| [ReferenceDate](Crm.Presales.Deals.md#referencedate) | datetime (nullable) | The date to which this document refers, i.e. when the action really occurred. If null, Document_Date is taken. [Default(Today)] [Filter(ge;le)] 
| [ReferenceDocumentNo](Crm.Presales.Deals.md#referencedocumentno) | string (nullable) | The number of the document (issued by the other party), which was the reason for the creation of the current document. The numebr should be unique within the party documents. [Filter(eq;like)] 
| [ReleaseTime](Crm.Presales.Deals.md#releasetime) | datetime (nullable) | Date and time when the document was released (State set to Released). [Filter(ge;le)] [ReadOnly] 
| [RevenueEndDate](Crm.Presales.Deals.md#revenueenddate) | datetime | Expected date on which the last revenue from this deal will occur. [Required] [Default(Today)] [Filter(ge;le)] 
| [RevenueStartDate](Crm.Presales.Deals.md#revenuestartdate) | datetime | Expected date on which revenue from this deal will start. [Required] [Default(Today)] [Filter(ge;le)] 
| [State](Crm.Presales.Deals.md#state) | [DocumentState](Crm.Presales.Deals.md#state) | The current system state of the document. Allowed values: 0=New;5=Corrective;10=Computer Planned;20=Human Planned;30=Released;40=Completed;50=Closed. [Required] [Default(0)] [Filter(multi eq;ge;le)] [ReadOnly] 
| [SuccessProbability](Crm.Presales.Deals.md#successprobability) | decimal | Probability of success of that opportunity in percents (for example, 15 percent is stored as 0.15). [Required] [Default(0)] 
| [Void](Crm.Presales.Deals.md#void) | boolean | True if the document is null and void. [Required] [Default(false)] [Filter(eq)] [ReadOnly] 
| [VoidReason](Crm.Presales.Deals.md#voidreason) | string (nullable) | Reason for voiding the document, entered by the user. [ReadOnly] 
| [VoidTime](Crm.Presales.Deals.md#voidtime) | datetime (nullable) | Date/time when the document has become void. [ReadOnly] 
| [VoidUser](Crm.Presales.Deals.md#voiduser) | string (nullable) | The user who voided the document. [ReadOnly] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [AccessKey](Crm.Presales.Deals.md#accesskey) | [AccessKeys](Systems.Security.AccessKeys.md) (nullable) | The access key, containing the user permissions for this document. null means that all users have unlimited permissions. [Filter(multi eq)] |
| [AdjustedDocument](Crm.Presales.Deals.md#adjusteddocument) | [Documents](General.Documents.md) (nullable) | The primary document, which the current document adjusts. null when this is not an adjustment document. [Filter(multi eq)] [ReadOnly] |
| [AssignedToUser](Crm.Presales.Deals.md#assignedtouser) | [Users](Systems.Security.Users.md) (nullable) | The user to which this document is assigned for handling. null means that the document is not assigned to specific user. [Filter(multi eq)] |
| [CurrencyDirectory](Crm.Presales.Deals.md#currencydirectory) | [CurrencyDirectories](General.CurrencyDirectories.md) (nullable) | The currency directory, containing all the convertion rates, used by the document. null means that the document does not need currency convertions. [Filter(multi eq)] |
| [Dealer](Crm.Presales.Deals.md#dealer) | [Dealers](Crm.Dealers.md) (nullable) | The external dealer, which provided the opportunity. [Filter(multi eq)] |
| [DocumentType](Crm.Presales.Deals.md#documenttype) | [DocumentTypes](General.DocumentTypes.md) | The user defined type of the document. Determines document behaviour, properties, additional amounts, validation, generations, etc. [Required] [Filter(multi eq)] |
| [EnterpriseCompany](Crm.Presales.Deals.md#enterprisecompany) | [EnterpriseCompanies](General.EnterpriseCompanies.md) | The enterprise company which issued the document. [Required] [Filter(multi eq)] |
| [EnterpriseCompanyLocation](Crm.Presales.Deals.md#enterprisecompanylocation) | [CompanyLocations](General.Contacts.CompanyLocations.md) (nullable) | The enterprise company location which issued the document. null means that there is only one location within the enterprise company and locations are not used. [Filter(multi eq)] |
| [ExpectedRevenueCurrency](Crm.Presales.Deals.md#expectedrevenuecurrency) | [Currencies](General.Currencies.md) | The currency of Expected Revenue. [Required] [Filter(multi eq)] |
| [FromCompanyDivision](Crm.Presales.Deals.md#fromcompanydivision) | [CompanyDivisions](General.Contacts.CompanyDivisions.md) (nullable) | The division of the company, issuing the document. null when the document is not issued by any specific division. [Filter(multi eq)] |
| [FromParty](Crm.Presales.Deals.md#fromparty) | [Parties](General.Contacts.Parties.md) | The party which issued the document. [Required] [Filter(multi eq)] |
| [LeadingSalesPerson](Crm.Presales.Deals.md#leadingsalesperson) | [SalesPersons](Crm.SalesPersons.md) | The sales person, responsible for the opportunity. [Required] [Filter(multi eq)] |
| [MasterDocument](Crm.Presales.Deals.md#masterdocument) | [Documents](General.Documents.md) | In a multi-document tree, this is the root document, that created the whole tree. If this is the root it is equal to Id. [Required] [Filter(multi eq)] |
| [Parent](Crm.Presales.Deals.md#parent) | [Documents](General.Documents.md) (nullable) | In a multi-document tree, this is the direct parent document. If this is the root it is null. [Filter(multi eq)] |
| [Party](Crm.Presales.Deals.md#party) | [Parties](General.Contacts.Parties.md) | The prospect customers party. The party might not yet have a customer record. [Required] [Filter(multi eq)] |
| [PrimeCauseDocument](Crm.Presales.Deals.md#primecausedocument) | [Documents](General.Documents.md) (nullable) | The document that is the prime cause for creation of the current document. [Filter(multi eq)] |
| [ResponsiblePerson](Crm.Presales.Deals.md#responsibleperson) | [Persons](General.Contacts.Persons.md) (nullable) | The person that is responsible for this order or transaction. It could be the sales person, the orderer, etc. [Filter(multi eq)] |
| [ReverseOfDocument](Crm.Presales.Deals.md#reverseofdocument) | [Documents](General.Documents.md) (nullable) | The document which the current document is reverse of. [Filter(multi eq)] [ReadOnly] |
| [Sequence](Crm.Presales.Deals.md#sequence) | [Sequences](General.Sequences.md) (nullable) | The sequence that will be used to give new numbers to the documents of this type. [Filter(multi eq)] [ReadOnly] |
| [ToCompanyDivision](Crm.Presales.Deals.md#tocompanydivision) | [CompanyDivisions](General.Contacts.CompanyDivisions.md) (nullable) | The division of the company, receiving the document. null when the document is not received by any specific division. [Filter(multi eq)] |
| [ToParty](Crm.Presales.Deals.md#toparty) | [Parties](General.Contacts.Parties.md) (nullable) | The party which should receive the document. [Filter(multi eq)] |
| [UserStatus](Crm.Presales.Deals.md#userstatus) | [DocumentTypeUserStatuses](General.DocumentTypeUserStatuses.md) (nullable) | The user status of this document if applicable for this document type. null means unknown or not yet set. [Filter(multi eq)] [ReadOnly] |

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

### DealStatus

Current status of this deal. 'SUC' = Successful, 'UNS' = Unsuccessful, 'INP' = In progress. [Required] [Default("INP")] [Filter(multi eq)]

_Type_: **[DealStatus](Crm.Presales.Deals.md#dealstatus)**  
Allowed values for the [DealStatus](Crm.Presales.Deals.md#dealstatus) data attribute  
_Allowed Values (Crm.Presales.DealsRepository.DealStatus Enum Members)_  

| Value | Description |
| ---- | --- |
| InProgress | InProgress value. Stored as 'INP'. <br /> _Database Value:_ 'INP' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'InProgress' |
| Successful | Successful value. Stored as 'SUC'. <br /> _Database Value:_ 'SUC' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'Successful' |
| Unsuccessful | Unsuccessful value. Stored as 'UNS'. <br /> _Database Value:_ 'UNS' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'Unsuccessful' |

_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **InProgress**  

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

### ExpectedRevenue

Expected total revenue. For automatically renewed contracts it's the amount until the first renewal. [Currency: ExpectedRevenueCurrency] [Required] [Default(0)] [Filter(ge;le)]

_Type_: **[Amount](../data-types.md#amount)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

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

_Type_: **[ParentDocument<br />RelationshipType](Crm.Presales.Deals.md#parentdocumentrelationshiptype) (nullable)**  
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

### ReferenceDocumentNo

The number of the document (issued by the other party), which was the reason for the creation of the current document. The numebr should be unique within the party documents. [Filter(eq;like)]

_Type_: **string (nullable)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### ReleaseTime

Date and time when the document was released (State set to Released). [Filter(ge;le)] [ReadOnly]

_Type_: **datetime (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### RevenueEndDate

Expected date on which the last revenue from this deal will occur. [Required] [Default(Today)] [Filter(ge;le)]

_Type_: **datetime**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **CurrentDate**  

_Front-End Recalc Expressions:_  
`IIF( ( obj.RevenueStartDate >= obj.RevenueEndDate), obj.RevenueStartDate, obj.RevenueEndDate)`
### RevenueStartDate

Expected date on which revenue from this deal will start. [Required] [Default(Today)] [Filter(ge;le)]

_Type_: **datetime**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **CurrentDate**  

### State

The current system state of the document. Allowed values: 0=New;5=Corrective;10=Computer Planned;20=Human Planned;30=Released;40=Completed;50=Closed. [Required] [Default(0)] [Filter(multi eq;ge;le)] [ReadOnly]

_Type_: **[DocumentState](Crm.Presales.Deals.md#state)**  
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

### SuccessProbability

Probability of success of that opportunity in percents (for example, 15 percent is stored as 0.15). [Required] [Default(0)]

_Type_: **decimal**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  

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

### Dealer

The external dealer, which provided the opportunity. [Filter(multi eq)]

_Type_: **[Dealers](Crm.Dealers.md) (nullable)**  
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

### ExpectedRevenueCurrency

The currency of Expected Revenue. [Required] [Filter(multi eq)]

_Type_: **[Currencies](General.Currencies.md)**  
_Supported Filters_: **Equals, EqualsIn**  

_Front-End Recalc Expressions:_  
`IIF( ( obj.ExpectedRevenueCurrency != null), obj.ExpectedRevenueCurrency, obj.EnterpriseCompany.BaseCurrency)`
### FromCompanyDivision

The division of the company, issuing the document. null when the document is not issued by any specific division. [Filter(multi eq)]

_Type_: **[CompanyDivisions](General.Contacts.CompanyDivisions.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### FromParty

The party which issued the document. [Required] [Filter(multi eq)]

_Type_: **[Parties](General.Contacts.Parties.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### LeadingSalesPerson

The sales person, responsible for the opportunity. [Required] [Filter(multi eq)]

_Type_: **[SalesPersons](Crm.SalesPersons.md)**  
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

The prospect customers party. The party might not yet have a customer record. [Required] [Filter(multi eq)]

_Type_: **[Parties](General.Contacts.Parties.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### PrimeCauseDocument

The document that is the prime cause for creation of the current document. [Filter(multi eq)]

_Type_: **[Documents](General.Documents.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

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

[!list erp.entity=Crm.Presales.Deals erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Crm.Presales.Deals erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Crm.Presales.Deals erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_Presales_Deals?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Crm_Presales_Deals?$top=10>

