---
uid: Applications.Service.ServiceActivities
---
# Applications.Service.ServiceActivities Entity

Contains service activity headers. The service activities are the actual actions performed to service (repair) an object. Entity: Srv_Service_Activities

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [CompleteTime](Applications.Service.ServiceActivities.md#completetime) | datetime (nullable) | Exact time, when the document was last completed[Filter(ge;le)] 
| [CreationTime](Applications.Service.ServiceActivities.md#creationtime) | datetime | Date/Time when the document was created [Required][Filter(ge;le)] 
| [CreationUser](Applications.Service.ServiceActivities.md#creationuser) | string | The login name of the user, who created the document [Required][Filter(like)] 
| [CreditLimitOverride](Applications.Service.ServiceActivities.md#creditlimitoverride) | boolean | Specifies a value, which would be provided to SalesOrder.CreditLimitOverride, when generating SalesOrder. [Required] [Default(false)] [Filter(eq)] 
| [DeadlineTime](Applications.Service.ServiceActivities.md#deadlinetime) | datetime (nullable) | The deadline for the task. null if there is no deadline. [Filter(ge;le)] 
| [DocumentDate](Applications.Service.ServiceActivities.md#documentdate) | datetime | The date on which the document was issued [Required][Filter(eq;ge;le)][ORD] 
| [DocumentNo](Applications.Service.ServiceActivities.md#documentno) | string | Document number, unique within Document_Type_Id [Required][Filter(eq;like)][ORD] 
| [DocumentNotes](Applications.Service.ServiceActivities.md#documentnotes) | string (nullable) | Notes for this Document 
| [DocumentVersion](Applications.Service.ServiceActivities.md#documentversion) | int32 | [Filter(eq;ge;le)] 
| [EndTime](Applications.Service.ServiceActivities.md#endtime) | datetime (nullable) | Currently planned ending time of the task. [Filter(ge;le)] 
| [EntityName](Applications.Service.ServiceActivities.md#entityname) | string | The entity name of the document equal to the entity name of the document type.[Filter(eq)] [ORD] 
| [Id](Applications.Service.ServiceActivities.md#id) | guid |  
| [IsReleased](Applications.Service.ServiceActivities.md#isreleased) | boolean | True if the document is not void and its state is released or greater. [Required] [Default(false)] [Filter(eq)] [ReadOnly] 
| [IsSingleExecution](Applications.Service.ServiceActivities.md#issingleexecution) | boolean | Specifies whether the document is a single execution of its order document. [Required] [Default(false)] [Filter(eq)] [ReadOnly] 
| [Notes](Applications.Service.ServiceActivities.md#notes) | string (nullable) | Notes for this Activity. 
| [ParentDocument<br />RelationshipType](Applications.Service.ServiceActivities.md#parentdocumentrelationshiptype) | [ParentDocument<br />RelationshipType](Applications.Service.ServiceActivities.md#parentdocumentrelationshiptype) (nullable) | Type of relationship between the current document and the parent document(s). Affects the constraints for execution/completion for the documents. Possible values: 'S' = 'Subtask', 'N' = 'Next task'. 
| [PlannedDurationMinutes](Applications.Service.ServiceActivities.md#planneddurationminutes) | int32 (nullable) | Total planned duration of the activity, regardless of the current execution status. [Filter(ge;le)] 
| [PlanningOnly](Applications.Service.ServiceActivities.md#planningonly) | boolean (nullable) | Indicates that the document is used only for planning (and as consequence its state cannot be greater than Planned) [Required] 
| [Priority](Applications.Service.ServiceActivities.md#priority) | [Priority](Applications.Service.ServiceActivities.md#priority) | Priority on the scale from 1 (least important) to 5 (very important). [Required] [Default(3)] 
| [Private](Applications.Service.ServiceActivities.md#private) | boolean | True if the task is visible only to its owner; false if this is publicly visible task. [Required] [Default(false)] 
| [ReadOnly](Applications.Service.ServiceActivities.md#readonly) | boolean | True - the document is read only; false - the document is not read only [Required] 
| [ReceiverPersonName](Applications.Service.ServiceActivities.md#receiverpersonname) | string (nullable) | Copy of the name of the receiver at the time the activity was signed. [Filter(like)] 
| [ReferenceDate](Applications.Service.ServiceActivities.md#referencedate) | datetime (nullable) | The date to which this document refers, i.e. when the action really occurred. If null, Document_Date is taken [Filter(ge;le)] 
| [ReferenceDocumentNo](Applications.Service.ServiceActivities.md#referencedocumentno) | string (nullable) | The number of the document (issued by the other party), which was the reason for the creation of the current document. The numebr should be unique within the party documents [Filter(eq;like)] 
| [ReleaseTime](Applications.Service.ServiceActivities.md#releasetime) | datetime (nullable) | Exact time, when the document was first released [Filter(ge;le)] 
| [ReminderTime](Applications.Service.ServiceActivities.md#remindertime) | datetime (nullable) | When to snooze to the owner to remind him for the task. This default reminder is copied to and managed by the Reminders entity. 
| [StartTime](Applications.Service.ServiceActivities.md#starttime) | datetime | Currently planned starting time of the task. [Required] [Default(Now)] [Filter(ge;le)] 
| [State](Applications.Service.ServiceActivities.md#state) | [DocumentState](Applications.Service.ServiceActivities.md#state) | 0=New;5=Corrective;10=Computer Planned;20=Human Planned;30=Released;40=Completed;50=Closed [Required][Filter(eq;ge;le)] 
| [Subject](Applications.Service.ServiceActivities.md#subject) | string | Task primary subject (required). [Required] [Filter(eq;like)] 
| [SystemType](Applications.Service.ServiceActivities.md#systemtype) | [SystemType](Applications.Service.ServiceActivities.md#systemtype) | T=Task; C=Communication; M=Meeting. [Required] 
| [Void](Applications.Service.ServiceActivities.md#void) | boolean | True if the document is null and void [Required][Filter(eq)] 
| [VoidReason](Applications.Service.ServiceActivities.md#voidreason) | string (nullable) | Reason for voiding the document, entered by the user 
| [VoidTime](Applications.Service.ServiceActivities.md#voidtime) | datetime (nullable) | Date/time when the document has become void 
| [VoidUser](Applications.Service.ServiceActivities.md#voiduser) | string (nullable) | The user who voided the document 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [AccessKey](Applications.Service.ServiceActivities.md#accesskey) | [AccessKeys](Systems.Security.AccessKeys.md) (nullable) | The access key, containing the user permissions for this document. null means that all users have unlimited permissions |
| [AdjustedDocument](Applications.Service.ServiceActivities.md#adjusteddocument) | [Documents](General.Documents.md) (nullable) | The primary document, which the current document adjusts. null when this is not an adjustment document |
| [AssignedToUser](Applications.Service.ServiceActivities.md#assignedtouser) | [Users](Systems.Security.Users.md) (nullable) | The user to which this document is assigned for handling. null means that the document is not assigned to specific user |
| [ContactPerson](Applications.Service.ServiceActivities.md#contactperson) | [Persons](General.Contacts.Persons.md) (nullable) | The contact person, from the side of the Target Party. [Filter(multi eq)] |
| [CurrencyDirectory](Applications.Service.ServiceActivities.md#currencydirectory) | [CurrencyDirectories](General.CurrencyDirectories.md) (nullable) | The currency directory, containing all the convertion rates, used by the document. null means that the document does not need currency convertions |
| [Customer](Applications.Service.ServiceActivities.md#customer) | [Customers](Crm.Customers.md) | The receiver of the work. [Required] [Filter(multi eq)] |
| [DefaultServiceObject](Applications.Service.ServiceActivities.md#defaultserviceobject) | [ServiceObjects](Applications.Service.ServiceObjects.md) (nullable) | Default service object for materials and services lines. [Filter(multi eq)] |
| [DocumentType](Applications.Service.ServiceActivities.md#documenttype) | [DocumentTypes](General.DocumentTypes.md) | The user defined type of the document. Determines document behaviour, properties, additional amounts, validation, generations, etc. [Required] |
| [EnterpriseCompany](Applications.Service.ServiceActivities.md#enterprisecompany) | [EnterpriseCompanies](General.EnterpriseCompanies.md) | The enterprise company which issued the document [Required] |
| [EnterpriseCompanyLocation](Applications.Service.ServiceActivities.md#enterprisecompanylocation) | [CompanyLocations](General.Contacts.CompanyLocations.md) (nullable) | The enterprise company location which issued the document. null means that there is only one location within the enterprise company and locations are not used |
| [FromCompanyDivision](Applications.Service.ServiceActivities.md#fromcompanydivision) | [CompanyDivisions](General.Contacts.CompanyDivisions.md) (nullable) | The division of the company, issuing the document. null when the document is not issued by any specific division |
| [FromParty](Applications.Service.ServiceActivities.md#fromparty) | [Parties](General.Contacts.Parties.md) | The party which issued the document [Required] |
| [LocationPartyContact<br />Mechanism](Applications.Service.ServiceActivities.md#locationpartycontactmechanism) | [PartyContactMechanisms](General.Contacts.PartyContactMechanisms.md) (nullable) | The location where or the communication line used to conduct the work. [Filter(multi eq)] |
| [MasterDocument](Applications.Service.ServiceActivities.md#masterdocument) | [Documents](General.Documents.md) | In a multi-document tree, this is the root document, that created the whole tree. If this is the root it is equal to Id [Required] |
| [OwnerParty](Applications.Service.ServiceActivities.md#ownerparty) | [Parties](General.Contacts.Parties.md) | The party that owns the task. Initially this is the party that has created the task. [Required] [Filter(multi eq)] |
| [Parent](Applications.Service.ServiceActivities.md#parent) | [Documents](General.Documents.md) (nullable) | In a multi-document tree, this is the direct parent document. If this is the root it is null |
| [PrimeCauseDocument](Applications.Service.ServiceActivities.md#primecausedocument) | [Documents](General.Documents.md) (nullable) | The document that is the prime cause for creation of the current document |
| [ProjectTask](Applications.Service.ServiceActivities.md#projecttask) | [ProjectTasks](Projects.ProjectTasks.md) (nullable) | The project task for which the work is performed. null when the activity is not related to a project task. [Filter(multi eq)] |
| [ReceiverPerson](Applications.Service.ServiceActivities.md#receiverperson) | [Persons](General.Contacts.Persons.md) (nullable) | The id of the person from the customers company, that received and signed for the service. [Filter(multi eq)] |
| [ResponsibleParty](Applications.Service.ServiceActivities.md#responsibleparty) | [Parties](General.Contacts.Parties.md) | Who is responsible for executing the task. Initially this is the owner of the task. [Required] [Filter(multi eq)] |
| [ResponsiblePerson](Applications.Service.ServiceActivities.md#responsibleperson) | [Persons](General.Contacts.Persons.md) (nullable) | The person that is responsible for this order or transaction. It could be the sales person, the orderer, etc. |
| [ReverseOfDocument](Applications.Service.ServiceActivities.md#reverseofdocument) | [Documents](General.Documents.md) (nullable) | The document which the current document is reverse of |
| [Sequence](Applications.Service.ServiceActivities.md#sequence) | [Sequences](General.Sequences.md) (nullable) | The sequence that will be used to give new numbers to the documents of this type |
| [ServiceAgreement](Applications.Service.ServiceActivities.md#serviceagreement) | [ServiceAgreements](Applications.Service.ServiceAgreements.md) (nullable) | The service agreement under which the work was done. [Filter(multi eq)] |
| [ShipToCustomer](Applications.Service.ServiceActivities.md#shiptocustomer) | [Customers](Crm.Customers.md) (nullable) | Specific customer location of the main customer that receives the work. [Filter(multi eq)] |
| [Store](Applications.Service.ServiceActivities.md#store) | [Stores](Logistics.Inventory.Stores.md) (nullable) | The default store from which materials are taken. [Filter(multi eq)] |
| [TargetParty](Applications.Service.ServiceActivities.md#targetparty) | [Parties](General.Contacts.Parties.md) (nullable) | External participant or target of the task. [Filter(multi eq)] |
| [ToCompanyDivision](Applications.Service.ServiceActivities.md#tocompanydivision) | [CompanyDivisions](General.Contacts.CompanyDivisions.md) | The division of the company, receiving the document. null when the document is not received by any specific division |
| [ToParty](Applications.Service.ServiceActivities.md#toparty) | [Parties](General.Contacts.Parties.md) (nullable) | The party which should receive the document |
| [UserStatus](Applications.Service.ServiceActivities.md#userstatus) | [DocumentTypeUserStatuses](General.DocumentTypeUserStatuses.md) (nullable) | The user status of this document if applicable for this document type. null means unknown or not yet set |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Comments | [DocumentComments](General.DocumentComments.md) | List of [DocumentComment](General.DocumentComments.md) child objects, based on the [DocumentComment.Document](General.DocumentComments.md#document) back reference 
| DistributedAmounts | [DocumentDistributedAmounts](General.DocumentDistributedAmounts.md) | List of [DocumentDistributed<br />Amount](General.DocumentDistributedAmounts.md) child objects, based on the [DocumentDistributedAmount.Document](General.DocumentDistributedAmounts.md#document) back nce 
| DocumentAmounts | [DocumentAmounts](General.DocumentAmounts.md) |  
| FileAttachments | [DocumentFileAttachments](General.DocumentFileAttachments.md) | List of [DocumentFileAttachment](General.DocumentFileAttachments.md) child objects, based on the [DocumentFileAttachment.Document](General.DocumentFileAttachments.md#document) back reference 
| LineAmounts | [DocumentLineAmounts](General.DocumentLineAmounts.md) | List of [DocumentLineAmount](General.DocumentLineAmounts.md) child objects, based on the [DocumentLineAmount.Document](General.DocumentLineAmounts.md#document) back reference 
| Materials | [ServiceActivityMaterials](Applications.Service.ServiceActivityMaterials.md) | List of [ServiceActivityMaterial](Applications.Service.ServiceActivityMaterials.md) child objects, based on the [Applications.Service.ServiceActivityMaterial.ServiceActivity](Applications.Service.ServiceActivityMaterials.md#serviceactivity) back reference 
| Participants | [ActivityParticipants](General.Contacts.ActivityParticipants.md) | List of [ActivityParticipant](General.Contacts.ActivityParticipants.md) child objects, based on the [General.Contacts.ActivityParticipant.Activity](General.Contacts.ActivityParticipants.md#activity) back reference 
| Prints | [DocumentPrints](General.DocumentPrints.md) | List of [DocumentPrint](General.DocumentPrints.md) child objects, based on the [DocumentPrint.Document](General.DocumentPrints.md#document) back reference 
| Reminders | [Reminders](General.Contacts.Reminders.md) | List of [Reminder](General.Contacts.Reminders.md) child objects, based on the [General.Contacts.Reminder.Activity](General.Contacts.Reminders.md#activity) back reference 
| Resources | [ActivityResources](General.Contacts.ActivityResources.md) | List of [ActivityResource](General.Contacts.ActivityResources.md) child objects, based on the [General.Contacts.ActivityResource.Activity](General.Contacts.ActivityResources.md#activity) back reference 
| Services | [ServiceActivityServices](Applications.Service.ServiceActivityServices.md) | List of [ServiceActivityService](Applications.Service.ServiceActivityServices.md) child objects, based on the [Applications.Service.ServiceActivityService.ServiceActivity](Applications.Service.ServiceActivityServices.md#serviceactivity) back reference 
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

### CreditLimitOverride

Specifies a value, which would be provided to SalesOrder.CreditLimitOverride, when generating SalesOrder. [Required] [Default(false)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### DeadlineTime

The deadline for the task. null if there is no deadline. [Filter(ge;le)]

_Type_: **datetime (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
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

### EndTime

Currently planned ending time of the task. [Filter(ge;le)]

_Type_: **datetime (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

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

Notes for this Activity.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ParentDocumentRelationshipType

Type of relationship between the current document and the parent document(s). Affects the constraints for execution/completion for the documents. Possible values: 'S' = 'Subtask', 'N' = 'Next task'.

_Type_: **[ParentDocument<br />RelationshipType](Applications.Service.ServiceActivities.md#parentdocumentrelationshiptype) (nullable)**  
Relationship between parent and child documents  
_Allowed Values (General.ParentDocumentRelationshipType Enum Members)_  

| Value | Description |
| ---- | --- |
| Subtask | The child document is a sub-task of the parent document. (Complete child to complete parent) <br /> _Database Value:_ 'S' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Subtask' |
| NextTask | The child document is next task of the parent document. (Complete parent to complete child) <br /> _Database Value:_ 'N' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'NextTask' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### PlannedDurationMinutes

Total planned duration of the activity, regardless of the current execution status. [Filter(ge;le)]

_Type_: **int32 (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### PlanningOnly

Indicates that the document is used only for planning (and as consequence its state cannot be greater than Planned) [Required]

_Type_: **boolean (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### Priority

Priority on the scale from 1 (least important) to 5 (very important). [Required] [Default(3)]

_Type_: **[Priority](Applications.Service.ServiceActivities.md#priority)**  
Generic enum type for Priority properties  
_Allowed Values (General.Priority Enum Members)_  

| Value | Description |
| ---- | --- |
| Lowest | Lowest value. Stored as 1. <br /> _Database Value:_ 1 <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'Lowest' |
| Low | Low value. Stored as 2. <br /> _Database Value:_ 2 <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'Low' |
| Medium | Medium value. Stored as 3. <br /> _Database Value:_ 3 <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'Medium' |
| High | High value. Stored as 4. <br /> _Database Value:_ 4 <br /> _Model Value:_ 4 <br /> _Domain API Value:_ 'High' |
| Highest | Highest value. Stored as 5. <br /> _Database Value:_ 5 <br /> _Model Value:_ 5 <br /> _Domain API Value:_ 'Highest' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **3**  

### Private

True if the task is visible only to its owner; false if this is publicly visible task. [Required] [Default(false)]

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### ReadOnly

True - the document is read only; false - the document is not read only [Required]

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### ReceiverPersonName

Copy of the name of the receiver at the time the activity was signed. [Filter(like)]

_Type_: **string (nullable)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`obj.ReceiverPerson.PartyName`
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

### ReminderTime

When to snooze to the owner to remind him for the task. This default reminder is copied to and managed by the Reminders entity.

_Type_: **datetime (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### StartTime

Currently planned starting time of the task. [Required] [Default(Now)] [Filter(ge;le)]

_Type_: **datetime**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **CurrentDateTime**  

### State

0=New;5=Corrective;10=Computer Planned;20=Human Planned;30=Released;40=Completed;50=Closed [Required][Filter(eq;ge;le)]

_Type_: **[DocumentState](Applications.Service.ServiceActivities.md#state)**  
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

### Subject

Task primary subject (required). [Required] [Filter(eq;like)]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`GetSystemSubject( obj.SystemType, obj.TargetParty)`

### SystemType

T=Task; C=Communication; M=Meeting. [Required]

_Type_: **[SystemType](Applications.Service.ServiceActivities.md#systemtype)**  
Allowed values for the [SystemType](General.Contacts.Activities.md#systemtype) data attribute  
_Allowed Values (General.Contacts.ActivitiesRepository.SystemType Enum Members)_  

| Value | Description |
| ---- | --- |
| Communication | Communication value. Stored as 'C'. <br /> _Database Value:_ 'C' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Communication' |
| Meeting | Meeting value. Stored as 'M'. <br /> _Database Value:_ 'M' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'Meeting' |
| Task | Task value. Stored as 'T'. <br /> _Database Value:_ 'T' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'Task' |

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

### ContactPerson

The contact person, from the side of the Target Party. [Filter(multi eq)]

_Type_: **[Persons](General.Contacts.Persons.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### CurrencyDirectory

The currency directory, containing all the convertion rates, used by the document. null means that the document does not need currency convertions

_Type_: **[CurrencyDirectories](General.CurrencyDirectories.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### Customer

The receiver of the work. [Required] [Filter(multi eq)]

_Type_: **[Customers](Crm.Customers.md)**  
_Supported Filters_: **Equals, EqualsIn**  

_Front-End Recalc Expressions:_  
`obj.ShipToCustomer.DetermineCustomerFromShipToCustomer( obj.EnterpriseCompany, obj.Customer)`
### DefaultServiceObject

Default service object for materials and services lines. [Filter(multi eq)]

_Type_: **[ServiceObjects](Applications.Service.ServiceObjects.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

_Front-End Recalc Expressions:_  
`obj.Materials.Select( c => c.ServiceObject).Distinct( ).OnlyIfSingle( )`
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

### LocationPartyContactMechanism

The location where or the communication line used to conduct the work. [Filter(multi eq)]

_Type_: **[PartyContactMechanisms](General.Contacts.PartyContactMechanisms.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

_Front-End Recalc Expressions:_  
`obj.Customer.Party.DefaultContactMechanism`
### MasterDocument

In a multi-document tree, this is the root document, that created the whole tree. If this is the root it is equal to Id [Required]

_Type_: **[Documents](General.Documents.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### OwnerParty

The party that owns the task. Initially this is the party that has created the task. [Required] [Filter(multi eq)]

_Type_: **[Parties](General.Contacts.Parties.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### Parent

In a multi-document tree, this is the direct parent document. If this is the root it is null

_Type_: **[Documents](General.Documents.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### PrimeCauseDocument

The document that is the prime cause for creation of the current document

_Type_: **[Documents](General.Documents.md) (nullable)**  
_Supported Filters_: **EqualsIn**  

### ProjectTask

The project task for which the work is performed. null when the activity is not related to a project task. [Filter(multi eq)]

_Type_: **[ProjectTasks](Projects.ProjectTasks.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### ReceiverPerson

The id of the person from the customers company, that received and signed for the service. [Filter(multi eq)]

_Type_: **[Persons](General.Contacts.Persons.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### ResponsibleParty

Who is responsible for executing the task. Initially this is the owner of the task. [Required] [Filter(multi eq)]

_Type_: **[Parties](General.Contacts.Parties.md)**  
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

### ServiceAgreement

The service agreement under which the work was done. [Filter(multi eq)]

_Type_: **[ServiceAgreements](Applications.Service.ServiceAgreements.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### ShipToCustomer

Specific customer location of the main customer that receives the work. [Filter(multi eq)]

_Type_: **[Customers](Crm.Customers.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

_Front-End Recalc Expressions:_  
`obj.Customer.DetermineShipToCustomer( obj.EnterpriseCompany, obj.EnterpriseCompanyLocation, obj.ShipToCustomer)`
### Store

The default store from which materials are taken. [Filter(multi eq)]

_Type_: **[Stores](Logistics.Inventory.Stores.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

_Front-End Recalc Expressions:_  
`obj.Materials.Select( c => c.LineStore).Distinct( ).OnlyIfSingle( )`
### TargetParty

External participant or target of the task. [Filter(multi eq)]

_Type_: **[Parties](General.Contacts.Parties.md) (nullable)**  
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

[!list erp.entity=Applications.Service.ServiceActivities erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Applications.Service.ServiceActivities erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Applications.Service.ServiceActivities erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_Service_ServiceActivities?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_Service_ServiceActivities?$top=10>

