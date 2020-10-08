---
uid: Applications.Service.ServiceActivities
---
# Applications.Service.ServiceActivities

Contains service activity headers. The service activities are the actual actions performed to service (repair) an object. Entity: Srv_Service_Activities

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Applications.Service.ServiceActivities.md#Id) | guid |  
| [CompleteTime](Applications.Service.ServiceActivities.md#CompleteTime) | datetime (nullable) | Exact time, when the document was last completed[Filter(ge;le)] 
| [CreationTime](Applications.Service.ServiceActivities.md#CreationTime) | datetime | Date/Time when the document was created [Required][Filter(ge;le)] 
| [CreationUser](Applications.Service.ServiceActivities.md#CreationUser) | string | The login name of the user, who created the document [Required][Filter(like)] 
| [DocumentDate](Applications.Service.ServiceActivities.md#DocumentDate) | datetime | The date on which the document was issued [Required][Filter(eq;ge;le)][ORD] 
| [DocumentNo](Applications.Service.ServiceActivities.md#DocumentNo) | string | Document number, unique within Document_Type_Id [Required][Filter(eq;like)][ORD] 
| [DocumentVersion](Applications.Service.ServiceActivities.md#DocumentVersion) | int32 | [Filter(eq;ge;le)] 
| [DocumentNotes](Applications.Service.ServiceActivities.md#DocumentNotes) | string (nullable) | Notes for this Document 
| [ParentDocumentRelationshipType](Applications.Service.ServiceActivities.md#ParentDocumentRelationshipType) | [General.ParentDocumentRelationshipType](Applications.Service.ServiceActivities.md#ParentDocumentRelationshipType) (nullable) | Type of relationship between the current document and the parent document(s). Affects the constraints for execution/completion for the documents. Possible values: 'S' = 'Subtask', 'N' = 'Next task'. 
| [PlanningOnly](Applications.Service.ServiceActivities.md#PlanningOnly) | boolean (nullable) | Indicates that the document is used only for planning (and as consequence its state cannot be greater than Planned) [Required] 
| [ReadOnly](Applications.Service.ServiceActivities.md#ReadOnly) | boolean | True - the document is read only; false - the document is not read only [Required] 
| [ReferenceDate](Applications.Service.ServiceActivities.md#ReferenceDate) | datetime (nullable) | The date to which this document refers, i.e. when the action really occurred. If null, Document_Date is taken [Filter(ge;le)] 
| [ReferenceDocumentNo](Applications.Service.ServiceActivities.md#ReferenceDocumentNo) | string (nullable) | The number of the document (issued by the other party), which was the reason for the creation of the current document. The numebr should be unique within the party documents [Filter(eq;like)] 
| [ReleaseTime](Applications.Service.ServiceActivities.md#ReleaseTime) | datetime (nullable) | Exact time, when the document was first released [Filter(ge;le)] 
| [State](Applications.Service.ServiceActivities.md#State) | [General.DocumentState](Applications.Service.ServiceActivities.md#State) | 0=New;5=Corrective;10=Computer Planned;20=Human Planned;30=Released;40=Completed;50=Closed [Required][Filter(eq;ge;le)] 
| [Void](Applications.Service.ServiceActivities.md#Void) | boolean | True if the document is null and void [Required][Filter(eq)] 
| [VoidReason](Applications.Service.ServiceActivities.md#VoidReason) | string (nullable) | Reason for voiding the document, entered by the user 
| [VoidTime](Applications.Service.ServiceActivities.md#VoidTime) | datetime (nullable) | Date/time when the document has become void 
| [VoidUser](Applications.Service.ServiceActivities.md#VoidUser) | string (nullable) | The user who voided the document 
| [EntityName](Applications.Service.ServiceActivities.md#EntityName) | string | The entity name of the document equal to the entity name of the document type.[Filter(eq)] [ORD] 
| [DeadlineTime](Applications.Service.ServiceActivities.md#DeadlineTime) | datetime (nullable) | The deadline for the task. null if there is no deadline. [Filter(ge;le)] 
| [EndTime](Applications.Service.ServiceActivities.md#EndTime) | datetime (nullable) | Currently planned ending time of the task. [Filter(ge;le)] 
| [IsReleased](Applications.Service.ServiceActivities.md#IsReleased) | boolean | True if the document is not void and its state is released or greater. [Required] [Default(false)] [Filter(eq)] [ReadOnly] 
| [IsSingleExecution](Applications.Service.ServiceActivities.md#IsSingleExecution) | boolean | Specifies whether the document is a single execution of its order document. [Required] [Default(false)] [Filter(eq)] [ReadOnly] 
| [Notes](Applications.Service.ServiceActivities.md#Notes) | string (nullable) | Notes for this Activity. 
| [PlannedDurationMinutes](Applications.Service.ServiceActivities.md#PlannedDurationMinutes) | int32 (nullable) | Total planned duration of the activity, regardless of the current execution status. [Filter(ge;le)] 
| [Priority](Applications.Service.ServiceActivities.md#Priority) | [General.Priority](Applications.Service.ServiceActivities.md#Priority) | Priority on the scale from 1 (least important) to 5 (very important). [Required] [Default(3)] 
| [Private](Applications.Service.ServiceActivities.md#Private) | boolean | True if the task is visible only to its owner; false if this is publicly visible task. [Required] [Default(false)] 
| [ReminderTime](Applications.Service.ServiceActivities.md#ReminderTime) | datetime (nullable) | When to snooze to the owner to remind him for the task. This default reminder is copied to and managed by the Reminders entity. 
| [StartTime](Applications.Service.ServiceActivities.md#StartTime) | datetime | Currently planned starting time of the task. [Required] [Default(Now)] [Filter(ge;le)] 
| [Subject](Applications.Service.ServiceActivities.md#Subject) | string | Task primary subject (required). [Required] [Filter(eq;like)] 
| [SystemType](Applications.Service.ServiceActivities.md#SystemType) | [General.Contacts.ActivitiesRepository.SystemType](Applications.Service.ServiceActivities.md#SystemType) | T=Task; C=Communication; M=Meeting. [Required] 
| [CreditLimitOverride](Applications.Service.ServiceActivities.md#CreditLimitOverride) | boolean | Specifies a value, which would be provided to SalesOrder.CreditLimitOverride, when generating SalesOrder. [Required] [Default(false)] [Filter(eq)] 
| [ReceiverPersonName](Applications.Service.ServiceActivities.md#ReceiverPersonName) | string (nullable) | Copy of the name of the receiver at the time the activity was signed. [Filter(like)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [AccessKey](Applications.Service.ServiceActivities.md#AccessKey) | [Systems.Security.AccessKeys](Systems.Security.AccessKeys.md) (nullable) | The access key, containing the user permissions for this document. null means that all users have unlimited permissions |
| [AdjustedDocument](Applications.Service.ServiceActivities.md#AdjustedDocument) | [General.Documents](General.Documents.md) (nullable) | The primary document, which the current document adjusts. null when this is not an adjustment document |
| [AssignedToUser](Applications.Service.ServiceActivities.md#AssignedToUser) | [Systems.Security.Users](Systems.Security.Users.md) (nullable) | The user to which this document is assigned for handling. null means that the document is not assigned to specific user |
| [CurrencyDirectory](Applications.Service.ServiceActivities.md#CurrencyDirectory) | [General.CurrencyDirectories](General.CurrencyDirectories.md) (nullable) | The currency directory, containing all the convertion rates, used by the document. null means that the document does not need currency convertions |
| [DocumentType](Applications.Service.ServiceActivities.md#DocumentType) | [General.DocumentTypes](General.DocumentTypes.md) | The user defined type of the document. Determines document behaviour, properties, additional amounts, validation, generations, etc. [Required] |
| [EnterpriseCompany](Applications.Service.ServiceActivities.md#EnterpriseCompany) | [General.EnterpriseCompanies](General.EnterpriseCompanies.md) | The enterprise company which issued the document [Required] |
| [EnterpriseCompanyLocation](Applications.Service.ServiceActivities.md#EnterpriseCompanyLocation) | [General.Contacts.CompanyLocations](General.Contacts.CompanyLocations.md) (nullable) | The enterprise company location which issued the document. null means that there is only one location within the enterprise company and locations are not used |
| [FromCompanyDivision](Applications.Service.ServiceActivities.md#FromCompanyDivision) | [General.Contacts.CompanyDivisions](General.Contacts.CompanyDivisions.md) (nullable) | The division of the company, issuing the document. null when the document is not issued by any specific division |
| [FromParty](Applications.Service.ServiceActivities.md#FromParty) | [General.Contacts.Parties](General.Contacts.Parties.md) | The party which issued the document [Required] |
| [MasterDocument](Applications.Service.ServiceActivities.md#MasterDocument) | [General.Documents](General.Documents.md) | In a multi-document tree, this is the root document, that created the whole tree. If this is the root it is equal to Id [Required] |
| [Parent](Applications.Service.ServiceActivities.md#Parent) | [General.Documents](General.Documents.md) (nullable) | In a multi-document tree, this is the direct parent document. If this is the root it is null |
| [PrimeCauseDocument](Applications.Service.ServiceActivities.md#PrimeCauseDocument) | [General.Documents](General.Documents.md) (nullable) | The document that is the prime cause for creation of the current document |
| [ResponsiblePerson](Applications.Service.ServiceActivities.md#ResponsiblePerson) | [General.Contacts.Persons](General.Contacts.Persons.md) (nullable) | The person that is responsible for this order or transaction. It could be the sales person, the orderer, etc. |
| [ReverseOfDocument](Applications.Service.ServiceActivities.md#ReverseOfDocument) | [General.Documents](General.Documents.md) (nullable) | The document which the current document is reverse of |
| [Sequence](Applications.Service.ServiceActivities.md#Sequence) | [General.Sequences](General.Sequences.md) (nullable) | The sequence that will be used to give new numbers to the documents of this type |
| [ToCompanyDivision](Applications.Service.ServiceActivities.md#ToCompanyDivision) | [General.Contacts.CompanyDivisions](General.Contacts.CompanyDivisions.md) | The division of the company, receiving the document. null when the document is not received by any specific division |
| [ToParty](Applications.Service.ServiceActivities.md#ToParty) | [General.Contacts.Parties](General.Contacts.Parties.md) (nullable) | The party which should receive the document |
| [UserStatus](Applications.Service.ServiceActivities.md#UserStatus) | [General.DocumentTypeUserStatuses](General.DocumentTypeUserStatuses.md) (nullable) | The user status of this document if applicable for this document type. null means unknown or not yet set |
| [ContactPerson](Applications.Service.ServiceActivities.md#ContactPerson) | [General.Contacts.Persons](General.Contacts.Persons.md) (nullable) | The contact person, from the side of the Target Party. [Filter(multi eq)] |
| [OwnerParty](Applications.Service.ServiceActivities.md#OwnerParty) | [General.Contacts.Parties](General.Contacts.Parties.md) | The party that owns the task. Initially this is the party that has created the task. [Required] [Filter(multi eq)] |
| [ProjectTask](Applications.Service.ServiceActivities.md#ProjectTask) | [Projects.ProjectTasks](Projects.ProjectTasks.md) (nullable) | The project task for which the work is performed. null when the activity is not related to a project task. [Filter(multi eq)] |
| [ResponsibleParty](Applications.Service.ServiceActivities.md#ResponsibleParty) | [General.Contacts.Parties](General.Contacts.Parties.md) | Who is responsible for executing the task. Initially this is the owner of the task. [Required] [Filter(multi eq)] |
| [TargetParty](Applications.Service.ServiceActivities.md#TargetParty) | [General.Contacts.Parties](General.Contacts.Parties.md) (nullable) | External participant or target of the task. [Filter(multi eq)] |
| [Customer](Applications.Service.ServiceActivities.md#Customer) | [Crm.Customers](Crm.Customers.md) | The receiver of the work. [Required] [Filter(multi eq)] |
| [DefaultServiceObject](Applications.Service.ServiceActivities.md#DefaultServiceObject) | [Applications.Service.ServiceObjects](Applications.Service.ServiceObjects.md) (nullable) | Default service object for materials and services lines. [Filter(multi eq)] |
| [LocationPartyContactMechanism](Applications.Service.ServiceActivities.md#LocationPartyContactMechanism) | [General.Contacts.PartyContactMechanisms](General.Contacts.PartyContactMechanisms.md) (nullable) | The location where or the communication line used to conduct the work. [Filter(multi eq)] |
| [ReceiverPerson](Applications.Service.ServiceActivities.md#ReceiverPerson) | [General.Contacts.Persons](General.Contacts.Persons.md) (nullable) | The id of the person from the customers company, that received and signed for the service. [Filter(multi eq)] |
| [ServiceAgreement](Applications.Service.ServiceActivities.md#ServiceAgreement) | [Applications.Service.ServiceAgreements](Applications.Service.ServiceAgreements.md) (nullable) | The service agreement under which the work was done. [Filter(multi eq)] |
| [ShipToCustomer](Applications.Service.ServiceActivities.md#ShipToCustomer) | [Crm.Customers](Crm.Customers.md) (nullable) | Specific customer location of the main customer that receives the work. [Filter(multi eq)] |
| [Store](Applications.Service.ServiceActivities.md#Store) | [Logistics.Inventory.Stores](Logistics.Inventory.Stores.md) (nullable) | The default store from which materials are taken. [Filter(multi eq)] |

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
| Participants | [General.Contacts.ActivityParticipants](General.Contacts.ActivityParticipants.md) | List of [ActivityParticipant](General.Contacts.ActivityParticipants.md) child objects, based on the [General.Contacts.ActivityParticipant.Activity](General.Contacts.ActivityParticipants.md#Activity) back reference 
| Resources | [General.Contacts.ActivityResources](General.Contacts.ActivityResources.md) | List of [ActivityResource](General.Contacts.ActivityResources.md) child objects, based on the [General.Contacts.ActivityResource.Activity](General.Contacts.ActivityResources.md#Activity) back reference 
| Reminders | [General.Contacts.Reminders](General.Contacts.Reminders.md) | List of [Reminder](General.Contacts.Reminders.md) child objects, based on the [General.Contacts.Reminder.Activity](General.Contacts.Reminders.md#Activity) back reference 
| Materials | [Applications.Service.ServiceActivityMaterials](Applications.Service.ServiceActivityMaterials.md) | List of [ServiceActivityMaterial](Applications.Service.ServiceActivityMaterials.md) child objects, based on the [Applications.Service.ServiceActivityMaterial.ServiceActivity](Applications.Service.ServiceActivityMaterials.md#ServiceActivity) back reference 
| Services | [Applications.Service.ServiceActivityServices](Applications.Service.ServiceActivityServices.md) | List of [ServiceActivityService](Applications.Service.ServiceActivityServices.md) child objects, based on the [Applications.Service.ServiceActivityService.ServiceActivity](Applications.Service.ServiceActivityServices.md#ServiceActivity) back reference 


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

_Type_: **[General.ParentDocumentRelationshipType](Applications.Service.ServiceActivities.md#ParentDocumentRelationshipType) (nullable)**  
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

_Type_: **[General.DocumentState](Applications.Service.ServiceActivities.md#State)**  
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

### DeadlineTime

> The deadline for the task. null if there is no deadline. [Filter(ge;le)]

_Type_: **datetime (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### EndTime

> Currently planned ending time of the task. [Filter(ge;le)]

_Type_: **datetime (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
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

> Notes for this Activity.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### PlannedDurationMinutes

> Total planned duration of the activity, regardless of the current execution status. [Filter(ge;le)]

_Type_: **int32 (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### Priority

> Priority on the scale from 1 (least important) to 5 (very important). [Required] [Default(3)]

_Type_: **[General.Priority](Applications.Service.ServiceActivities.md#Priority)**  
Generic enum type for Priority properties  
_Allowed Values (Enum Members)_  

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

> True if the task is visible only to its owner; false if this is publicly visible task. [Required] [Default(false)]

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### ReminderTime

> When to snooze to the owner to remind him for the task. This default reminder is copied to and managed by the Reminders entity.

_Type_: **datetime (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### StartTime

> Currently planned starting time of the task. [Required] [Default(Now)] [Filter(ge;le)]

_Type_: **datetime**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **CurrentDateTime**  

### Subject

> Task primary subject (required). [Required] [Filter(eq;like)]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`GetSystemSubject(obj.SystemType, obj.TargetParty)`

### SystemType

> T=Task; C=Communication; M=Meeting. [Required]

_Type_: **[General.Contacts.ActivitiesRepository.SystemType](Applications.Service.ServiceActivities.md#SystemType)**  
Allowed values for the [SystemType](General.Contacts.Activities.md#SystemType) data attribute  
_Allowed Values (Enum Members)_  

| Value | Description |
| ---- | --- |
| Communication | Communication value. Stored as 'C'. <br /> _Database Value:_ 'C' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Communication' |
| Meeting | Meeting value. Stored as 'M'. <br /> _Database Value:_ 'M' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'Meeting' |
| Task | Task value. Stored as 'T'. <br /> _Database Value:_ 'T' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'Task' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### CreditLimitOverride

> Specifies a value, which would be provided to SalesOrder.CreditLimitOverride, when generating SalesOrder. [Required] [Default(false)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### ReceiverPersonName

> Copy of the name of the receiver at the time the activity was signed. [Filter(like)]

_Type_: **string (nullable)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`obj.ReceiverPerson.PartyName`

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

### ContactPerson

> The contact person, from the side of the Target Party. [Filter(multi eq)]

_Type_: **[General.Contacts.Persons](General.Contacts.Persons.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### OwnerParty

> The party that owns the task. Initially this is the party that has created the task. [Required] [Filter(multi eq)]

_Type_: **[General.Contacts.Parties](General.Contacts.Parties.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### ProjectTask

> The project task for which the work is performed. null when the activity is not related to a project task. [Filter(multi eq)]

_Type_: **[Projects.ProjectTasks](Projects.ProjectTasks.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### ResponsibleParty

> Who is responsible for executing the task. Initially this is the owner of the task. [Required] [Filter(multi eq)]

_Type_: **[General.Contacts.Parties](General.Contacts.Parties.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### TargetParty

> External participant or target of the task. [Filter(multi eq)]

_Type_: **[General.Contacts.Parties](General.Contacts.Parties.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Customer

> The receiver of the work. [Required] [Filter(multi eq)]

_Type_: **[Crm.Customers](Crm.Customers.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`obj.ShipToCustomer.DetermineCustomerFromShipToCustomer(obj.EnterpriseCompany, obj.Customer)`
### DefaultServiceObject

> Default service object for materials and services lines. [Filter(multi eq)]

_Type_: **[Applications.Service.ServiceObjects](Applications.Service.ServiceObjects.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`obj.Materials.Select(c => c.ServiceObject).Distinct().OnlyIfSingle()`
### LocationPartyContactMechanism

> The location where or the communication line used to conduct the work. [Filter(multi eq)]

_Type_: **[General.Contacts.PartyContactMechanisms](General.Contacts.PartyContactMechanisms.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`obj.Customer.Party.DefaultContactMechanism`
### ReceiverPerson

> The id of the person from the customers company, that received and signed for the service. [Filter(multi eq)]

_Type_: **[General.Contacts.Persons](General.Contacts.Persons.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### ServiceAgreement

> The service agreement under which the work was done. [Filter(multi eq)]

_Type_: **[Applications.Service.ServiceAgreements](Applications.Service.ServiceAgreements.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### ShipToCustomer

> Specific customer location of the main customer that receives the work. [Filter(multi eq)]

_Type_: **[Crm.Customers](Crm.Customers.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`obj.Customer.DetermineShipToCustomer(obj.EnterpriseCompany, obj.EnterpriseCompanyLocation, obj.ShipToCustomer)`
### Store

> The default store from which materials are taken. [Filter(multi eq)]

_Type_: **[Logistics.Inventory.Stores](Logistics.Inventory.Stores.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`obj.Materials.Select(c => c.LineStore).Distinct().OnlyIfSingle()`


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

