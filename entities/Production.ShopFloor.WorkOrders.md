---
uid: Production.ShopFloor.WorkOrders
---
# Production.ShopFloor.WorkOrders Entity

Scheduled and released production orders. Each order can contain the production of many items. Entity: Prd_Work_Orders

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [AdjustmentNumber](Production.ShopFloor.WorkOrders.md#adjustmentnumber) | int32 | Consecutive number of the correction that this document is applying to the adjusted document. [Required] [Default(0)] [ReadOnly] 
| [AdjustmentTime](Production.ShopFloor.WorkOrders.md#adjustmenttime) | datetime (nullable) | Date/time when the document last has been adjusted by corrective document. [ReadOnly] 
| [AdjustmentUser](Production.ShopFloor.WorkOrders.md#adjustmentuser) | string (nullable) | The user who adjusted the document. [ReadOnly] 
| [CompleteTime](Production.ShopFloor.WorkOrders.md#completetime) | datetime (nullable) | Date and time when the document was completed (State set to Completed). [Filter(ge;le)] [ReadOnly] 
| [CompletionDate](Production.ShopFloor.WorkOrders.md#completiondate) | datetime (nullable) | Scheduled date of completion. Specifies the date when the workorder was completed. null means that the order is not yet completed. 
| [CreationTime](Production.ShopFloor.WorkOrders.md#creationtime) | datetime | Date/Time when the document was created. [Required] [Default(Now)] [Filter(ge;le)] [ReadOnly] 
| [CreationUser](Production.ShopFloor.WorkOrders.md#creationuser) | string | The login name of the user, who created the document. [Required] [Filter(like)] [ReadOnly] 
| [DocumentDate](Production.ShopFloor.WorkOrders.md#documentdate) | date | The date on which the document was issued. [Required] [Default(Today)] [Filter(eq;ge;le)] [ORD] 
| [DocumentNo](Production.ShopFloor.WorkOrders.md#documentno) | string | Document number, unique within Document_Type_Id. [Required] [Filter(eq;like)] [ORD] 
| [DocumentNotes](Production.ShopFloor.WorkOrders.md#documentnotes) | string (nullable) | Notes for this Document. 
| [DocumentVersion](Production.ShopFloor.WorkOrders.md#documentversion) | int32 | Consecutive version number, starting with 1. Each update produces a new version of the document. [Required] [Default(1)] [Filter(eq;ge;le)] [ReadOnly] 
| [DueDate](Production.ShopFloor.WorkOrders.md#duedate) | datetime (nullable) | The final due date, when the production should be ready. 
| [DurationHour](Production.ShopFloor.WorkOrders.md#durationhour) | decimal | The duration of all operations in the protocol either planned (for planned orders) or actual (for completed orders). [Required] [Default(0)] 
| [EntityName](Production.ShopFloor.WorkOrders.md#entityname) | string | The entity name of the document header. [Required] [Filter(eq)] [ORD] [ReadOnly] 
| [Id](Production.ShopFloor.WorkOrders.md#id) | guid |  
| [IsReleased](Production.ShopFloor.WorkOrders.md#isreleased) | boolean | True if the document is not void and its state is released or greater. [Required] [Default(false)] [Filter(eq)] [ReadOnly] 
| [IsSingleExecution](Production.ShopFloor.WorkOrders.md#issingleexecution) | boolean | Specifies whether the document is a single execution of its order document. [Required] [Default(false)] [Filter(eq)] [ReadOnly] 
| [Notes](Production.ShopFloor.WorkOrders.md#notes) | string (nullable) | User notes for the production order. 
| [ParentDocument<br />RelationshipType](Production.ShopFloor.WorkOrders.md#parentdocumentrelationshiptype) | [ParentDocument<br />RelationshipType](Production.ShopFloor.WorkOrders.md#parentdocumentrelationshiptype) (nullable) | Type of relationship between the current document and the parent document(s). Affects the constraints for execution/completion for the documents. Possible values: 'S' = 'Subtask', 'N' = 'Next task'. [ReadOnly] 
| [PlanningOnly](Production.ShopFloor.WorkOrders.md#planningonly) | boolean | Indicates that the document is used only for planning (and as consequence its state cannot be greater than Planned). [Required] [Default(false)] [ReadOnly] 
| [Priority](Production.ShopFloor.WorkOrders.md#priority) | [Priority](Production.ShopFloor.WorkOrders.md#priority) | Priority of the work order. Higher priority orders might seize resources from lower priority orders. 1=Lowest priority ... 5=Highest. [Required] [Default(3)] [Filter(ge;le)] 
| [ReadOnly](Production.ShopFloor.WorkOrders.md#readonly) | boolean | True - the document is read only; false - the document is not read only. [Required] [Default(false)] [ReadOnly] 
| [ReferenceDate](Production.ShopFloor.WorkOrders.md#referencedate) | datetime (nullable) | The date to which this document refers, i.e. when the action really occurred. If null, Document_Date is taken. [Default(Today)] [Filter(ge;le)] 
| [ReferenceDocumentNo](Production.ShopFloor.WorkOrders.md#referencedocumentno) | string (nullable) | The number of the document (issued by the other party), which was the reason for the creation of the current document. The numebr should be unique within the party documents. [Filter(eq;like)] 
| [ReleaseDate](Production.ShopFloor.WorkOrders.md#releasedate) | datetime (nullable) | Scheduled release date. Specifies the date when the order is planned/released to production. null means that still there is no plan for releasing the order. 
| [ReleaseTime](Production.ShopFloor.WorkOrders.md#releasetime) | datetime (nullable) | Date and time when the document was released (State set to Released). [Filter(ge;le)] [ReadOnly] 
| [State](Production.ShopFloor.WorkOrders.md#state) | [DocumentState](Production.ShopFloor.WorkOrders.md#state) | The current system state of the document. Allowed values: 0=New;5=Corrective;10=Computer Planned;20=Human Planned;30=Released;40=Completed;50=Closed. [Required] [Default(0)] [Filter(multi eq;ge;le)] [ReadOnly] 
| [Void](Production.ShopFloor.WorkOrders.md#void) | boolean | True if the document is null and void. [Required] [Default(false)] [Filter(eq)] [ReadOnly] 
| [VoidReason](Production.ShopFloor.WorkOrders.md#voidreason) | string (nullable) | Reason for voiding the document, entered by the user. [ReadOnly] 
| [VoidTime](Production.ShopFloor.WorkOrders.md#voidtime) | datetime (nullable) | Date/time when the document has become void. [ReadOnly] 
| [VoidUser](Production.ShopFloor.WorkOrders.md#voiduser) | string (nullable) | The user who voided the document. [ReadOnly] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [AccessKey](Production.ShopFloor.WorkOrders.md#accesskey) | [AccessKeys](Systems.Security.AccessKeys.md) (nullable) | The access key, containing the user permissions for this document. null means that all users have unlimited permissions. [Filter(multi eq)] |
| [AdjustedDocument](Production.ShopFloor.WorkOrders.md#adjusteddocument) | [Documents](General.Documents.md) (nullable) | The primary document, which the current document adjusts. null when this is not an adjustment document. [Filter(multi eq)] [ReadOnly] |
| [AssignedToUser](Production.ShopFloor.WorkOrders.md#assignedtouser) | [Users](Systems.Security.Users.md) (nullable) | The user to which this document is assigned for handling. null means that the document is not assigned to specific user. [Filter(multi eq)] |
| [CurrencyDirectory](Production.ShopFloor.WorkOrders.md#currencydirectory) | [CurrencyDirectories](General.CurrencyDirectories.md) (nullable) | The currency directory, containing all the convertion rates, used by the document. null means that the document does not need currency convertions. [Filter(multi eq)] |
| [DefaultMaterialsStore](Production.ShopFloor.WorkOrders.md#defaultmaterialsstore) | [Stores](Logistics.Inventory.Stores.md) (nullable) | Default materials store for the ingredients. [Filter(multi eq)] |
| [DefaultOutputStore](Production.ShopFloor.WorkOrders.md#defaultoutputstore) | [Stores](Logistics.Inventory.Stores.md) (nullable) | Default output store for the finished products. [Filter(multi eq)] |
| [DocumentType](Production.ShopFloor.WorkOrders.md#documenttype) | [DocumentTypes](General.DocumentTypes.md) | The user defined type of the document. Determines document behaviour, properties, additional amounts, validation, generations, etc. [Required] [Filter(multi eq)] |
| [EnterpriseCompany](Production.ShopFloor.WorkOrders.md#enterprisecompany) | [EnterpriseCompanies](General.EnterpriseCompanies.md) | The enterprise company which issued the document. [Required] [Filter(multi eq)] |
| [EnterpriseCompanyLocation](Production.ShopFloor.WorkOrders.md#enterprisecompanylocation) | [CompanyLocations](General.Contacts.CompanyLocations.md) (nullable) | The enterprise company location which issued the document. null means that there is only one location within the enterprise company and locations are not used. [Filter(multi eq)] |
| [FromCompanyDivision](Production.ShopFloor.WorkOrders.md#fromcompanydivision) | [CompanyDivisions](General.Contacts.CompanyDivisions.md) (nullable) | The division of the company, issuing the document. null when the document is not issued by any specific division. [Filter(multi eq)] |
| [FromParty](Production.ShopFloor.WorkOrders.md#fromparty) | [Parties](General.Contacts.Parties.md) | The party which issued the document. [Required] [Filter(multi eq)] |
| [MasterDocument](Production.ShopFloor.WorkOrders.md#masterdocument) | [Documents](General.Documents.md) | In a multi-document tree, this is the root document, that created the whole tree. If this is the root it is equal to Id. [Required] [Filter(multi eq)] |
| [Parent](Production.ShopFloor.WorkOrders.md#parent) | [Documents](General.Documents.md) (nullable) | In a multi-document tree, this is the direct parent document. If this is the root it is null. [Filter(multi eq)] |
| [PrimeCauseDocument](Production.ShopFloor.WorkOrders.md#primecausedocument) | [Documents](General.Documents.md) (nullable) | The document that is the prime cause for creation of the current document. [Filter(multi eq)] |
| [ResponsiblePerson](Production.ShopFloor.WorkOrders.md#responsibleperson) | [Persons](General.Contacts.Persons.md) (nullable) | The person that is responsible for this order or transaction. It could be the sales person, the orderer, etc. [Filter(multi eq)] |
| [ReverseOfDocument](Production.ShopFloor.WorkOrders.md#reverseofdocument) | [Documents](General.Documents.md) (nullable) | The document which the current document is reverse of. [Filter(multi eq)] [ReadOnly] |
| [Sequence](Production.ShopFloor.WorkOrders.md#sequence) | [Sequences](General.Sequences.md) (nullable) | The sequence that will be used to give new numbers to the documents of this type. [Filter(multi eq)] [ReadOnly] |
| [ToCompanyDivision](Production.ShopFloor.WorkOrders.md#tocompanydivision) | [CompanyDivisions](General.Contacts.CompanyDivisions.md) (nullable) | The division of the company, receiving the document. null when the document is not received by any specific division. [Filter(multi eq)] |
| [ToParty](Production.ShopFloor.WorkOrders.md#toparty) | [Parties](General.Contacts.Parties.md) (nullable) | The party which should receive the document. [Filter(multi eq)] |
| [UserStatus](Production.ShopFloor.WorkOrders.md#userstatus) | [DocumentTypeUserStatuses](General.DocumentTypeUserStatuses.md) (nullable) | The user status of this document if applicable for this document type. null means unknown or not yet set. [Filter(multi eq)] [ReadOnly] |
| [Workgroup](Production.ShopFloor.WorkOrders.md#workgroup) | [Workgroups](Production.Resources.Workgroups.md) (nullable) | The workgroup which performs the operations. [Filter(multi eq)] |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Comments | [DocumentComments](General.DocumentComments.md) | List of [DocumentComment](General.DocumentComments.md) child objects, based on the [General.DocumentComment.Document](General.DocumentComments.md#document) back reference 
| DistributedAmounts | [DocumentDistributedAmounts](General.DocumentDistributedAmounts.md) | List of [DocumentDistributed<br />Amount](General.DocumentDistributedAmounts.md) child objects, based on the [General.DocumentDistributedAmount.Document](General.DocumentDistributedAmounts.md#document) back reference 
| DocumentAmounts | [DocumentAmounts](General.DocumentAmounts.md) | List of [DocumentAmount](General.DocumentAmounts.md) child objects, based on the [General.DocumentAmount.Document](General.DocumentAmounts.md#document) back reference 
| FileAttachments | [DocumentFileAttachments](General.DocumentFileAttachments.md) | List of [DocumentFileAttachment](General.DocumentFileAttachments.md) child objects, based on the [General.DocumentFileAttachment.Document](General.DocumentFileAttachments.md#document) back reference 
| ItemIngredients | [WorkOrderItemIngredients](Production.ShopFloor.WorkOrderItemIngredients.md) | List of [WorkOrderItemIngredient](Production.ShopFloor.WorkOrderItemIngredients.md) child objects, based on the [Production.ShopFloor.WorkOrderItemIngredient.WorkOrder](Production.ShopFloor.WorkOrderItemIngredients.md#workorder) back reference 
| Items | [WorkOrderItems](Production.ShopFloor.WorkOrderItems.md) | List of [WorkOrderItem](Production.ShopFloor.WorkOrderItems.md) child objects, based on the [Production.ShopFloor.WorkOrderItem.WorkOrder](Production.ShopFloor.WorkOrderItems.md#workorder) back reference 
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

### CompletionDate

Scheduled date of completion. Specifies the date when the workorder was completed. null means that the order is not yet completed.

_Type_: **datetime (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`obj.Items.Select( c => WorkOrderItemsRepository.CompletionDateAttribute.GetUntypedValue( c, False)).Distinct( ).OnlyIfSingle( )`
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

### DueDate

The final due date, when the production should be ready.

_Type_: **datetime (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### DurationHour

The duration of all operations in the protocol either planned (for planned orders) or actual (for completed orders). [Required] [Default(0)]

_Type_: **decimal**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### EntityName

The entity name of the document header. [Required] [Filter(eq)] [ORD] [ReadOnly]

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

User notes for the production order.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ParentDocumentRelationshipType

Type of relationship between the current document and the parent document(s). Affects the constraints for execution/completion for the documents. Possible values: 'S' = 'Subtask', 'N' = 'Next task'. [ReadOnly]

_Type_: **[ParentDocument<br />RelationshipType](Production.ShopFloor.WorkOrders.md#parentdocumentrelationshiptype) (nullable)**  
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

### Priority

Priority of the work order. Higher priority orders might seize resources from lower priority orders. 1=Lowest priority ... 5=Highest. [Required] [Default(3)] [Filter(ge;le)]

_Type_: **[Priority](Production.ShopFloor.WorkOrders.md#priority)**  
Allowed values for the [Priority](Production.ShopFloor.WorkOrders.md#priority) data attribute  
_Allowed Values (Production.ShopFloor.WorkOrdersRepository.Priority Enum Members)_  

| Value | Description |
| ---- | --- |
| Lowest | Lowest value. Stored as 1. <br /> _Database Value:_ 1 <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'Lowest' |
| Two | Two value. Stored as 2. <br /> _Database Value:_ 2 <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'Two' |
| Three | Three value. Stored as 3. <br /> _Database Value:_ 3 <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'Three' |
| Four | Four value. Stored as 4. <br /> _Database Value:_ 4 <br /> _Model Value:_ 4 <br /> _Domain API Value:_ 'Four' |
| Highest | Highest value. Stored as 5. <br /> _Database Value:_ 5 <br /> _Model Value:_ 5 <br /> _Domain API Value:_ 'Highest' |

_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **3**  

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

### ReleaseDate

Scheduled release date. Specifies the date when the order is planned/released to production. null means that still there is no plan for releasing the order.

_Type_: **datetime (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`obj.Items.Select( c => WorkOrderItemsRepository.ReleaseDateAttribute.GetUntypedValue( c, False)).Distinct( ).OnlyIfSingle( )`
### ReleaseTime

Date and time when the document was released (State set to Released). [Filter(ge;le)] [ReadOnly]

_Type_: **datetime (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### State

The current system state of the document. Allowed values: 0=New;5=Corrective;10=Computer Planned;20=Human Planned;30=Released;40=Completed;50=Closed. [Required] [Default(0)] [Filter(multi eq;ge;le)] [ReadOnly]

_Type_: **[DocumentState](Production.ShopFloor.WorkOrders.md#state)**  
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

### DefaultMaterialsStore

Default materials store for the ingredients. [Filter(multi eq)]

_Type_: **[Stores](Logistics.Inventory.Stores.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

_Front-End Recalc Expressions:_  
`obj.ItemIngredients.Select( c => c.Store).Distinct( ).OnlyIfSingle( )`
### DefaultOutputStore

Default output store for the finished products. [Filter(multi eq)]

_Type_: **[Stores](Logistics.Inventory.Stores.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

_Front-End Recalc Expressions:_  
`obj.Items.Select( c => c.OutputStore).Distinct( ).OnlyIfSingle( )`
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

### Workgroup

The workgroup which performs the operations. [Filter(multi eq)]

_Type_: **[Workgroups](Production.Resources.Workgroups.md) (nullable)**  
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

[!list erp.entity=Production.ShopFloor.WorkOrders erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Production.ShopFloor.WorkOrders erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Production.ShopFloor.WorkOrders erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Production_ShopFloor_WorkOrders?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Production_ShopFloor_WorkOrders?$top=10>

