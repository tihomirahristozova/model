---
uid: Logistics.Shipment.TransportationOrders
---
# Logistics.Shipment.TransportationOrders Entity

**Namespace:** [Logistics.Shipment](Logistics.Shipment.md)  
**Inherited From:** [General.Documents](General.Documents.md)  

Transportation ordered to specific carrier or vehicle. Entity: Log_Transportation_Orders

## Default Visualization
Default Display Text Format:  
_{DocumentType.Code}:{DocumentNo} - {DocumentType.TypeName:T}_  
Default Search Member:  
_DocumentNo_  

## Aggregate
  @aggregates  
Aggregate Tree  
* [Logistics.Shipment.TransportationOrders](Logistics.Shipment.TransportationOrders.md)  
  * [Logistics.Shipment.TransportationOrderLines](Logistics.Shipment.TransportationOrderLines.md)  
  * [General.DocumentAmounts](General.DocumentAmounts.md)  
    * [General.DocumentAmountReferencedDocuments](General.DocumentAmountReferencedDocuments.md)  
  * [General.DocumentComments](General.DocumentComments.md)  
  * [General.DocumentDistributedAmounts](General.DocumentDistributedAmounts.md)  
  * [General.DocumentFileAttachments](General.DocumentFileAttachments.md)  
  * [General.DocumentLineAmounts](General.DocumentLineAmounts.md)  
  * [General.DocumentPrints](General.DocumentPrints.md)  
  * [General.DocumentStateChanges](General.DocumentStateChanges.md)  
  * [General.DocumentVersions](General.DocumentVersions.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [AdjustmentNumber](Logistics.Shipment.TransportationOrders.md#adjustmentnumber) | int32 | Consecutive number of the correction that this document is applying to the adjusted document. [Required] [Default(0)] [ReadOnly] (Inherited from [Documents](General.Documents.md)) 
| [AdjustmentTime](Logistics.Shipment.TransportationOrders.md#adjustmenttime) | datetime (nullable) | Date/time when the document last has been adjusted by corrective document. [ReadOnly] (Inherited from [Documents](General.Documents.md)) 
| [AdjustmentUser](Logistics.Shipment.TransportationOrders.md#adjustmentuser) | string (nullable) | The user who adjusted the document. [ReadOnly] (Inherited from [Documents](General.Documents.md)) 
| [ArrivalDate](Logistics.Shipment.TransportationOrders.md#arrivaldate) | date | Planned arrival date. [Required] [Filter(ge;le)] 
| [ArrivalTime](Logistics.Shipment.TransportationOrders.md#arrivaltime) | time | Planned arrival time. [Required] [Filter(ge;le)] 
| [CompleteTime](Logistics.Shipment.TransportationOrders.md#completetime) | datetime (nullable) | Date and time when the document was completed (State set to Completed). [Filter(ge;le)] [ReadOnly] (Inherited from [Documents](General.Documents.md)) 
| [CreationTime](Logistics.Shipment.TransportationOrders.md#creationtime) | datetime | Date/Time when the document was created. [Required] [Default(Now)] [Filter(ge;le)] [ReadOnly] (Inherited from [Documents](General.Documents.md)) 
| [CreationUser](Logistics.Shipment.TransportationOrders.md#creationuser) | string | The login name of the user, who created the document. [Required] [Filter(like)] [ReadOnly] (Inherited from [Documents](General.Documents.md)) 
| [DepartureDate](Logistics.Shipment.TransportationOrders.md#departuredate) | date | Planned departure date. [Required] [Filter(ge;le)] 
| [DepartureTime](Logistics.Shipment.TransportationOrders.md#departuretime) | time | Planned departure time. [Required] [Filter(ge;le)] 
| [DocumentDate](Logistics.Shipment.TransportationOrders.md#documentdate) | date | The date on which the document was issued. [Required] [Default(Today)] [Filter(eq;ge;le)] [ORD] (Inherited from [Documents](General.Documents.md)) 
| [DocumentNo](Logistics.Shipment.TransportationOrders.md#documentno) | string | Document number, unique within Document_Type_Id. [Required] [Filter(eq;like)] [ORD] (Inherited from [Documents](General.Documents.md)) 
| [DocumentNotes](Logistics.Shipment.TransportationOrders.md#documentnotes) | string (nullable) | Notes for this Document. (Inherited from [Documents](General.Documents.md)) 
| [DocumentVersion](Logistics.Shipment.TransportationOrders.md#documentversion) | int32 | Consecutive version number, starting with 1. Each update produces a new version of the document. [Required] [Default(1)] [Filter(eq;ge;le)] [ReadOnly] (Inherited from [Documents](General.Documents.md)) 
| [EntityName](Logistics.Shipment.TransportationOrders.md#entityname) | string | The entity name of the document header. [Required] [Filter(eq)] [ORD] [ReadOnly] (Inherited from [Documents](General.Documents.md)) 
| [Id](Logistics.Shipment.TransportationOrders.md#id) | guid |  
| [ParentDocument<br />RelationshipType](Logistics.Shipment.TransportationOrders.md#parentdocumentrelationshiptype) | [ParentDocument<br />RelationshipType](Logistics.Shipment.TransportationOrders.md#parentdocumentrelationshiptype) (nullable) | Type of relationship between the current document and the parent document(s). Affects the constraints for execution/completion for the documents. Possible values: 'S' = 'Subtask', 'N' = 'Next task'. [ReadOnly] (Inherited from [Documents](General.Documents.md)) 
| [PlanningOnly](Logistics.Shipment.TransportationOrders.md#planningonly) | boolean | Indicates that the document is used only for planning (and as consequence its state cannot be greater than Planned). [Required] [Default(false)] [ReadOnly] (Inherited from [Documents](General.Documents.md)) 
| [ReadOnly](Logistics.Shipment.TransportationOrders.md#readonly) | boolean | True - the document is read only; false - the document is not read only. [Required] [Default(false)] [ReadOnly] (Inherited from [Documents](General.Documents.md)) 
| [ReferenceDate](Logistics.Shipment.TransportationOrders.md#referencedate) | datetime (nullable) | The date to which this document refers, i.e. when the action really occurred. If null, Document_Date is taken. [Default(Today)] [Filter(ge;le)] (Inherited from [Documents](General.Documents.md)) 
| [ReferenceDocumentNo](Logistics.Shipment.TransportationOrders.md#referencedocumentno) | string (nullable) | The number of the document (issued by the other party), which was the reason for the creation of the current document. The numebr should be unique within the party documents. [Filter(eq;like)] (Inherited from [Documents](General.Documents.md)) 
| [ReleaseTime](Logistics.Shipment.TransportationOrders.md#releasetime) | datetime (nullable) | Date and time when the document was released (State set to Released). [Filter(ge;le)] [ReadOnly] (Inherited from [Documents](General.Documents.md)) 
| [State](Logistics.Shipment.TransportationOrders.md#state) | [DocumentState](Logistics.Shipment.TransportationOrders.md#state) | The current system state of the document. Allowed values: 0=New;5=Corrective;10=Computer Planned;20=Human Planned;30=Released;40=Completed;50=Closed. [Required] [Default(0)] [Filter(multi eq;ge;le)] [ReadOnly] (Inherited from [Documents](General.Documents.md)) 
| [Void](Logistics.Shipment.TransportationOrders.md#void) | boolean | True if the document is null and void. [Required] [Default(false)] [Filter(eq)] [ReadOnly] (Inherited from [Documents](General.Documents.md)) 
| [VoidReason](Logistics.Shipment.TransportationOrders.md#voidreason) | string (nullable) | Reason for voiding the document, entered by the user. [ReadOnly] (Inherited from [Documents](General.Documents.md)) 
| [VoidTime](Logistics.Shipment.TransportationOrders.md#voidtime) | datetime (nullable) | Date/time when the document has become void. [ReadOnly] (Inherited from [Documents](General.Documents.md)) 
| [VoidUser](Logistics.Shipment.TransportationOrders.md#voiduser) | string (nullable) | The user who voided the document. [ReadOnly] (Inherited from [Documents](General.Documents.md)) 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [AccessKey](Logistics.Shipment.TransportationOrders.md#accesskey) | [AccessKeys](Systems.Security.AccessKeys.md) (nullable) | The access key, containing the user permissions for this document. null means that all users have unlimited permissions. [Filter(multi eq)] (Inherited from [Documents](General.Documents.md)) |
| [AdjustedDocument](Logistics.Shipment.TransportationOrders.md#adjusteddocument) | [Documents](General.Documents.md) (nullable) | The primary document, which the current document adjusts. null when this is not an adjustment document. [Filter(multi eq)] [ReadOnly] (Inherited from [Documents](General.Documents.md)) |
| [AssignedToUser](Logistics.Shipment.TransportationOrders.md#assignedtouser) | [Users](Systems.Security.Users.md) (nullable) | The user to which this document is assigned for handling. null means that the document is not assigned to specific user. [Filter(multi eq)] (Inherited from [Documents](General.Documents.md)) |
| [Carrier](Logistics.Shipment.TransportationOrders.md#carrier) | [Carriers](Logistics.Shipment.Carriers.md) (nullable) | The carrier chosen for this transportation. null when the transportation is done with own transport. [Filter(multi eq)] |
| [Crew](Logistics.Shipment.TransportationOrders.md#crew) | [Crews](Applications.Fleet.Crews.md) (nullable) | The crew which is assigned to operate the vehicle of the current Transportation Order. If null means the crew is yet unknown or the order is executed by external carrier. [Filter(multi eq)] [Introduced in version 18.2] |
| [CurrencyDirectory](Logistics.Shipment.TransportationOrders.md#currencydirectory) | [CurrencyDirectories](General.CurrencyDirectories.md) (nullable) | The currency directory, containing all the convertion rates, used by the document. null means that the document does not need currency convertions. [Filter(multi eq)] (Inherited from [Documents](General.Documents.md)) |
| [DocumentType](Logistics.Shipment.TransportationOrders.md#documenttype) | [DocumentTypes](General.DocumentTypes.md) | The user defined type of the document. Determines document behaviour, properties, additional amounts, validation, generations, etc. [Required] [Filter(multi eq)] (Inherited from [Documents](General.Documents.md)) |
| [EnterpriseCompany](Logistics.Shipment.TransportationOrders.md#enterprisecompany) | [EnterpriseCompanies](General.EnterpriseCompanies.md) | The enterprise company which issued the document. [Required] [Filter(multi eq)] (Inherited from [Documents](General.Documents.md)) |
| [EnterpriseCompanyLocation](Logistics.Shipment.TransportationOrders.md#enterprisecompanylocation) | [CompanyLocations](General.Contacts.CompanyLocations.md) (nullable) | The enterprise company location which issued the document. null means that there is only one location within the enterprise company and locations are not used. [Filter(multi eq)] (Inherited from [Documents](General.Documents.md)) |
| [FromCompanyDivision](Logistics.Shipment.TransportationOrders.md#fromcompanydivision) | [CompanyDivisions](General.Contacts.CompanyDivisions.md) (nullable) | The division of the company, issuing the document. null when the document is not issued by any specific division. [Filter(multi eq)] (Inherited from [Documents](General.Documents.md)) |
| [FromGeoPoint](Logistics.Shipment.TransportationOrders.md#fromgeopoint) | [GeoPoints](General.Geography.GeoPoints.md) | The geographic point from which the route begins. [Required] [Filter(multi eq)] |
| [FromParty](Logistics.Shipment.TransportationOrders.md#fromparty) | [Parties](General.Contacts.Parties.md) | The party which issued the document. [Required] [Filter(multi eq)] (Inherited from [Documents](General.Documents.md)) |
| [MasterDocument](Logistics.Shipment.TransportationOrders.md#masterdocument) | [Documents](General.Documents.md) | In a multi-document tree, this is the root document, that created the whole tree. If this is the root it is equal to Id. [Required] [Filter(multi eq)] (Inherited from [Documents](General.Documents.md)) |
| [Parent](Logistics.Shipment.TransportationOrders.md#parent) | [Documents](General.Documents.md) (nullable) | In a multi-document tree, this is the direct parent document. If this is the root it is null. [Filter(multi eq)] (Inherited from [Documents](General.Documents.md)) |
| [PrimeCauseDocument](Logistics.Shipment.TransportationOrders.md#primecausedocument) | [Documents](General.Documents.md) (nullable) | The document that is the prime cause for creation of the current document. [Filter(multi eq)] (Inherited from [Documents](General.Documents.md)) |
| [ResponsiblePerson](Logistics.Shipment.TransportationOrders.md#responsibleperson) | [Persons](General.Contacts.Persons.md) (nullable) | The person that is responsible for this order or transaction. It could be the sales person, the orderer, etc. [Filter(multi eq)] (Inherited from [Documents](General.Documents.md)) |
| [ReverseOfDocument](Logistics.Shipment.TransportationOrders.md#reverseofdocument) | [Documents](General.Documents.md) (nullable) | The document which the current document is reverse of. [Filter(multi eq)] [ReadOnly] (Inherited from [Documents](General.Documents.md)) |
| [Sequence](Logistics.Shipment.TransportationOrders.md#sequence) | [Sequences](General.Sequences.md) (nullable) | The sequence that will be used to give new numbers to the documents of this type. [Filter(multi eq)] [ReadOnly] (Inherited from [Documents](General.Documents.md)) |
| [ToCompanyDivision](Logistics.Shipment.TransportationOrders.md#tocompanydivision) | [CompanyDivisions](General.Contacts.CompanyDivisions.md) (nullable) | The division of the company, receiving the document. null when the document is not received by any specific division. [Filter(multi eq)] (Inherited from [Documents](General.Documents.md)) |
| [ToGeoPoint](Logistics.Shipment.TransportationOrders.md#togeopoint) | [GeoPoints](General.Geography.GeoPoints.md) | The geographic point at which the route ends. [Required] [Filter(multi eq)] |
| [ToParty](Logistics.Shipment.TransportationOrders.md#toparty) | [Parties](General.Contacts.Parties.md) (nullable) | The party which should receive the document. [Filter(multi eq)] (Inherited from [Documents](General.Documents.md)) |
| [TransportationMode](Logistics.Shipment.TransportationOrders.md#transportationmode) | [TransportationModes](Logistics.Shipment.TransportationModes.md) (nullable) | The mode of transportation which should be used for this order. null when it is unknown or doesn't matter. [Filter(multi eq)] |
| [TransportationVehicle](Logistics.Shipment.TransportationOrders.md#transportationvehicle) | [TransportationVehicles](Logistics.Shipment.TransportationVehicles.md) (nullable) | The own transportation vehicle, which will be used for the transportation. [Filter(multi eq)] |
| [UserStatus](Logistics.Shipment.TransportationOrders.md#userstatus) | [DocumentTypeUserStatuses](General.DocumentTypeUserStatuses.md) (nullable) | The user status of this document if applicable for this document type. null means unknown or not yet set. [Filter(multi eq)] [ReadOnly] (Inherited from [Documents](General.Documents.md)) |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Comments | [DocumentComments](General.DocumentComments.md) | List of [DocumentComment](General.DocumentComments.md) child objects, based on the [General.DocumentComment.Document](General.DocumentComments.md#document) back reference (Inherited from [Documents](General.Documents.md)) 
| DistributedAmounts | [DocumentDistributedAmounts](General.DocumentDistributedAmounts.md) | List of [DocumentDistributed<br />Amount](General.DocumentDistributedAmounts.md) child objects, based on the [General.DocumentDistributedAmount.Document](General.DocumentDistributedAmounts.md#document) back reference (Inherited from [Documents](General.Documents.md)) 
| DocumentAmounts | [DocumentAmounts](General.DocumentAmounts.md) | List of [DocumentAmount](General.DocumentAmounts.md) child objects, based on the [General.DocumentAmount.Document](General.DocumentAmounts.md#document) back reference (Inherited from [Documents](General.Documents.md)) 
| FileAttachments | [DocumentFileAttachments](General.DocumentFileAttachments.md) | List of [DocumentFileAttachment](General.DocumentFileAttachments.md) child objects, based on the [General.DocumentFileAttachment.Document](General.DocumentFileAttachments.md#document) back reference (Inherited from [Documents](General.Documents.md)) 
| LineAmounts | [DocumentLineAmounts](General.DocumentLineAmounts.md) | List of [DocumentLineAmount](General.DocumentLineAmounts.md) child objects, based on the [General.DocumentLineAmount.Document](General.DocumentLineAmounts.md#document) back reference (Inherited from [Documents](General.Documents.md)) 
| Lines | [TransportationOrderLines](Logistics.Shipment.TransportationOrderLines.md) | List of [TransportationOrderLine](Logistics.Shipment.TransportationOrderLines.md) child objects, based on the [Logistics.Shipment.TransportationOrderLine.TransportationOrder](Logistics.Shipment.TransportationOrderLines.md#transportationorder) back reference 
| Prints | [DocumentPrints](General.DocumentPrints.md) | List of [DocumentPrint](General.DocumentPrints.md) child objects, based on the [General.DocumentPrint.Document](General.DocumentPrints.md#document) back reference (Inherited from [Documents](General.Documents.md)) 
| StateChanges | [DocumentStateChanges](General.DocumentStateChanges.md) | List of [DocumentStateChange](General.DocumentStateChanges.md) child objects, based on the [General.DocumentStateChange.Document](General.DocumentStateChanges.md#document) back reference (Inherited from [Documents](General.Documents.md)) 
| Versions | [DocumentVersions](General.DocumentVersions.md) | List of [DocumentVersion](General.DocumentVersions.md) child objects, based on the [General.DocumentVersion.Document](General.DocumentVersions.md#document) back reference (Inherited from [Documents](General.Documents.md)) 


## Attribute Details

### AdjustmentNumber

Consecutive number of the correction that this document is applying to the adjusted document. [Required] [Default(0)] [ReadOnly] (Inherited from [Documents](General.Documents.md))

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### AdjustmentTime

Date/time when the document last has been adjusted by corrective document. [ReadOnly] (Inherited from [Documents](General.Documents.md))

_Type_: **datetime (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### AdjustmentUser

The user who adjusted the document. [ReadOnly] (Inherited from [Documents](General.Documents.md))

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ArrivalDate

Planned arrival date. [Required] [Filter(ge;le)]

_Type_: **date**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### ArrivalTime

Planned arrival time. [Required] [Filter(ge;le)]

_Type_: **time**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### CompleteTime

Date and time when the document was completed (State set to Completed). [Filter(ge;le)] [ReadOnly] (Inherited from [Documents](General.Documents.md))

_Type_: **datetime (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### CreationTime

Date/Time when the document was created. [Required] [Default(Now)] [Filter(ge;le)] [ReadOnly] (Inherited from [Documents](General.Documents.md))

_Type_: **datetime**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **CurrentDateTime**  

### CreationUser

The login name of the user, who created the document. [Required] [Filter(like)] [ReadOnly] (Inherited from [Documents](General.Documents.md))

_Type_: **string**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### DepartureDate

Planned departure date. [Required] [Filter(ge;le)]

_Type_: **date**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### DepartureTime

Planned departure time. [Required] [Filter(ge;le)]

_Type_: **time**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### DocumentDate

The date on which the document was issued. [Required] [Default(Today)] [Filter(eq;ge;le)] [ORD] (Inherited from [Documents](General.Documents.md))

_Type_: **date**  
_Indexed_: **True**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **True**  
_Default Value_: **CurrentDate**  

### DocumentNo

Document number, unique within Document_Type_Id. [Required] [Filter(eq;like)] [ORD] (Inherited from [Documents](General.Documents.md))

_Type_: **string**  
_Indexed_: **True**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  

### DocumentNotes

Notes for this Document. (Inherited from [Documents](General.Documents.md))

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### DocumentVersion

Consecutive version number, starting with 1. Each update produces a new version of the document. [Required] [Default(1)] [Filter(eq;ge;le)] [ReadOnly] (Inherited from [Documents](General.Documents.md))

_Type_: **int32**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **1**  

### EntityName

The entity name of the document header. [Required] [Filter(eq)] [ORD] [ReadOnly] (Inherited from [Documents](General.Documents.md))

_Type_: **string**  
_Indexed_: **True**  
_Supported Filters_: **Equals**  
_Supports Order By_: **True**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### ParentDocumentRelationshipType

Type of relationship between the current document and the parent document(s). Affects the constraints for execution/completion for the documents. Possible values: 'S' = 'Subtask', 'N' = 'Next task'. [ReadOnly] (Inherited from [Documents](General.Documents.md))

_Type_: **[ParentDocument<br />RelationshipType](Logistics.Shipment.TransportationOrders.md#parentdocumentrelationshiptype) (nullable)**  
Relationship between parent and child documents  
_Allowed Values (General.ParentDocumentRelationshipType Enum Members)_  

| Value | Description |
| ---- | --- |
| Subtask | The child document is a sub-task of the parent document. (Complete child to complete parent) <br /> _Database Value:_ 'S' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Subtask' |
| NextTask | The child document is next task of the parent document. (Complete parent to complete child) <br /> _Database Value:_ 'N' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'NextTask' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### PlanningOnly

Indicates that the document is used only for planning (and as consequence its state cannot be greater than Planned). [Required] [Default(false)] [ReadOnly] (Inherited from [Documents](General.Documents.md))

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### ReadOnly

True - the document is read only; false - the document is not read only. [Required] [Default(false)] [ReadOnly] (Inherited from [Documents](General.Documents.md))

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### ReferenceDate

The date to which this document refers, i.e. when the action really occurred. If null, Document_Date is taken. [Default(Today)] [Filter(ge;le)] (Inherited from [Documents](General.Documents.md))

_Type_: **datetime (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **CurrentDate**  

### ReferenceDocumentNo

The number of the document (issued by the other party), which was the reason for the creation of the current document. The numebr should be unique within the party documents. [Filter(eq;like)] (Inherited from [Documents](General.Documents.md))

_Type_: **string (nullable)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### ReleaseTime

Date and time when the document was released (State set to Released). [Filter(ge;le)] [ReadOnly] (Inherited from [Documents](General.Documents.md))

_Type_: **datetime (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### State

The current system state of the document. Allowed values: 0=New;5=Corrective;10=Computer Planned;20=Human Planned;30=Released;40=Completed;50=Closed. [Required] [Default(0)] [Filter(multi eq;ge;le)] [ReadOnly] (Inherited from [Documents](General.Documents.md))

_Type_: **[DocumentState](Logistics.Shipment.TransportationOrders.md#state)**  
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

True if the document is null and void. [Required] [Default(false)] [Filter(eq)] [ReadOnly] (Inherited from [Documents](General.Documents.md))

_Type_: **boolean**  
_Indexed_: **True**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### VoidReason

Reason for voiding the document, entered by the user. [ReadOnly] (Inherited from [Documents](General.Documents.md))

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### VoidTime

Date/time when the document has become void. [ReadOnly] (Inherited from [Documents](General.Documents.md))

_Type_: **datetime (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### VoidUser

The user who voided the document. [ReadOnly] (Inherited from [Documents](General.Documents.md))

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### AccessKey

The access key, containing the user permissions for this document. null means that all users have unlimited permissions. [Filter(multi eq)] (Inherited from [Documents](General.Documents.md))

_Type_: **[AccessKeys](Systems.Security.AccessKeys.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### AdjustedDocument

The primary document, which the current document adjusts. null when this is not an adjustment document. [Filter(multi eq)] [ReadOnly] (Inherited from [Documents](General.Documents.md))

_Type_: **[Documents](General.Documents.md) (nullable)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  

### AssignedToUser

The user to which this document is assigned for handling. null means that the document is not assigned to specific user. [Filter(multi eq)] (Inherited from [Documents](General.Documents.md))

_Type_: **[Users](Systems.Security.Users.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### Carrier

The carrier chosen for this transportation. null when the transportation is done with own transport. [Filter(multi eq)]

_Type_: **[Carriers](Logistics.Shipment.Carriers.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### Crew

The crew which is assigned to operate the vehicle of the current Transportation Order. If null means the crew is yet unknown or the order is executed by external carrier. [Filter(multi eq)] [Introduced in version 18.2]

_Type_: **[Crews](Applications.Fleet.Crews.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### CurrencyDirectory

The currency directory, containing all the convertion rates, used by the document. null means that the document does not need currency convertions. [Filter(multi eq)] (Inherited from [Documents](General.Documents.md))

_Type_: **[CurrencyDirectories](General.CurrencyDirectories.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### DocumentType

The user defined type of the document. Determines document behaviour, properties, additional amounts, validation, generations, etc. [Required] [Filter(multi eq)] (Inherited from [Documents](General.Documents.md))

_Type_: **[DocumentTypes](General.DocumentTypes.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  

### EnterpriseCompany

The enterprise company which issued the document. [Required] [Filter(multi eq)] (Inherited from [Documents](General.Documents.md))

_Type_: **[EnterpriseCompanies](General.EnterpriseCompanies.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  

### EnterpriseCompanyLocation

The enterprise company location which issued the document. null means that there is only one location within the enterprise company and locations are not used. [Filter(multi eq)] (Inherited from [Documents](General.Documents.md))

_Type_: **[CompanyLocations](General.Contacts.CompanyLocations.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### FromCompanyDivision

The division of the company, issuing the document. null when the document is not issued by any specific division. [Filter(multi eq)] (Inherited from [Documents](General.Documents.md))

_Type_: **[CompanyDivisions](General.Contacts.CompanyDivisions.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### FromGeoPoint

The geographic point from which the route begins. [Required] [Filter(multi eq)]

_Type_: **[GeoPoints](General.Geography.GeoPoints.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### FromParty

The party which issued the document. [Required] [Filter(multi eq)] (Inherited from [Documents](General.Documents.md))

_Type_: **[Parties](General.Contacts.Parties.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### MasterDocument

In a multi-document tree, this is the root document, that created the whole tree. If this is the root it is equal to Id. [Required] [Filter(multi eq)] (Inherited from [Documents](General.Documents.md))

_Type_: **[Documents](General.Documents.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  

### Parent

In a multi-document tree, this is the direct parent document. If this is the root it is null. [Filter(multi eq)] (Inherited from [Documents](General.Documents.md))

_Type_: **[Documents](General.Documents.md) (nullable)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  

### PrimeCauseDocument

The document that is the prime cause for creation of the current document. [Filter(multi eq)] (Inherited from [Documents](General.Documents.md))

_Type_: **[Documents](General.Documents.md) (nullable)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  

### ResponsiblePerson

The person that is responsible for this order or transaction. It could be the sales person, the orderer, etc. [Filter(multi eq)] (Inherited from [Documents](General.Documents.md))

_Type_: **[Persons](General.Contacts.Persons.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### ReverseOfDocument

The document which the current document is reverse of. [Filter(multi eq)] [ReadOnly] (Inherited from [Documents](General.Documents.md))

_Type_: **[Documents](General.Documents.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### Sequence

The sequence that will be used to give new numbers to the documents of this type. [Filter(multi eq)] [ReadOnly] (Inherited from [Documents](General.Documents.md))

_Type_: **[Sequences](General.Sequences.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### ToCompanyDivision

The division of the company, receiving the document. null when the document is not received by any specific division. [Filter(multi eq)] (Inherited from [Documents](General.Documents.md))

_Type_: **[CompanyDivisions](General.Contacts.CompanyDivisions.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### ToGeoPoint

The geographic point at which the route ends. [Required] [Filter(multi eq)]

_Type_: **[GeoPoints](General.Geography.GeoPoints.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### ToParty

The party which should receive the document. [Filter(multi eq)] (Inherited from [Documents](General.Documents.md))

_Type_: **[Parties](General.Contacts.Parties.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### TransportationMode

The mode of transportation which should be used for this order. null when it is unknown or doesn't matter. [Filter(multi eq)]

_Type_: **[TransportationModes](Logistics.Shipment.TransportationModes.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### TransportationVehicle

The own transportation vehicle, which will be used for the transportation. [Filter(multi eq)]

_Type_: **[TransportationVehicles](Logistics.Shipment.TransportationVehicles.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### UserStatus

The user status of this document if applicable for this document type. null means unknown or not yet set. [Filter(multi eq)] [ReadOnly] (Inherited from [Documents](General.Documents.md))

_Type_: **[DocumentTypeUserStatuses](General.DocumentTypeUserStatuses.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  


## API Methods

Methods that can be invoked in public APIs.

### ChangeState

Changes the document state to the specified new state              (Inherited from [Documents](General.Documents.md))  
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

Changes the document state to Completed with all Release-ed sub-documents              (Inherited from [Documents](General.Documents.md))  
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

Makes the document void. The operation is irreversible.              (Inherited from [Documents](General.Documents.md))  
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

Gets a document printout as a file. The returned value is Base64 string representation of the file contents.              (Inherited from [Documents](General.Documents.md))  
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

The document and all of its owned objects will be altered to become valid.              (Inherited from [Documents](General.Documents.md))  
_Return Type_: **void**  
_Declaring Type_: **[Documents](General.Documents.md)**  
_Domain API Request_: **POST**  

In some cases the objects in child collection of the document depend on values from other child objects.             This method ensures that all child objects are properly validated.             The changes are only in memory and are not committed to the server.

### GetAllParentDocuments

Gets all parent documents, traversing the parent document chain by using the [Parent](General.Documents.md#parent) property.              (Inherited from [Documents](General.Documents.md))  
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

[!list erp.entity=Logistics.Shipment.TransportationOrders erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Logistics.Shipment.TransportationOrders erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Logistics.Shipment.TransportationOrders erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_Shipment_TransportationOrders?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_Shipment_TransportationOrders?$top=10>

