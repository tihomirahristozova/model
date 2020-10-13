---
uid: Logistics.Shipment.TransportationRequisitions
---
# Logistics.Shipment.TransportationRequisitions Entity

Client requisition for transportation. Entity: Log_Transportation_Requisitions

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [CompleteTime](Logistics.Shipment.TransportationRequisitions.md#completetime) | datetime (nullable) | Exact time, when the document was last completed[Filter(ge;le)] 
| [CreationTime](Logistics.Shipment.TransportationRequisitions.md#creationtime) | datetime | Date/Time when the document was created [Required][Filter(ge;le)] 
| [CreationUser](Logistics.Shipment.TransportationRequisitions.md#creationuser) | string | The login name of the user, who created the document [Required][Filter(like)] 
| [DocumentDate](Logistics.Shipment.TransportationRequisitions.md#documentdate) | datetime | The date on which the document was issued [Required][Filter(eq;ge;le)][ORD] 
| [DocumentNo](Logistics.Shipment.TransportationRequisitions.md#documentno) | string | Document number, unique within Document_Type_Id [Required][Filter(eq;like)][ORD] 
| [DocumentNotes](Logistics.Shipment.TransportationRequisitions.md#documentnotes) | string (nullable) | Notes for this Document 
| [DocumentVersion](Logistics.Shipment.TransportationRequisitions.md#documentversion) | int32 | [Filter(eq;ge;le)] 
| [EntityName](Logistics.Shipment.TransportationRequisitions.md#entityname) | string | The entity name of the document equal to the entity name of the document type.[Filter(eq)] [ORD] 
| [Id](Logistics.Shipment.TransportationRequisitions.md#id) | guid |  
| [ParentDocument<br />RelationshipType](Logistics.Shipment.TransportationRequisitions.md#parentdocumentrelationshiptype) | [ParentDocument<br />RelationshipType](Logistics.Shipment.TransportationRequisitions.md#parentdocumentrelationshiptype) (nullable) | Type of relationship between the current document and the parent document(s). Affects the constraints for execution/completion for the documents. Possible values: 'S' = 'Subtask', 'N' = 'Next task'. 
| [PlanningOnly](Logistics.Shipment.TransportationRequisitions.md#planningonly) | boolean (nullable) | Indicates that the document is used only for planning (and as consequence its state cannot be greater than Planned) [Required] 
| [ReadOnly](Logistics.Shipment.TransportationRequisitions.md#readonly) | boolean | True - the document is read only; false - the document is not read only [Required] 
| [ReferenceDate](Logistics.Shipment.TransportationRequisitions.md#referencedate) | datetime (nullable) | The date to which this document refers, i.e. when the action really occurred. If null, Document_Date is taken [Filter(ge;le)] 
| [ReferenceDocumentNo](Logistics.Shipment.TransportationRequisitions.md#referencedocumentno) | string (nullable) | The number of the document (issued by the other party), which was the reason for the creation of the current document. The numebr should be unique within the party documents [Filter(eq;like)] 
| [ReleaseTime](Logistics.Shipment.TransportationRequisitions.md#releasetime) | datetime (nullable) | Exact time, when the document was first released [Filter(ge;le)] 
| [RequestedArrivalDate](Logistics.Shipment.TransportationRequisitions.md#requestedarrivaldate) | date | Requested arrival date. null when no specific date is requested. [Required] [Filter(ge;le)] 
| [RequestedArrivalTime](Logistics.Shipment.TransportationRequisitions.md#requestedarrivaltime) | time (nullable) | Requested arrival time. null when no specific time is requested. [Filter(ge;le)] 
| [RequestedDepartureDate](Logistics.Shipment.TransportationRequisitions.md#requesteddeparturedate) | date | Requested date of departure. null when no specific date is requested. [Required] [Filter(ge;le)] 
| [RequestedDepartureTime](Logistics.Shipment.TransportationRequisitions.md#requesteddeparturetime) | time (nullable) | Requested time of departure. null when no specific time is requested. [Filter(ge;le)] 
| [State](Logistics.Shipment.TransportationRequisitions.md#state) | [DocumentState](Logistics.Shipment.TransportationRequisitions.md#state) | 0=New;5=Corrective;10=Computer Planned;20=Human Planned;30=Released;40=Completed;50=Closed [Required][Filter(eq;ge;le)] 
| [Void](Logistics.Shipment.TransportationRequisitions.md#void) | boolean | True if the document is null and void [Required][Filter(eq)] 
| [VoidReason](Logistics.Shipment.TransportationRequisitions.md#voidreason) | string (nullable) | Reason for voiding the document, entered by the user 
| [VoidTime](Logistics.Shipment.TransportationRequisitions.md#voidtime) | datetime (nullable) | Date/time when the document has become void 
| [VoidUser](Logistics.Shipment.TransportationRequisitions.md#voiduser) | string (nullable) | The user who voided the document 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [AccessKey](Logistics.Shipment.TransportationRequisitions.md#accesskey) | [AccessKeys](Systems.Security.AccessKeys.md) (nullable) | The access key, containing the user permissions for this document. null means that all users have unlimited permissions |
| [AdjustedDocument](Logistics.Shipment.TransportationRequisitions.md#adjusteddocument) | [Documents](General.Documents.md) (nullable) | The primary document, which the current document adjusts. null when this is not an adjustment document |
| [AssignedToUser](Logistics.Shipment.TransportationRequisitions.md#assignedtouser) | [Users](Systems.Security.Users.md) (nullable) | The user to which this document is assigned for handling. null means that the document is not assigned to specific user |
| [CurrencyDirectory](Logistics.Shipment.TransportationRequisitions.md#currencydirectory) | [CurrencyDirectories](General.CurrencyDirectories.md) (nullable) | The currency directory, containing all the convertion rates, used by the document. null means that the document does not need currency convertions |
| [DocumentType](Logistics.Shipment.TransportationRequisitions.md#documenttype) | [DocumentTypes](General.DocumentTypes.md) | The user defined type of the document. Determines document behaviour, properties, additional amounts, validation, generations, etc. [Required] |
| [EnterpriseCompany](Logistics.Shipment.TransportationRequisitions.md#enterprisecompany) | [EnterpriseCompanies](General.EnterpriseCompanies.md) | The enterprise company which issued the document [Required] |
| [EnterpriseCompanyLocation](Logistics.Shipment.TransportationRequisitions.md#enterprisecompanylocation) | [CompanyLocations](General.Contacts.CompanyLocations.md) (nullable) | The enterprise company location which issued the document. null means that there is only one location within the enterprise company and locations are not used |
| [FromCompanyDivision](Logistics.Shipment.TransportationRequisitions.md#fromcompanydivision) | [CompanyDivisions](General.Contacts.CompanyDivisions.md) (nullable) | The division of the company, issuing the document. null when the document is not issued by any specific division |
| [FromParty](Logistics.Shipment.TransportationRequisitions.md#fromparty) | [Parties](General.Contacts.Parties.md) | The party which issued the document [Required] |
| [MasterDocument](Logistics.Shipment.TransportationRequisitions.md#masterdocument) | [Documents](General.Documents.md) | In a multi-document tree, this is the root document, that created the whole tree. If this is the root it is equal to Id [Required] |
| [Parent](Logistics.Shipment.TransportationRequisitions.md#parent) | [Documents](General.Documents.md) (nullable) | In a multi-document tree, this is the direct parent document. If this is the root it is null |
| [PrimeCauseDocument](Logistics.Shipment.TransportationRequisitions.md#primecausedocument) | [Documents](General.Documents.md) (nullable) | The document that is the prime cause for creation of the current document |
| [ResponsiblePerson](Logistics.Shipment.TransportationRequisitions.md#responsibleperson) | [Persons](General.Contacts.Persons.md) (nullable) | The person that is responsible for this order or transaction. It could be the sales person, the orderer, etc. |
| [ReverseOfDocument](Logistics.Shipment.TransportationRequisitions.md#reverseofdocument) | [Documents](General.Documents.md) (nullable) | The document which the current document is reverse of |
| [Sequence](Logistics.Shipment.TransportationRequisitions.md#sequence) | [Sequences](General.Sequences.md) (nullable) | The sequence that will be used to give new numbers to the documents of this type |
| [ToCompanyDivision](Logistics.Shipment.TransportationRequisitions.md#tocompanydivision) | [CompanyDivisions](General.Contacts.CompanyDivisions.md) | The division of the company, receiving the document. null when the document is not received by any specific division |
| [ToParty](Logistics.Shipment.TransportationRequisitions.md#toparty) | [Parties](General.Contacts.Parties.md) (nullable) | The party which should receive the document |
| [TransportFromGeoPoint](Logistics.Shipment.TransportationRequisitions.md#transportfromgeopoint) | [GeoPoints](General.Geography.GeoPoints.md) (nullable) | Geographical location of the loading, if available. [Filter(multi eq)] |
| [TransportFromParty](Logistics.Shipment.TransportationRequisitions.md#transportfromparty) | [Parties](General.Contacts.Parties.md) | Shipping party. [Required] [Filter(multi eq)] |
| [TransportFromParty<br />ContactMechanism](Logistics.Shipment.TransportationRequisitions.md#transportfrompartycontactmechanism) | [PartyContactMechanisms](General.Contacts.PartyContactMechanisms.md) | Loading address. [Required] [Filter(multi eq)] |
| [TransportToGeoPoint](Logistics.Shipment.TransportationRequisitions.md#transporttogeopoint) | [GeoPoints](General.Geography.GeoPoints.md) (nullable) | Geographical location of the unloading, if available. [Filter(multi eq)] |
| [TransportToParty](Logistics.Shipment.TransportationRequisitions.md#transporttoparty) | [Parties](General.Contacts.Parties.md) | Receiving party. [Required] [Filter(multi eq)] |
| [TransportToParty<br />ContactMechanism](Logistics.Shipment.TransportationRequisitions.md#transporttopartycontactmechanism) | [PartyContactMechanisms](General.Contacts.PartyContactMechanisms.md) | Unload address. [Required] [Filter(multi eq)] |
| [UserStatus](Logistics.Shipment.TransportationRequisitions.md#userstatus) | [DocumentTypeUserStatuses](General.DocumentTypeUserStatuses.md) (nullable) | The user status of this document if applicable for this document type. null means unknown or not yet set |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Comments | [DocumentComments](General.DocumentComments.md) | List of [DocumentComment](General.DocumentComments.md) child objects, based on the [DocumentComment.Document](General.DocumentComments.md#document) back reference 
| DistributedAmounts | [DocumentDistributedAmounts](General.DocumentDistributedAmounts.md) | List of [DocumentDistributed<br />Amount](General.DocumentDistributedAmounts.md) child objects, based on the [DocumentDistributedAmount.Document](General.DocumentDistributedAmounts.md#document) back reference 
| DocumentAmounts | [DocumentAmounts](General.DocumentAmounts.md) |  
| FileAttachments | [DocumentFileAttachments](General.DocumentFileAttachments.md) | List of [DocumentFileAttachment](General.DocumentFileAttachments.md) child objects, based on the [DocumentFileAttachment.Document](General.DocumentFileAttachments.md#document) back reference 
| LineAmounts | [DocumentLineAmounts](General.DocumentLineAmounts.md) | List of [DocumentLineAmount](General.DocumentLineAmounts.md) child objects, based on the [DocumentLineAmount.Document](General.DocumentLineAmounts.md#document) back reference 
| Lines | [TransportationRequisitionLines](Logistics.Shipment.TransportationRequisitionLines.md) | List of [Transportation<br />RequisitionLine](Logistics.Shipment.Transportation<br />RequisitionLines.md) child objects, based on the [Logistics.Shipment.Transportation<br />RequisitionLine.TransportationRequisition](Logistics.Shipment.Transportation<br />RequisitionLines.md#transportationrequisition) back reference 
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

### EntityName

The entity name of the document equal to the entity name of the document type.[Filter(eq)] [ORD]

_Type_: **string**  
_Supported Filters_: **Equals**  
_Supports Order By_: **True**  

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### ParentDocumentRelationshipType

Type of relationship between the current document and the parent document(s). Affects the constraints for execution/completion for the documents. Possible values: 'S' = 'Subtask', 'N' = 'Next task'.

_Type_: **[ParentDocument<br />RelationshipType](Logistics.Shipment.TransportationRequisitions.md#parentdocumentrelationshiptype) (nullable)**  
Relationship between parent and child documents  
_Allowed Values (General.ParentDocumentRelationshipType Enum Members)_  

| Value | Description |
| ---- | --- |
| Subtask | The child document is a sub-task of the parent document. (Complete child to complete parent) <br /> _Database Value:_ 'S' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Subtask' |
| NextTask | The child document is next task of the parent document. (Complete parent to complete child) <br /> _Database Value:_ 'N' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'NextTask' |

_Supported Filters_: **NotFilterable**  
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

### RequestedArrivalDate

Requested arrival date. null when no specific date is requested. [Required] [Filter(ge;le)]

_Type_: **date**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### RequestedArrivalTime

Requested arrival time. null when no specific time is requested. [Filter(ge;le)]

_Type_: **time (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### RequestedDepartureDate

Requested date of departure. null when no specific date is requested. [Required] [Filter(ge;le)]

_Type_: **date**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### RequestedDepartureTime

Requested time of departure. null when no specific time is requested. [Filter(ge;le)]

_Type_: **time (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### State

0=New;5=Corrective;10=Computer Planned;20=Human Planned;30=Released;40=Completed;50=Closed [Required][Filter(eq;ge;le)]

_Type_: **[DocumentState](Logistics.Shipment.TransportationRequisitions.md#state)**  
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

### Parent

In a multi-document tree, this is the direct parent document. If this is the root it is null

_Type_: **[Documents](General.Documents.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

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

### TransportFromGeoPoint

Geographical location of the loading, if available. [Filter(multi eq)]

_Type_: **[GeoPoints](General.Geography.GeoPoints.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### TransportFromParty

Shipping party. [Required] [Filter(multi eq)]

_Type_: **[Parties](General.Contacts.Parties.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### TransportFromPartyContactMechanism

Loading address. [Required] [Filter(multi eq)]

_Type_: **[PartyContactMechanisms](General.Contacts.PartyContactMechanisms.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### TransportToGeoPoint

Geographical location of the unloading, if available. [Filter(multi eq)]

_Type_: **[GeoPoints](General.Geography.GeoPoints.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### TransportToParty

Receiving party. [Required] [Filter(multi eq)]

_Type_: **[Parties](General.Contacts.Parties.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### TransportToPartyContactMechanism

Unload address. [Required] [Filter(multi eq)]

_Type_: **[PartyContactMechanisms](General.Contacts.PartyContactMechanisms.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### UserStatus

The user status of this document if applicable for this document type. null means unknown or not yet set

_Type_: **[DocumentTypeUserStatuses](General.DocumentTypeUserStatuses.md) (nullable)**  
_Supported Filters_: **EqualsIn**  



## Business Rules

[!list erp.entity=Logistics.Shipment.TransportationRequisitions erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Logistics.Shipment.TransportationRequisitions erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Logistics.Shipment.TransportationRequisitions erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_Shipment_TransportationRequisitions?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_Shipment_TransportationRequisitions?$top=10>

