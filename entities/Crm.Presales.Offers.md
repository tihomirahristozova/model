---
uid: Crm.Presales.Offers
---
# Crm.Presales.Offers Entity

Offers (quotes) for sales of products. Can contain variants and choice groups. The user can select some approved lines and generate Sales Order. Entity: Crm_Offers

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [AcceptedOn](Crm.Presales.Offers.md#acceptedon) | datetime (nullable) | The date on which the customer accepted the offer. null if the offer is not yet accepted or the date is unknown. 
| [CompleteTime](Crm.Presales.Offers.md#completetime) | datetime (nullable) | Exact time, when the document was last completed[Filter(ge;le)] 
| [CreationTime](Crm.Presales.Offers.md#creationtime) | datetime | Date/Time when the document was created [Required][Filter(ge;le)] 
| [CreationUser](Crm.Presales.Offers.md#creationuser) | string | The login name of the user, who created the document [Required][Filter(like)] 
| [DocumentDate](Crm.Presales.Offers.md#documentdate) | datetime | The date on which the document was issued [Required][Filter(eq;ge;le)][ORD] 
| [DocumentNo](Crm.Presales.Offers.md#documentno) | string | Document number, unique within Document_Type_Id [Required][Filter(eq;like)][ORD] 
| [DocumentNotes](Crm.Presales.Offers.md#documentnotes) | string (nullable) | Notes for this Document 
| [DocumentVersion](Crm.Presales.Offers.md#documentversion) | int32 | [Filter(eq;ge;le)] 
| [EntityName](Crm.Presales.Offers.md#entityname) | string | The entity name of the document equal to the entity name of the document type.[Filter(eq)] [ORD] 
| [Id](Crm.Presales.Offers.md#id) | guid |  
| [IsReleased](Crm.Presales.Offers.md#isreleased) | boolean | True if the document is not void and its state is released or greater. [Required] [Default(false)] [Filter(eq)] [ReadOnly] 
| [IsSingleExecution](Crm.Presales.Offers.md#issingleexecution) | boolean | Specifies whether the document is a single execution of its order document. [Required] [Default(false)] [Filter(eq)] [ReadOnly] 
| [Notes](Crm.Presales.Offers.md#notes) | string (nullable) | Notes for this Offer. 
| [ParentDocument<br />RelationshipType](Crm.Presales.Offers.md#parentdocumentrelationshiptype) | [ParentDocument<br />RelationshipType](Crm.Presales.Offers.md#parentdocumentrelationshiptype) (nullable) | Type of relationship between the current document and the parent document(s). Affects the constraints for execution/completion for the documents. Possible values: 'S' = 'Subtask', 'N' = 'Next task'. 
| [PaymentDueDate](Crm.Presales.Offers.md#paymentduedate) | datetime (nullable) | The last term for payment. 
| [PlanningOnly](Crm.Presales.Offers.md#planningonly) | boolean (nullable) | Indicates that the document is used only for planning (and as consequence its state cannot be greater than Planned) [Required] 
| [ReadOnly](Crm.Presales.Offers.md#readonly) | boolean | True - the document is read only; false - the document is not read only [Required] 
| [ReferenceDate](Crm.Presales.Offers.md#referencedate) | datetime (nullable) | The date to which this document refers, i.e. when the action really occurred. If null, Document_Date is taken [Filter(ge;le)] 
| [ReferenceDocumentNo](Crm.Presales.Offers.md#referencedocumentno) | string (nullable) | The number of the document (issued by the other party), which was the reason for the creation of the current document. The numebr should be unique within the party documents [Filter(eq;like)] 
| [ReleaseTime](Crm.Presales.Offers.md#releasetime) | datetime (nullable) | Exact time, when the document was first released [Filter(ge;le)] 
| [RequiredDeliveryDate](Crm.Presales.Offers.md#requireddeliverydate) | date (nullable) | When not null, specifies required delivery date for all offer lines. When the lines contain different delivery dates, this is null. 
| [State](Crm.Presales.Offers.md#state) | [DocumentState](Crm.Presales.Offers.md#state) | 0=New;5=Corrective;10=Computer Planned;20=Human Planned;30=Released;40=Completed;50=Closed [Required][Filter(eq;ge;le)] 
| [ValidTill](Crm.Presales.Offers.md#validtill) | datetime (nullable) | Last date when the offer is valid. null means the offer has no specific validity date. [Filter(ge;le)] 
| [Void](Crm.Presales.Offers.md#void) | boolean | True if the document is null and void [Required][Filter(eq)] 
| [VoidReason](Crm.Presales.Offers.md#voidreason) | string (nullable) | Reason for voiding the document, entered by the user 
| [VoidTime](Crm.Presales.Offers.md#voidtime) | datetime (nullable) | Date/time when the document has become void 
| [VoidUser](Crm.Presales.Offers.md#voiduser) | string (nullable) | The user who voided the document 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [AccessKey](Crm.Presales.Offers.md#accesskey) | [AccessKeys](Systems.Security.AccessKeys.md) (nullable) | The access key, containing the user permissions for this document. null means that all users have unlimited permissions |
| [AdjustedDocument](Crm.Presales.Offers.md#adjusteddocument) | [Documents](General.Documents.md) (nullable) | The primary document, which the current document adjusts. null when this is not an adjustment document |
| [AssignedToUser](Crm.Presales.Offers.md#assignedtouser) | [Users](Systems.Security.Users.md) (nullable) | The user to which this document is assigned for handling. null means that the document is not assigned to specific user |
| [CurrencyDirectory](Crm.Presales.Offers.md#currencydirectory) | [CurrencyDirectories](General.CurrencyDirectories.md) (nullable) | The currency directory, containing all the convertion rates, used by the document. null means that the document does not need currency convertions |
| [Customer](Crm.Presales.Offers.md#customer) | [Customers](Crm.Customers.md) | The customer to which the products are offered. [Required] [Filter(multi eq)] |
| [Deal](Crm.Presales.Offers.md#deal) | [Deals](Crm.Presales.Deals.md) (nullable) | The opportunity (deal) on which this offer is based. [Filter(multi eq)] |
| [DocumentCurrency](Crm.Presales.Offers.md#documentcurrency) | [Currencies](General.Currencies.md) | The currency in which the document is issued. All amounts are in this currency. [Required] [Filter(multi eq)] |
| [DocumentType](Crm.Presales.Offers.md#documenttype) | [DocumentTypes](General.DocumentTypes.md) | The user defined type of the document. Determines document behaviour, properties, additional amounts, validation, generations, etc. [Required] |
| [EnterpriseCompany](Crm.Presales.Offers.md#enterprisecompany) | [EnterpriseCompanies](General.EnterpriseCompanies.md) | The enterprise company which issued the document [Required] |
| [EnterpriseCompanyLocation](Crm.Presales.Offers.md#enterprisecompanylocation) | [CompanyLocations](General.Contacts.CompanyLocations.md) (nullable) | The enterprise company location which issued the document. null means that there is only one location within the enterprise company and locations are not used |
| [FromCompanyDivision](Crm.Presales.Offers.md#fromcompanydivision) | [CompanyDivisions](General.Contacts.CompanyDivisions.md) (nullable) | The division of the company, issuing the document. null when the document is not issued by any specific division |
| [FromParty](Crm.Presales.Offers.md#fromparty) | [Parties](General.Contacts.Parties.md) | The party which issued the document [Required] |
| [MasterDocument](Crm.Presales.Offers.md#masterdocument) | [Documents](General.Documents.md) | In a multi-document tree, this is the root document, that created the whole tree. If this is the root it is equal to Id [Required] |
| [Parent](Crm.Presales.Offers.md#parent) | [Documents](General.Documents.md) (nullable) | In a multi-document tree, this is the direct parent document. If this is the root it is null |
| [PaymentType](Crm.Presales.Offers.md#paymenttype) | [PaymentTypes](Finance.Payments.PaymentTypes.md) (nullable) | Way of payment. null means that no specific way of payment was offered. [Filter(multi eq)] |
| [PriceList](Crm.Presales.Offers.md#pricelist) | [PriceLists](Crm.PriceLists.md) (nullable) | The price list, based on which the prices are selected. Initially copied from the definition of the Customer. [Filter(multi eq)] |
| [PrimeCauseDocument](Crm.Presales.Offers.md#primecausedocument) | [Documents](General.Documents.md) (nullable) | The document that is the prime cause for creation of the current document |
| [RecipientPerson](Crm.Presales.Offers.md#recipientperson) | [Persons](General.Contacts.Persons.md) (nullable) | The offer recipient. It should be employee of the customer. null means that there is no default recipient or he/she is unknown. [Filter(multi eq)] |
| [ResponsiblePerson](Crm.Presales.Offers.md#responsibleperson) | [Persons](General.Contacts.Persons.md) (nullable) | The person that is responsible for this order or transaction. It could be the sales person, the orderer, etc. |
| [ReverseOfDocument](Crm.Presales.Offers.md#reverseofdocument) | [Documents](General.Documents.md) (nullable) | The document which the current document is reverse of |
| [SalesPerson](Crm.Presales.Offers.md#salesperson) | [SalesPersons](Crm.SalesPersons.md) (nullable) | Responsible sales person. null when no sales person was assigned. [Filter(multi eq)] |
| [Sequence](Crm.Presales.Offers.md#sequence) | [Sequences](General.Sequences.md) (nullable) | The sequence that will be used to give new numbers to the documents of this type |
| [ShipToCustomer](Crm.Presales.Offers.md#shiptocustomer) | [Customers](Crm.Customers.md) (nullable) | The customer to whom to ship the sales order. Usually it is a customer entry for a sub-party of the primary customer. [Filter(multi eq)] |
| [Store](Crm.Presales.Offers.md#store) | [Stores](Logistics.Inventory.Stores.md) (nullable) | The store, from which the products will be sold. When null, the store is unknown or N/A. [Filter(multi eq)] |
| [ToCompanyDivision](Crm.Presales.Offers.md#tocompanydivision) | [CompanyDivisions](General.Contacts.CompanyDivisions.md) | The division of the company, receiving the document. null when the document is not received by any specific division |
| [ToParty](Crm.Presales.Offers.md#toparty) | [Parties](General.Contacts.Parties.md) (nullable) | The party which should receive the document |
| [UserStatus](Crm.Presales.Offers.md#userstatus) | [DocumentTypeUserStatuses](General.DocumentTypeUserStatuses.md) (nullable) | The user status of this document if applicable for this document type. null means unknown or not yet set |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Comments | [DocumentComments](General.DocumentComments.md) | List of [DocumentComment](General.DocumentComments.md) child objects, based on the [DocumentComment.Document](General.DocumentComments.md#document) back reference 
| DistributedAmounts | [DocumentDistributedAmounts](General.DocumentDistributedAmounts.md) | List of [DocumentDistributed<br />Amount](General.DocumentDistributedAmounts.md) child objects, based on the [DocumentDistributedAmount.Document](General.DocumentDistributedAmounts.md#document) back nce 
| DocumentAmounts | [DocumentAmounts](General.DocumentAmounts.md) | List of [DocumentAmount](General.DocumentAmounts.md) child objects, based on the [DocumentAmount.Document](General.DocumentAmounts.md#document) back reference 
| FileAttachments | [DocumentFileAttachments](General.DocumentFileAttachments.md) | List of [DocumentFileAttachment](General.DocumentFileAttachments.md) child objects, based on the [DocumentFileAttachment.Document](General.DocumentFileAttachments.md#document) back reference 
| LineAmounts | [DocumentLineAmounts](General.DocumentLineAmounts.md) | List of [DocumentLineAmount](General.DocumentLineAmounts.md) child objects, based on the [DocumentLineAmount.Document](General.DocumentLineAmounts.md#document) back reference 
| Lines | [OfferLines](Crm.Presales.OfferLines.md) | List of [OfferLine](Crm.Presales.OfferLines.md) child objects, based on the [Crm.Presales.OfferLine.Offer](Crm.Presales.OfferLines.md#offer) back reference 
| Prints | [DocumentPrints](General.DocumentPrints.md) | List of [DocumentPrint](General.DocumentPrints.md) child objects, based on the [DocumentPrint.Document](General.DocumentPrints.md#document) back reference 
| StateChanges | [DocumentStateChanges](General.DocumentStateChanges.md) | List of [DocumentStateChange](General.DocumentStateChanges.md) child objects, based on the [DocumentStateChange.Document](General.DocumentStateChanges.md#document) back reference 
| Versions | [DocumentVersions](General.DocumentVersions.md) | List of [DocumentVersion](General.Documents.md#documentversion) child objects, based on the [DocumentVersion.Document](General.DocumentVersions.md#document) back reference 


## Attribute Details

### AcceptedOn

> The date on which the customer accepted the offer. null if the offer is not yet accepted or the date is unknown.

_Type_: **datetime (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

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

### DocumentNotes

> Notes for this Document

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### DocumentVersion

> [Filter(eq;ge;le)]

_Type_: **int32**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **1**  

### EntityName

> The entity name of the document equal to the entity name of the document type.[Filter(eq)] [ORD]

_Type_: **string**  
_Supported Filters_: **Equals**  
_Supports Order By_: **True**  

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

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

> Notes for this Offer.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ParentDocumentRelationshipType

> Type of relationship between the current document and the parent document(s). Affects the constraints for execution/completion for the documents. Possible values: 'S' = 'Subtask', 'N' = 'Next task'.

_Type_: **[ParentDocument<br />RelationshipType](Crm.Presales.Offers.md#parentdocumentrelationshiptype) (nullable)**  
Relationship between parent and child documents  
_Allowed Values (General.ParentDocumentRelationshipType Enum Members)_  

| Value | Description |
| ---- | --- |
| Subtask | The child document is a sub-task of the parent document. (Complete child to complete parent) <br /> _Database Value:_ 'S' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Subtask' |
| NextTask | The child document is next task of the parent document. (Complete parent to complete child) <br /> _Database Value:_ 'N' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'NextTask' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### PaymentDueDate

> The last term for payment.

_Type_: **datetime (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`obj.DocumentDate.AddDays( Convert( IIF( ( obj.ShipToCustomer.DefaultPaymentTermDays != 0), obj.ShipToCustomer.DefaultPaymentTermDays, obj.Customer.DefaultPaymentTermDays), Double))`
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

### RequiredDeliveryDate

> When not null, specifies required delivery date for all offer lines. When the lines contain different delivery dates, this is null.

_Type_: **date (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`obj.DocumentDate.AddDays( Convert( IIF( ( obj.ShipToCustomer.DefaultDeliveryTermDays != 0), obj.ShipToCustomer.DefaultDeliveryTermDays, obj.Customer.DefaultDeliveryTermDays), Double))`
`obj.Lines.Select( c => OfferLinesRepository.RequiredDeliveryDateAttribute.GetUntypedValue( c, False)).Distinct( ).OnlyIfSingle( )`
### State

> 0=New;5=Corrective;10=Computer Planned;20=Human Planned;30=Released;40=Completed;50=Closed [Required][Filter(eq;ge;le)]

_Type_: **[DocumentState](Crm.Presales.Offers.md#state)**  
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

### ValidTill

> Last date when the offer is valid. null means the offer has no specific validity date. [Filter(ge;le)]

_Type_: **datetime (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

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


## Reference Details

### AccessKey

> The access key, containing the user permissions for this document. null means that all users have unlimited permissions

_Type_: **[AccessKeys](Systems.Security.AccessKeys.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### AdjustedDocument

> The primary document, which the current document adjusts. null when this is not an adjustment document

_Type_: **[Documents](General.Documents.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### AssignedToUser

> The user to which this document is assigned for handling. null means that the document is not assigned to specific user

_Type_: **[Users](Systems.Security.Users.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### CurrencyDirectory

> The currency directory, containing all the convertion rates, used by the document. null means that the document does not need currency convertions

_Type_: **[CurrencyDirectories](General.CurrencyDirectories.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### Customer

> The customer to which the products are offered. [Required] [Filter(multi eq)]

_Type_: **[Customers](Crm.Customers.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### Deal

> The opportunity (deal) on which this offer is based. [Filter(multi eq)]

_Type_: **[Deals](Crm.Presales.Deals.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### DocumentCurrency

> The currency in which the document is issued. All amounts are in this currency. [Required] [Filter(multi eq)]

_Type_: **[Currencies](General.Currencies.md)**  
_Supported Filters_: **Equals, EqualsIn**  

_Back-End Default Expression:_  
`obj.ShipToCustomer.DefaultCurrency.IfNullThen( obj.Customer.DefaultCurrency).IfNullThen( obj.DocumentCurrency).IfNullThen( obj.EnterpriseCompany.BaseCurrency)`

_Front-End Recalc Expressions:_  
`obj.ShipToCustomer.DefaultCurrency.IfNullThen( obj.Customer.DefaultCurrency).IfNullThen( obj.DocumentCurrency).IfNullThen( obj.EnterpriseCompany.BaseCurrency)`
### DocumentType

> The user defined type of the document. Determines document behaviour, properties, additional amounts, validation, generations, etc. [Required]

_Type_: **[DocumentTypes](General.DocumentTypes.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### EnterpriseCompany

> The enterprise company which issued the document [Required]

_Type_: **[EnterpriseCompanies](General.EnterpriseCompanies.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### EnterpriseCompanyLocation

> The enterprise company location which issued the document. null means that there is only one location within the enterprise company and locations are not used

_Type_: **[CompanyLocations](General.Contacts.CompanyLocations.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### FromCompanyDivision

> The division of the company, issuing the document. null when the document is not issued by any specific division

_Type_: **[CompanyDivisions](General.Contacts.CompanyDivisions.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### FromParty

> The party which issued the document [Required]

_Type_: **[Parties](General.Contacts.Parties.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### MasterDocument

> In a multi-document tree, this is the root document, that created the whole tree. If this is the root it is equal to Id [Required]

_Type_: **[Documents](General.Documents.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### Parent

> In a multi-document tree, this is the direct parent document. If this is the root it is null

_Type_: **[Documents](General.Documents.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### PaymentType

> Way of payment. null means that no specific way of payment was offered. [Filter(multi eq)]

_Type_: **[PaymentTypes](Finance.Payments.PaymentTypes.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

_Front-End Recalc Expressions:_  
`obj.ShipToCustomer.DefaultPaymentType.IfNullThen( obj.Customer.DefaultPaymentType).IfNullThen( obj.PaymentType)`
### PriceList

> The price list, based on which the prices are selected. Initially copied from the definition of the Customer. [Filter(multi eq)]

_Type_: **[PriceLists](Crm.PriceLists.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### PrimeCauseDocument

> The document that is the prime cause for creation of the current document

_Type_: **[Documents](General.Documents.md) (nullable)**  
_Supported Filters_: **EqualsIn**  

### RecipientPerson

> The offer recipient. It should be employee of the customer. null means that there is no default recipient or he/she is unknown. [Filter(multi eq)]

_Type_: **[Persons](General.Contacts.Persons.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### ResponsiblePerson

> The person that is responsible for this order or transaction. It could be the sales person, the orderer, etc.

_Type_: **[Persons](General.Contacts.Persons.md) (nullable)**  
_Supported Filters_: **EqualsIn**  

### ReverseOfDocument

> The document which the current document is reverse of

_Type_: **[Documents](General.Documents.md) (nullable)**  
_Supported Filters_: **EqualsIn**  

### SalesPerson

> Responsible sales person. null when no sales person was assigned. [Filter(multi eq)]

_Type_: **[SalesPersons](Crm.SalesPersons.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

_Front-End Recalc Expressions:_  
`DetermineSalesPerson( obj.Transaction, obj.EnterpriseCompany, new [] {obj.Customer, obj.ShipToCustomer})`
### Sequence

> The sequence that will be used to give new numbers to the documents of this type

_Type_: **[Sequences](General.Sequences.md) (nullable)**  
_Supported Filters_: **EqualsIn**  

### ShipToCustomer

> The customer to whom to ship the sales order. Usually it is a customer entry for a sub-party of the primary customer. [Filter(multi eq)]

_Type_: **[Customers](Crm.Customers.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

_Front-End Recalc Expressions:_  
`DetermineShipToCustomer( obj.Transaction, obj.EnterpriseCompany, obj.EnterpriseCompanyLocation, obj.Customer)`
### Store

> The store, from which the products will be sold. When null, the store is unknown or N/A. [Filter(multi eq)]

_Type_: **[Stores](Logistics.Inventory.Stores.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### ToCompanyDivision

> The division of the company, receiving the document. null when the document is not received by any specific division

_Type_: **[CompanyDivisions](General.Contacts.CompanyDivisions.md)**  
_Supported Filters_: **NotFilterable**  

### ToParty

> The party which should receive the document

_Type_: **[Parties](General.Contacts.Parties.md) (nullable)**  
_Supported Filters_: **EqualsIn**  

### UserStatus

> The user status of this document if applicable for this document type. null means unknown or not yet set

_Type_: **[DocumentTypeUserStatuses](General.DocumentTypeUserStatuses.md) (nullable)**  
_Supported Filters_: **EqualsIn**  



## Business Rules

[!list erp.entity=Crm.Presales.Offers erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Crm.Presales.Offers erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Crm.Presales.Offers erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_Presales_Offers?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Crm_Presales_Offers?$top=10>

