---
uid: Logistics.Inventory.StoreOrders
---
# Logistics.Inventory.StoreOrders Entity

Orders for store transactions. After an order is executed, store transaction is created. Entity: Inv_Store_Orders

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [CompleteTime](Logistics.Inventory.StoreOrders.md#completetime) | datetime (nullable) | Exact time, when the document was last completed[Filter(ge;le)] 
| [CreationTime](Logistics.Inventory.StoreOrders.md#creationtime) | datetime | Date/Time when the document was created [Required][Filter(ge;le)] 
| [CreationUser](Logistics.Inventory.StoreOrders.md#creationuser) | string | The login name of the user, who created the document [Required][Filter(like)] 
| [DocumentDate](Logistics.Inventory.StoreOrders.md#documentdate) | datetime | The date on which the document was issued [Required][Filter(eq;ge;le)][ORD] 
| [DocumentNo](Logistics.Inventory.StoreOrders.md#documentno) | string | Document number, unique within Document_Type_Id [Required][Filter(eq;like)][ORD] 
| [DocumentNotes](Logistics.Inventory.StoreOrders.md#documentnotes) | string (nullable) | Notes for this Document 
| [DocumentVersion](Logistics.Inventory.StoreOrders.md#documentversion) | int32 | [Filter(eq;ge;le)] 
| [DriverName](Logistics.Inventory.StoreOrders.md#drivername) | string (nullable) | The name of the driver, who will deliver the stocks. 
| [DueDate](Logistics.Inventory.StoreOrders.md#duedate) | datetime | The final date, when the store transaction should occur. [Required] [Default(Today)] [Filter(ge;le)] [ORD] 
| [EntityName](Logistics.Inventory.StoreOrders.md#entityname) | string | The entity name of the document equal to the entity name of the document type.[Filter(eq)] [ORD] 
| [Id](Logistics.Inventory.StoreOrders.md#id) | guid |  
| [IsReleased](Logistics.Inventory.StoreOrders.md#isreleased) | boolean | True if the document is not void and its state is released or greater. [Required] [Default(false)] [Filter(eq)] [ReadOnly] 
| [IsSingleExecution](Logistics.Inventory.StoreOrders.md#issingleexecution) | boolean | Specifies whether the document is a single execution of its order document. [Required] [Default(false)] [Filter(eq)] [ReadOnly] 
| [MovementType](Logistics.Inventory.StoreOrders.md#movementtype) | [MovementType](Logistics.Inventory.StoreOrders.md#movementtype) | Store order movement type. R=RECEIPT, I=ISSUE. [Required] [Default("R")] [Filter(multi eq)] 
| [ParentDocument<br />RelationshipType](Logistics.Inventory.StoreOrders.md#parentdocumentrelationshiptype) | [ParentDocument<br />RelationshipType](Logistics.Inventory.StoreOrders.md#parentdocumentrelationshiptype) (nullable) | Type of relationship between the current document and the parent document(s). Affects the constraints for execution/completion for the documents. Possible values: 'S' = 'Subtask', 'N' = 'Next task'. 
| [PlannedCompletionDate](Logistics.Inventory.StoreOrders.md#plannedcompletiondate) | datetime (nullable) | Date, when the quantities are expected to be completely issued/received. [Filter(ge;le)] 
| [PlannedReleaseDate](Logistics.Inventory.StoreOrders.md#plannedreleasedate) | datetime (nullable) | Date, when the respective store transaction document is scheduled to be released to the supplier or manufacturing. This is respected by all PAB (projected available balance) and ATP (available to promise) calculations as the date on which the store transaction is scheduled to occur. [Filter(ge;le)] 
| [PlanningOnly](Logistics.Inventory.StoreOrders.md#planningonly) | boolean (nullable) | Indicates that the document is used only for planning (and as consequence its state cannot be greater than Planned) [Required] 
| [ReadOnly](Logistics.Inventory.StoreOrders.md#readonly) | boolean | True - the document is read only; false - the document is not read only [Required] 
| [ReferenceDate](Logistics.Inventory.StoreOrders.md#referencedate) | datetime (nullable) | The date to which this document refers, i.e. when the action really occurred. If null, Document_Date is taken [Filter(ge;le)] 
| [ReferenceDocumentNo](Logistics.Inventory.StoreOrders.md#referencedocumentno) | string (nullable) | The number of the document (issued by the other party), which was the reason for the creation of the current document. The numebr should be unique within the party documents [Filter(eq;like)] 
| [ReleaseTime](Logistics.Inventory.StoreOrders.md#releasetime) | datetime (nullable) | Exact time, when the document was first released [Filter(ge;le)] 
| [State](Logistics.Inventory.StoreOrders.md#state) | [DocumentState](Logistics.Inventory.StoreOrders.md#state) | 0=New;5=Corrective;10=Computer Planned;20=Human Planned;30=Released;40=Completed;50=Closed [Required][Filter(eq;ge;le)] 
| [Status](Logistics.Inventory.StoreOrders.md#status) | string | P=Planned; F=Firm planned; R=Released; C=Completed. [Required] [Default("P")] 
| [TempTransportCompanyName](Logistics.Inventory.StoreOrders.md#temptransportcompanyname) | string (nullable) | Obsolete. Not used. 
| [VehicleRegNumber](Logistics.Inventory.StoreOrders.md#vehicleregnumber) | string (nullable) | Obsolete. Not used. 
| [Void](Logistics.Inventory.StoreOrders.md#void) | boolean | True if the document is null and void [Required][Filter(eq)] 
| [VoidReason](Logistics.Inventory.StoreOrders.md#voidreason) | string (nullable) | Reason for voiding the document, entered by the user 
| [VoidTime](Logistics.Inventory.StoreOrders.md#voidtime) | datetime (nullable) | Date/time when the document has become void 
| [VoidUser](Logistics.Inventory.StoreOrders.md#voiduser) | string (nullable) | The user who voided the document 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [AccessKey](Logistics.Inventory.StoreOrders.md#accesskey) | [AccessKeys](Systems.Security.AccessKeys.md) (nullable) | The access key, containing the user permissions for this document. null means that all users have unlimited permissions |
| [AdjustedDocument](Logistics.Inventory.StoreOrders.md#adjusteddocument) | [Documents](General.Documents.md) (nullable) | The primary document, which the current document adjusts. null when this is not an adjustment document |
| [AssignedToUser](Logistics.Inventory.StoreOrders.md#assignedtouser) | [Users](Systems.Security.Users.md) (nullable) | The user to which this document is assigned for handling. null means that the document is not assigned to specific user |
| [CurrencyDirectory](Logistics.Inventory.StoreOrders.md#currencydirectory) | [CurrencyDirectories](General.CurrencyDirectories.md) (nullable) | The currency directory, containing all the convertion rates, used by the document. null means that the document does not need currency convertions |
| [DocumentCurrency](Logistics.Inventory.StoreOrders.md#documentcurrency) | [Currencies](General.Currencies.md) | The currency in which the document amounts are expessed. [Required] [Filter(multi eq)] |
| [DocumentType](Logistics.Inventory.StoreOrders.md#documenttype) | [DocumentTypes](General.DocumentTypes.md) | The user defined type of the document. Determines document behaviour, properties, additional amounts, validation, generations, etc. [Required] |
| [EnterpriseCompany](Logistics.Inventory.StoreOrders.md#enterprisecompany) | [EnterpriseCompanies](General.EnterpriseCompanies.md) | The enterprise company which issued the document [Required] |
| [EnterpriseCompanyLocation](Logistics.Inventory.StoreOrders.md#enterprisecompanylocation) | [CompanyLocations](General.Contacts.CompanyLocations.md) (nullable) | The enterprise company location which issued the document. null means that there is only one location within the enterprise company and locations are not used |
| [FromCompanyDivision](Logistics.Inventory.StoreOrders.md#fromcompanydivision) | [CompanyDivisions](General.Contacts.CompanyDivisions.md) (nullable) | The division of the company, issuing the document. null when the document is not issued by any specific division |
| [FromParty](Logistics.Inventory.StoreOrders.md#fromparty) | [Parties](General.Contacts.Parties.md) | The party which issued the document [Required] |
| [IssuedByParty](Logistics.Inventory.StoreOrders.md#issuedbyparty) | [Parties](General.Contacts.Parties.md) (nullable) | The party, which issued the goods. [Filter(multi eq)] |
| [MasterDocument](Logistics.Inventory.StoreOrders.md#masterdocument) | [Documents](General.Documents.md) | In a multi-document tree, this is the root document, that created the whole tree. If this is the root it is equal to Id [Required] |
| [OrderingPerson](Logistics.Inventory.StoreOrders.md#orderingperson) | [Persons](General.Contacts.Persons.md) (nullable) | The person, which ordered the operation. [Filter(multi eq)] |
| [Parent](Logistics.Inventory.StoreOrders.md#parent) | [Documents](General.Documents.md) (nullable) | In a multi-document tree, this is the direct parent document. If this is the root it is null |
| [PrimeCauseDocument](Logistics.Inventory.StoreOrders.md#primecausedocument) | [Documents](General.Documents.md) (nullable) | The document that is the prime cause for creation of the current document |
| [ReceivedByParty](Logistics.Inventory.StoreOrders.md#receivedbyparty) | [Parties](General.Contacts.Parties.md) (nullable) | The party, which received the goods. [Filter(multi eq)] |
| [ResponsiblePerson](Logistics.Inventory.StoreOrders.md#responsibleperson) | [Persons](General.Contacts.Persons.md) (nullable) | The person that is responsible for this order or transaction. It could be the sales person, the orderer, etc. |
| [ReverseOfDocument](Logistics.Inventory.StoreOrders.md#reverseofdocument) | [Documents](General.Documents.md) (nullable) | The document which the current document is reverse of |
| [Sequence](Logistics.Inventory.StoreOrders.md#sequence) | [Sequences](General.Sequences.md) (nullable) | The sequence that will be used to give new numbers to the documents of this type |
| [Store](Logistics.Inventory.StoreOrders.md#store) | [Stores](Logistics.Inventory.Stores.md) | The designated warehouse for the operation. [Required] [Filter(multi eq)] |
| [ToCompanyDivision](Logistics.Inventory.StoreOrders.md#tocompanydivision) | [CompanyDivisions](General.Contacts.CompanyDivisions.md) | The division of the company, receiving the document. null when the document is not received by any specific division |
| [ToParty](Logistics.Inventory.StoreOrders.md#toparty) | [Parties](General.Contacts.Parties.md) (nullable) | The party which should receive the document |
| [UserStatus](Logistics.Inventory.StoreOrders.md#userstatus) | [DocumentTypeUserStatuses](General.DocumentTypeUserStatuses.md) (nullable) | The user status of this document if applicable for this document type. null means unknown or not yet set |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Comments | [DocumentComments](General.DocumentComments.md) | List of [DocumentComment](General.DocumentComments.md) child objects, based on the [DocumentComment.Document](General.DocumentComments.md#document) back reference 
| DistributedAmounts | [DocumentDistributedAmounts](General.DocumentDistributedAmounts.md) | List of [DocumentDistributed<br />Amount](General.DocumentDistributedAmounts.md) child objects, based on the [DocumentDistributedAmount.Document](General.DocumentDistributedAmounts.md#document) back reference 
| DocumentAmounts | [DocumentAmounts](General.DocumentAmounts.md) | List of [DocumentAmount](General.DocumentAmounts.md) child objects, based on the [DocumentAmount.Document](General.DocumentAmounts.md#document) back reference 
| FileAttachments | [DocumentFileAttachments](General.DocumentFileAttachments.md) | List of [DocumentFileAttachment](General.DocumentFileAttachments.md) child objects, based on the [DocumentFileAttachment.Document](General.DocumentFileAttachments.md#document) back reference 
| LineAmounts | [DocumentLineAmounts](General.DocumentLineAmounts.md) | List of [DocumentLineAmount](General.DocumentLineAmounts.md) child objects, based on the [DocumentLineAmount.Document](General.DocumentLineAmounts.md#document) back reference 
| Lines | [StoreOrderLines](Logistics.Inventory.StoreOrderLines.md) | List of [StoreOrderLine](Logistics.Inventory.StoreOrderLines.md) child objects, based on the [Logistics.Inventory.StoreOrderLine.StoreOrder](Logistics.Inventory.StoreOrderLines.md#storeorder) back reference 
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

### DriverName

The name of the driver, who will deliver the stocks.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### DueDate

The final date, when the store transaction should occur. [Required] [Default(Today)] [Filter(ge;le)] [ORD]

_Type_: **datetime**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **True**  
_Default Value_: **CurrentDate**  

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

### MovementType

Store order movement type. R=RECEIPT, I=ISSUE. [Required] [Default("R")] [Filter(multi eq)]

_Type_: **[MovementType](Logistics.Inventory.StoreOrders.md#movementtype)**  
Specifies the movement type (direction) of a warehouse document.  
_Allowed Values (Logistics.Inventory.MovementType Enum Members)_  

| Value | Description |
| ---- | --- |
| Issue | Goods issue <br /> _Database Value:_ 'I' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Issue' |
| Receipt | Goods receive <br /> _Database Value:_ 'R' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'Receipt' |

_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **Receipt**  

### ParentDocumentRelationshipType

Type of relationship between the current document and the parent document(s). Affects the constraints for execution/completion for the documents. Possible values: 'S' = 'Subtask', 'N' = 'Next task'.

_Type_: **[ParentDocument<br />RelationshipType](Logistics.Inventory.StoreOrders.md#parentdocumentrelationshiptype) (nullable)**  
Relationship between parent and child documents  
_Allowed Values (General.ParentDocumentRelationshipType Enum Members)_  

| Value | Description |
| ---- | --- |
| Subtask | The child document is a sub-task of the parent document. (Complete child to complete parent) <br /> _Database Value:_ 'S' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Subtask' |
| NextTask | The child document is next task of the parent document. (Complete parent to complete child) <br /> _Database Value:_ 'N' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'NextTask' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### PlannedCompletionDate

Date, when the quantities are expected to be completely issued/received. [Filter(ge;le)]

_Type_: **datetime (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### PlannedReleaseDate

Date, when the respective store transaction document is scheduled to be released to the supplier or manufacturing. This is respected by all PAB (projected available balance) and ATP (available to promise) calculations as the date on which the store transaction is scheduled to occur. [Filter(ge;le)]

_Type_: **datetime (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
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

### State

0=New;5=Corrective;10=Computer Planned;20=Human Planned;30=Released;40=Completed;50=Closed [Required][Filter(eq;ge;le)]

_Type_: **[DocumentState](Logistics.Inventory.StoreOrders.md#state)**  
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

### Status

P=Planned; F=Firm planned; R=Released; C=Completed. [Required] [Default("P")]

_Type_: **string**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **P**  

### TempTransportCompanyName

Obsolete. Not used.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### VehicleRegNumber

Obsolete. Not used.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

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

### DocumentCurrency

The currency in which the document amounts are expessed. [Required] [Filter(multi eq)]

_Type_: **[Currencies](General.Currencies.md)**  
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

### FromCompanyDivision

The division of the company, issuing the document. null when the document is not issued by any specific division

_Type_: **[CompanyDivisions](General.Contacts.CompanyDivisions.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### FromParty

The party which issued the document [Required]

_Type_: **[Parties](General.Contacts.Parties.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### IssuedByParty

The party, which issued the goods. [Filter(multi eq)]

_Type_: **[Parties](General.Contacts.Parties.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### MasterDocument

In a multi-document tree, this is the root document, that created the whole tree. If this is the root it is equal to Id [Required]

_Type_: **[Documents](General.Documents.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### OrderingPerson

The person, which ordered the operation. [Filter(multi eq)]

_Type_: **[Persons](General.Contacts.Persons.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### Parent

In a multi-document tree, this is the direct parent document. If this is the root it is null

_Type_: **[Documents](General.Documents.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### PrimeCauseDocument

The document that is the prime cause for creation of the current document

_Type_: **[Documents](General.Documents.md) (nullable)**  
_Supported Filters_: **EqualsIn**  

### ReceivedByParty

The party, which received the goods. [Filter(multi eq)]

_Type_: **[Parties](General.Contacts.Parties.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

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

### Store

The designated warehouse for the operation. [Required] [Filter(multi eq)]

_Type_: **[Stores](Logistics.Inventory.Stores.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### ToCompanyDivision

The division of the company, receiving the document. null when the document is not received by any specific division

_Type_: **[CompanyDivisions](General.Contacts.CompanyDivisions.md)**  
_Supported Filters_: **NotFilterable**  

### ToParty

The party which should receive the document

_Type_: **[Parties](General.Contacts.Parties.md) (nullable)**  
_Supported Filters_: **EqualsIn**  

### UserStatus

The user status of this document if applicable for this document type. null means unknown or not yet set

_Type_: **[DocumentTypeUserStatuses](General.DocumentTypeUserStatuses.md) (nullable)**  
_Supported Filters_: **EqualsIn**  



## Business Rules

[!list erp.entity=Logistics.Inventory.StoreOrders erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Logistics.Inventory.StoreOrders erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Logistics.Inventory.StoreOrders erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_Inventory_StoreOrders?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_Inventory_StoreOrders?$top=10>

