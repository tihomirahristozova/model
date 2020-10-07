# Crm.Sales.SalesOrders

Sales order document headers. Entity: Crm_Sales_Orders

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Crm.Sales.SalesOrders.md#Id) | guid |  
| [CompleteTime](Crm.Sales.SalesOrders.md#CompleteTime) | datetime (nullable) | Exact time, when the document was last completed[Filter(ge;le)] 
| [CreationTime](Crm.Sales.SalesOrders.md#CreationTime) | datetime | Date/Time when the document was created [Required][Filter(ge;le)] 
| [CreationUser](Crm.Sales.SalesOrders.md#CreationUser) | string | The login name of the user, who created the document [Required][Filter(like)] 
| [DocumentDate](Crm.Sales.SalesOrders.md#DocumentDate) | datetime | The date on which the document was issued [Required][Filter(eq;ge;le)][ORD] 
| [DocumentNo](Crm.Sales.SalesOrders.md#DocumentNo) | string | Document number, unique within Document_Type_Id [Required][Filter(eq;like)][ORD] 
| [DocumentVersion](Crm.Sales.SalesOrders.md#DocumentVersion) | int32 | [Filter(eq;ge;le)] 
| [DocumentNotes](Crm.Sales.SalesOrders.md#DocumentNotes) | string (nullable) | Notes for this Document 
| [ParentDocumentRelationshipType](Crm.Sales.SalesOrders.md#ParentDocumentRelationshipType) | [General.ParentDocumentRelationshipType](Crm.Sales.SalesOrders.md#ParentDocumentRelationshipType) (nullable) | Type of relationship between the current document and the parent document(s). Affects the constraints for execution/completion for the documents. Possible values: 'S' = 'Subtask', 'N' = 'Next task'. 
| [PlanningOnly](Crm.Sales.SalesOrders.md#PlanningOnly) | boolean (nullable) | Indicates that the document is used only for planning (and as consequence its state cannot be greater than Planned) [Required] 
| [ReadOnly](Crm.Sales.SalesOrders.md#ReadOnly) | boolean | True - the document is read only; false - the document is not read only [Required] 
| [ReferenceDate](Crm.Sales.SalesOrders.md#ReferenceDate) | datetime (nullable) | The date to which this document refers, i.e. when the action really occurred. If null, Document_Date is taken [Filter(ge;le)] 
| [ReferenceDocumentNo](Crm.Sales.SalesOrders.md#ReferenceDocumentNo) | string (nullable) | The number of the document (issued by the other party), which was the reason for the creation of the current document. The numebr should be unique within the party documents [Filter(eq;like)] 
| [ReleaseTime](Crm.Sales.SalesOrders.md#ReleaseTime) | datetime (nullable) | Exact time, when the document was first released [Filter(ge;le)] 
| [State](Crm.Sales.SalesOrders.md#State) | [General.DocumentState](Crm.Sales.SalesOrders.md#State) | 0=New;5=Corrective;10=Computer Planned;20=Human Planned;30=Released;40=Completed;50=Closed [Required][Filter(eq;ge;le)] 
| [Void](Crm.Sales.SalesOrders.md#Void) | boolean | True if the document is null and void [Required][Filter(eq)] 
| [VoidReason](Crm.Sales.SalesOrders.md#VoidReason) | string (nullable) | Reason for voiding the document, entered by the user 
| [VoidTime](Crm.Sales.SalesOrders.md#VoidTime) | datetime (nullable) | Date/time when the document has become void 
| [VoidUser](Crm.Sales.SalesOrders.md#VoidUser) | string (nullable) | The user who voided the document 
| [EntityName](Crm.Sales.SalesOrders.md#EntityName) | string | The entity name of the document equal to the entity name of the document type.[Filter(eq)] [ORD] 
| [CreditLimitOverride](Crm.Sales.SalesOrders.md#CreditLimitOverride) | boolean | Allows the sales order to be released even in the case of violations of credit limit or presence of overdue receivables. [Required] [Default(false)] [Filter(eq)] 
| [CustomerPurchaseOrderDate](Crm.Sales.SalesOrders.md#CustomerPurchaseOrderDate) | date (nullable) | Issue date of the referent customer purchase order. [Filter(ge;le)] 
| [CustomerPurchaseOrderNo](Crm.Sales.SalesOrders.md#CustomerPurchaseOrderNo) | string (nullable) | Reference number of the customer's purchase order. [Filter(eq;like)] 
| [DeliveryTermsCode](Crm.Sales.SalesOrders.md#DeliveryTermsCode) | [Finance.Intrastat.DeliveryTerms](Crm.Sales.SalesOrders.md#DeliveryTermsCode) (nullable) | Mode of delivery, like CIF, FOB, etc. Used also in Intrastat reporting. 
| [FiscalSalesNumber](Crm.Sales.SalesOrders.md#FiscalSalesNumber) | string (nullable) | Unique number of the sale, assigned for fiscal reporting purposes. The format is according to the applicable legislation. null means that there is no requirement for fiscal sales number for this document or it is unknown. [Filter(multi eq;like)] [ReadOnly] (Introduced in version 19.1.100.0) 
| [FromDate](Crm.Sales.SalesOrders.md#FromDate) | date (nullable) | When selling a service valid only for a period, denotes the beginning of the period. null means that it is unknown or N/A. (Introduced in version 20.1.100.0) 
| [IntrastatTransactionNatureCode](Crm.Sales.SalesOrders.md#IntrastatTransactionNatureCode) | [Finance.Intrastat.TransactionNature](Crm.Sales.SalesOrders.md#IntrastatTransactionNatureCode) (nullable) | Transaction nature; used for Intrastat reporting. 
| [IntrastatTransportModeCode](Crm.Sales.SalesOrders.md#IntrastatTransportModeCode) | [Finance.Intrastat.TransportMode](Crm.Sales.SalesOrders.md#IntrastatTransportModeCode) (nullable) | Transport mode; used for Intrastat reporting. 
| [IsReleased](Crm.Sales.SalesOrders.md#IsReleased) | boolean | True if the document is not void and its state is released or greater. [Required] [Default(false)] [Filter(eq)] [ReadOnly] 
| [IsSingleExecution](Crm.Sales.SalesOrders.md#IsSingleExecution) | boolean | Specifies whether the document is a single execution of its order document. [Required] [Default(false)] [Filter(eq)] [ReadOnly] 
| [IsValidField](Crm.Sales.SalesOrders.md#IsValidField) | boolean | True when the order is valid (e.g. released and not void). Used for internal processing. [Required] [Default(false)] [ReadOnly] 
| [Notes](Crm.Sales.SalesOrders.md#Notes) | string (nullable) | Notes for this SalesOrder. 
| [PaymentDueDate](Crm.Sales.SalesOrders.md#PaymentDueDate) | datetime (nullable) | The last term for the payment of the sales order. [Filter(ge;le)] 
| [PaymentDueStartDate](Crm.Sales.SalesOrders.md#PaymentDueStartDate) | datetime (nullable) | The date when the payment becomes due for documents with one installment. null when the document is with multiple installments. 
| [RequiredDeliveryDate](Crm.Sales.SalesOrders.md#RequiredDeliveryDate) | date (nullable) | The required delivery date for all lines in the sales order. Initially calculated, based on either the Ship To Customer or Customer delivery term. [Filter(ge;le)] 
| [ToDate](Crm.Sales.SalesOrders.md#ToDate) | date (nullable) | When selling a service valid only for a period, denotes the end of the period. null means that it is unknown or N/A. (Introduced in version 20.1.100.0) 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [AccessKey](Crm.Sales.SalesOrders.md#AccessKey) | [Systems.Security.AccessKeys](Systems.Security.AccessKeys.md) (nullable) | The access key, containing the user permissions for this document. null means that all users have unlimited permissions |
| [AdjustedDocument](Crm.Sales.SalesOrders.md#AdjustedDocument) | [General.Documents](General.Documents.md) (nullable) | The primary document, which the current document adjusts. null when this is not an adjustment document |
| [AssignedToUser](Crm.Sales.SalesOrders.md#AssignedToUser) | [Systems.Security.Users](Systems.Security.Users.md) (nullable) | The user to which this document is assigned for handling. null means that the document is not assigned to specific user |
| [CurrencyDirectory](Crm.Sales.SalesOrders.md#CurrencyDirectory) | [General.CurrencyDirectories](General.CurrencyDirectories.md) (nullable) | The currency directory, containing all the convertion rates, used by the document. null means that the document does not need currency convertions |
| [DocumentType](Crm.Sales.SalesOrders.md#DocumentType) | [General.DocumentTypes](General.DocumentTypes.md) | The user defined type of the document. Determines document behaviour, properties, additional amounts, validation, generations, etc. [Required] |
| [EnterpriseCompany](Crm.Sales.SalesOrders.md#EnterpriseCompany) | [General.EnterpriseCompanies](General.EnterpriseCompanies.md) | The enterprise company which issued the document [Required] |
| [EnterpriseCompanyLocation](Crm.Sales.SalesOrders.md#EnterpriseCompanyLocation) | [General.Contacts.CompanyLocations](General.Contacts.CompanyLocations.md) (nullable) | The enterprise company location which issued the document. null means that there is only one location within the enterprise company and locations are not used |
| [FromCompanyDivision](Crm.Sales.SalesOrders.md#FromCompanyDivision) | [General.Contacts.CompanyDivisions](General.Contacts.CompanyDivisions.md) (nullable) | The division of the company, issuing the document. null when the document is not issued by any specific division |
| [FromParty](Crm.Sales.SalesOrders.md#FromParty) | [General.Contacts.Parties](General.Contacts.Parties.md) | The party which issued the document [Required] |
| [MasterDocument](Crm.Sales.SalesOrders.md#MasterDocument) | [General.Documents](General.Documents.md) | In a multi-document tree, this is the root document, that created the whole tree. If this is the root it is equal to Id [Required] |
| [Parent](Crm.Sales.SalesOrders.md#Parent) | [General.Documents](General.Documents.md) (nullable) | In a multi-document tree, this is the direct parent document. If this is the root it is null |
| [PrimeCauseDocument](Crm.Sales.SalesOrders.md#PrimeCauseDocument) | [General.Documents](General.Documents.md) (nullable) | The document that is the prime cause for creation of the current document |
| [ResponsiblePerson](Crm.Sales.SalesOrders.md#ResponsiblePerson) | [General.Contacts.Persons](General.Contacts.Persons.md) (nullable) | The person that is responsible for this order or transaction. It could be the sales person, the orderer, etc. |
| [ReverseOfDocument](Crm.Sales.SalesOrders.md#ReverseOfDocument) | [General.Documents](General.Documents.md) (nullable) | The document which the current document is reverse of |
| [Sequence](Crm.Sales.SalesOrders.md#Sequence) | [General.Sequences](General.Sequences.md) (nullable) | The sequence that will be used to give new numbers to the documents of this type |
| [ToCompanyDivision](Crm.Sales.SalesOrders.md#ToCompanyDivision) | [General.Contacts.CompanyDivisions](General.Contacts.CompanyDivisions.md) | The division of the company, receiving the document. null when the document is not received by any specific division |
| [ToParty](Crm.Sales.SalesOrders.md#ToParty) | [General.Contacts.Parties](General.Contacts.Parties.md) (nullable) | The party which should receive the document |
| [UserStatus](Crm.Sales.SalesOrders.md#UserStatus) | [General.DocumentTypeUserStatuses](General.DocumentTypeUserStatuses.md) (nullable) | The user status of this document if applicable for this document type. null means unknown or not yet set |
| [Customer](Crm.Sales.SalesOrders.md#Customer) | [Crm.Customers](Crm.Customers.md) | The primary customer, which placed the sales order. [Required] [Filter(multi eq)] |
| [Deal](Crm.Sales.SalesOrders.md#Deal) | [Crm.Presales.Deals](Crm.Presales.Deals.md) (nullable) | The opportunity (deal) on which this order is based. [Filter(multi eq)] |
| [DealType](Crm.Sales.SalesOrders.md#DealType) | [Finance.Vat.DealTypes](Finance.Vat.DealTypes.md) (nullable) | Deal type to be passed to the invoice. If deal type in entered then the invoice creates VAT entry for this deal type. [Filter(multi eq)] |
| [Dealer](Crm.Sales.SalesOrders.md#Dealer) | [Crm.Dealers](Crm.Dealers.md) (nullable) | The external dealer, associated with the sales order. [Filter(multi eq)] |
| [DistributionChannel](Crm.Sales.SalesOrders.md#DistributionChannel) | [Crm.Marketing.DistributionChannels](Crm.Marketing.DistributionChannels.md) (nullable) | The distribution channel, that is used to deliver the products. [Filter(multi eq)] |
| [DocumentCurrency](Crm.Sales.SalesOrders.md#DocumentCurrency) | [General.Currencies](General.Currencies.md) | The currency of the document; e.g. the currency of the amounts in the document. [Required] [Filter(multi eq)] |
| [EndCustomerParty](Crm.Sales.SalesOrders.md#EndCustomerParty) | [General.Contacts.Parties](General.Contacts.Parties.md) (nullable) | The end customer is the customer of the dealer. It is stored for information purposes only. The end customer may not have customer definition; any party can be used. [Filter(multi eq)] (Introduced in version 20.1.100.0) |
| [FiscalPrinterPosDevice](Crm.Sales.SalesOrders.md#FiscalPrinterPosDevice) | [Crm.Pos.Devices](Crm.Pos.Devices.md) (nullable) | For POS sales, specifies the fiscal printer. null when the sales is not a POS sale. [Filter(multi eq)] (Introduced in version 19.1.100.0) |
| [IntrastatTransportCountry](Crm.Sales.SalesOrders.md#IntrastatTransportCountry) | [General.Geography.Countries](General.Geography.Countries.md) (nullable) | Country of origin of the transport company; used for Intrastat reporting. [Filter(multi eq)] |
| [PaymentAccount](Crm.Sales.SalesOrders.md#PaymentAccount) | [Finance.Payments.PaymentAccounts](Finance.Payments.PaymentAccounts.md) (nullable) | When not null, the payment account, where the payment is expected. null=no expectation for account. [Filter(multi eq)] |
| [PaymentType](Crm.Sales.SalesOrders.md#PaymentType) | [Finance.Payments.PaymentTypes](Finance.Payments.PaymentTypes.md) (nullable) | When not null specifies the payment type for the sales order. [Filter(multi eq)] |
| [PosLocation](Crm.Sales.SalesOrders.md#PosLocation) | [Crm.Pos.Locations](Crm.Pos.Locations.md) (nullable) | For POS sales, specifies the POS location, in which the sale is performed. null when the sales is not a POS sale. [Filter(multi eq)] (Introduced in version 19.1.100.0) |
| [PosOperator](Crm.Sales.SalesOrders.md#PosOperator) | [Crm.Pos.Operators](Crm.Pos.Operators.md) (nullable) | For POS sales, specifies the POS operator, who created the sale. null when the sale is not a POS sale. [Filter(multi eq)] (Introduced in version 19.1.100.0) |
| [PosTerminal](Crm.Sales.SalesOrders.md#PosTerminal) | [Crm.Pos.Terminals](Crm.Pos.Terminals.md) (nullable) | For POS sales, specifies the POS terminal, on which the sale is entered. null when the sales is not a POS sale. [Filter(multi eq)] (Introduced in version 19.1.100.0) |
| [PriceList](Crm.Sales.SalesOrders.md#PriceList) | [Crm.PriceLists](Crm.PriceLists.md) (nullable) | The price list to be used for determining product prices in the lines. [Filter(multi eq)] |
| [ReturnForInvoice](Crm.Sales.SalesOrders.md#ReturnForInvoice) | [Crm.Invoicing.Invoices](Crm.Invoicing.Invoices.md) (nullable) | When specified indicates that some of the goods sold in the sales orders invoiced with Return_For_Invoice_Id are returned with the current document. [Filter(multi eq)] |
| [ReturnForSalesOrder](Crm.Sales.SalesOrders.md#ReturnForSalesOrder) | [Crm.Sales.SalesOrders](Crm.Sales.SalesOrders.md) (nullable) | When specified indicates that some of the goods sold in Return_For_Sales_Order_Id are returned with the current document. [Filter(multi eq;like)] |
| [SalesPerson](Crm.Sales.SalesOrders.md#SalesPerson) | [Crm.SalesPersons](Crm.SalesPersons.md) (nullable) | Internal company sales person. [Filter(multi eq)] |
| [ShipToCustomer](Crm.Sales.SalesOrders.md#ShipToCustomer) | [Crm.Customers](Crm.Customers.md) (nullable) | The customer to whom to ship the sales order. Usually it is a customer entry for a sub-party of the primary customer. [Filter(multi eq)] |
| [ShipToPartyContactMechanism](Crm.Sales.SalesOrders.md#ShipToPartyContactMechanism) | [General.Contacts.PartyContactMechanisms](General.Contacts.PartyContactMechanisms.md) (nullable) | The contact mechanism (address) to whih to ship the sales order. [Filter(multi eq)] |
| [Store](Crm.Sales.SalesOrders.md#Store) | [Logistics.Inventory.Stores](Logistics.Inventory.Stores.md) (nullable) | The store from which to issue the sales order. null means that there is no store associated with the sales order or there are different stores for some of the lines. [Filter(multi eq)] |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| DocumentAmounts | [General.DocumentAmounts](General.DocumentAmounts.md) | List of [DocumentAmount](General.DocumentAmounts.md) child objects, based on the [DocumentAmount.Document](General.DocumentAmounts.md#Document) back reference 
| Comments | [General.DocumentComments](General.DocumentComments.md) | List of [DocumentComment](General.DocumentComments.md) child objects, based on the [DocumentComment.Document](General.DocumentComments.md#Document) back reference 
| DistributedAmounts | [General.DocumentDistributedAmounts](General.DocumentDistributedAmounts.md) | List of [DocumentDistributedAmount](General.DocumentDistributedAmounts.md) child objects, based on the [DocumentDistributedAmount.Document](General.DocumentDistributedAmounts.md#Document) back reference 
| FileAttachments | [General.DocumentFileAttachments](General.DocumentFileAttachments.md) | List of [DocumentFileAttachment](General.DocumentFileAttachments.md) child objects, based on the [DocumentFileAttachment.Document](General.DocumentFileAttachments.md#Document) back reference 
| LineAmounts | [General.DocumentLineAmounts](General.DocumentLineAmounts.md) | List of [DocumentLineAmount](General.DocumentLineAmounts.md) child objects, based on the [DocumentLineAmount.Document](General.DocumentLineAmounts.md#Document) back reference 
| Prints | [General.DocumentPrints](General.DocumentPrints.md) | List of [DocumentPrint](General.DocumentPrints.md) child objects, based on the [DocumentPrint.Document](General.DocumentPrints.md#Document) back reference 
| StateChanges | [General.DocumentStateChanges](General.DocumentStateChanges.md) | List of [DocumentStateChange](General.DocumentStateChanges.md) child objects, based on the [DocumentStateChange.Document](General.DocumentStateChanges.md#Document) back reference 
| Versions | [General.DocumentVersions](General.DocumentVersions.md) | List of [DocumentVersion](General.Documents.md#DocumentVersion) child objects, based on the [DocumentVersion.Document](General.DocumentVersions.md#Document) back reference 
| Lines | [Crm.Sales.SalesOrderLines](Crm.Sales.SalesOrderLines.md) | List of [SalesOrderLine](Crm.Sales.SalesOrderLines.md) child objects, based on the [Crm.Sales.SalesOrderLine.SalesOrder](Crm.Sales.SalesOrderLines.md#SalesOrder) back reference 
| PaymentPlans | [Crm.Sales.SalesOrderPaymentPlans](Crm.Sales.SalesOrderPaymentPlans.md) | List of [SalesOrderPaymentPlan](Crm.Sales.SalesOrderPaymentPlans.md) child objects, based on the [Crm.Sales.SalesOrderPaymentPlan.SalesOrder](Crm.Sales.SalesOrderPaymentPlans.md#SalesOrder) back reference 
| PromotionalPackages | [Crm.Sales.SalesOrderPromotionalPackages](Crm.Sales.SalesOrderPromotionalPackages.md) | List of [SalesOrderPromotionalPackage](Crm.Sales.SalesOrderPromotionalPackages.md) child objects, based on the [Crm.Sales.SalesOrderPromotionalPackage.SalesOrder](Crm.Sales.SalesOrderPromotionalPackages.md#SalesOrder) back reference 


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

_Type_: **[General.ParentDocumentRelationshipType](Crm.Sales.SalesOrders.md#ParentDocumentRelationshipType) (nullable)**  
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

_Type_: **[General.DocumentState](Crm.Sales.SalesOrders.md#State)**  
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

### CreditLimitOverride

> Allows the sales order to be released even in the case of violations of credit limit or presence of overdue receivables. [Required] [Default(false)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### CustomerPurchaseOrderDate

> Issue date of the referent customer purchase order. [Filter(ge;le)]

_Type_: **date (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### CustomerPurchaseOrderNo

> Reference number of the customer's purchase order. [Filter(eq;like)]

_Type_: **string (nullable)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### DeliveryTermsCode

> Mode of delivery, like CIF, FOB, etc. Used also in Intrastat reporting.

_Type_: **[Finance.Intrastat.DeliveryTerms](Crm.Sales.SalesOrders.md#DeliveryTermsCode) (nullable)**  
Generic enum type for DeliveryTerms properties  
_Allowed Values (Enum Members)_  

| Value | Description |
| ---- | --- |
| ExWorks | ExWorks value. Stored as 'EXW'. <br /> _Database Value:_ 'EXW' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'ExWorks' |
| FrancoCarrier | FrancoCarrier value. Stored as 'FCA'. <br /> _Database Value:_ 'FCA' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'FrancoCarrier' |
| FreeAlongsideShip | FreeAlongsideShip value. Stored as 'FAS'. <br /> _Database Value:_ 'FAS' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'FreeAlongsideShip' |
| FreeOnBoard | FreeOnBoard value. Stored as 'FOB'. <br /> _Database Value:_ 'FOB' <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'FreeOnBoard' |
| CostAndFreightCF | CostAndFreightCF value. Stored as 'CFR'. <br /> _Database Value:_ 'CFR' <br /> _Model Value:_ 4 <br /> _Domain API Value:_ 'CostAndFreightCF' |
| CostInsuranceAndFreight | CostInsuranceAndFreight value. Stored as 'CIF'. <br /> _Database Value:_ 'CIF' <br /> _Model Value:_ 5 <br /> _Domain API Value:_ 'CostInsuranceAndFreight' |
| CarriagePaidTo | CarriagePaidTo value. Stored as 'CPT'. <br /> _Database Value:_ 'CPT' <br /> _Model Value:_ 6 <br /> _Domain API Value:_ 'CarriagePaidTo' |
| CarriageAndInsurancePaidTo | CarriageAndInsurancePaidTo value. Stored as 'CIP'. <br /> _Database Value:_ 'CIP' <br /> _Model Value:_ 7 <br /> _Domain API Value:_ 'CarriageAndInsurancePaidTo' |
| DeliveredAtPlace | DeliveredAtPlace value. Stored as 'DAP'. <br /> _Database Value:_ 'DAP' <br /> _Model Value:_ 8 <br /> _Domain API Value:_ 'DeliveredAtPlace' |
| DeliveredAtTerminal | DeliveredAtTerminal value. Stored as 'DAT'. <br /> _Database Value:_ 'DAT' <br /> _Model Value:_ 9 <br /> _Domain API Value:_ 'DeliveredAtTerminal' |
| DeliveredDutyPaid | DeliveredDutyPaid value. Stored as 'DDP'. <br /> _Database Value:_ 'DDP' <br /> _Model Value:_ 10 <br /> _Domain API Value:_ 'DeliveredDutyPaid' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`obj.Lines.Select(c => SalesOrderLinesRepository.DeliveryTermsCodeAttribute.GetUntypedValue(c, False)).Distinct().OnlyIfSingle()`
### FiscalSalesNumber

> Unique number of the sale, assigned for fiscal reporting purposes. The format is according to the applicable legislation. null means that there is no requirement for fiscal sales number for this document or it is unknown. [Filter(multi eq;like)] [ReadOnly] (Introduced in version 19.1.100.0)

_Type_: **string (nullable)**  
_Supported Filters_: **Equals, Like, EqualsIn**  
_Supports Order By_: **False**  

### FromDate

> When selling a service valid only for a period, denotes the beginning of the period. null means that it is unknown or N/A. (Introduced in version 20.1.100.0)

_Type_: **date (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`obj.Lines.Select(c => SalesOrderLinesRepository.LineFromDateAttribute.GetUntypedValue(c, False)).Distinct().OnlyIfSingle()`
### IntrastatTransactionNatureCode

> Transaction nature; used for Intrastat reporting.

_Type_: **[Finance.Intrastat.TransactionNature](Crm.Sales.SalesOrders.md#IntrastatTransactionNatureCode) (nullable)**  
Generic enum type for TransactionNature properties  
_Allowed Values (Enum Members)_  

| Value | Description |
| ---- | --- |
| OutrightPurchaseOrSale | OutrightPurchaseOrSale value. Stored as '11'. <br /> _Database Value:_ '11' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'OutrightPurchaseOrSale' |
| SupplyForSale | SupplyForSale value. Stored as '12'. <br /> _Database Value:_ '12' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'SupplyForSale' |
| BarterTrade | BarterTrade value. Stored as '13'. <br /> _Database Value:_ '13' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'BarterTrade' |
| FinancialLeasing | FinancialLeasing value. Stored as '14'. <br /> _Database Value:_ '14' <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'FinancialLeasing' |
| OtherTransactions | OtherTransactions value. Stored as '19'. <br /> _Database Value:_ '19' <br /> _Model Value:_ 4 <br /> _Domain API Value:_ 'OtherTransactions' |
| ReturnStokilizing | ReturnStokilizing value. Stored as '21'. <br /> _Database Value:_ '21' <br /> _Model Value:_ 5 <br /> _Domain API Value:_ 'ReturnStokilizing' |
| ReplacementForReturnedGoods | ReplacementForReturnedGoods value. Stored as '22'. <br /> _Database Value:_ '22' <br /> _Model Value:_ 6 <br /> _Domain API Value:_ 'ReplacementForReturnedGoods' |
| ReplacementOfGoodsNotBeingReturned | ReplacementOfGoodsNotBeingReturned value. Stored as '23'. <br /> _Database Value:_ '23' <br /> _Model Value:_ 7 <br /> _Domain API Value:_ 'ReplacementOfGoodsNotBeingReturned' |
| ReturnOrExchangeOfOtherGoods | ReturnOrExchangeOfOtherGoods value. Stored as '29'. <br /> _Database Value:_ '29' <br /> _Model Value:_ 8 <br /> _Domain API Value:_ 'ReturnOrExchangeOfOtherGoods' |
| SpecificTransactions | SpecificTransactions value. Stored as '60'. <br /> _Database Value:_ '60' <br /> _Model Value:_ 9 <br /> _Domain API Value:_ 'SpecificTransactions' |
| OperationsOnJointProjects | OperationsOnJointProjects value. Stored as '70'. <br /> _Database Value:_ '70' <br /> _Model Value:_ 10 <br /> _Domain API Value:_ 'OperationsOnJointProjects' |
| TransactionsOfConstructionMaterialsAndEquipment | TransactionsOfConstructionMaterialsAndEquipment value. Stored as '80'. <br /> _Database Value:_ '80' <br /> _Model Value:_ 11 <br /> _Domain API Value:_ 'TransactionsOfConstructionMaterialsAndEquipment' |
| OtherTransactionsLeasing | OtherTransactionsLeasing value. Stored as '91'. <br /> _Database Value:_ '91' <br /> _Model Value:_ 12 <br /> _Domain API Value:_ 'OtherTransactionsLeasing' |
| OtherTransactionsOther | OtherTransactionsOther value. Stored as '99'. <br /> _Database Value:_ '99' <br /> _Model Value:_ 13 <br /> _Domain API Value:_ 'OtherTransactionsOther' |
| DealsThatIncludePropertyTransfersWithoutFinancialCompensationOrCompensationInKind | DealsThatIncludePropertyTransfersWithoutFinancialCompensationOrCompensationInKind value. Stored as '30'. <br /> _Database Value:_ '30' <br /> _Model Value:_ 14 <br /> _Domain API Value:_ 'DealsThatIncludePropertyTransfersWithoutFinancialCompensationOrCompensationInKind' |
| GoodsThatAreExpectedToBeReturnedToSender | GoodsThatAreExpectedToBeReturnedToSender value. Stored as '41'. <br /> _Database Value:_ '41' <br /> _Model Value:_ 15 <br /> _Domain API Value:_ 'GoodsThatAreExpectedToBeReturnedToSender' |
| GoodsThatAreNotExpectedToBeReturnedToSender | GoodsThatAreNotExpectedToBeReturnedToSender value. Stored as '42'. <br /> _Database Value:_ '42' <br /> _Model Value:_ 16 <br /> _Domain API Value:_ 'GoodsThatAreNotExpectedToBeReturnedToSender' |
| GoodsThatAreReturnedToSender | GoodsThatAreReturnedToSender value. Stored as '51'. <br /> _Database Value:_ '51' <br /> _Model Value:_ 17 <br /> _Domain API Value:_ 'GoodsThatAreReturnedToSender' |
| GoodsThatAreNotReturnedToSender | GoodsThatAreNotReturnedToSender value. Stored as '52'. <br /> _Database Value:_ '52' <br /> _Model Value:_ 18 <br /> _Domain API Value:_ 'GoodsThatAreNotReturnedToSender' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`obj.Lines.Select(c => SalesOrderLinesRepository.IntrastatTransactionNatureCodeAttribute.GetUntypedValue(c, False)).Distinct().OnlyIfSingle()`
### IntrastatTransportModeCode

> Transport mode; used for Intrastat reporting.

_Type_: **[Finance.Intrastat.TransportMode](Crm.Sales.SalesOrders.md#IntrastatTransportModeCode) (nullable)**  
Generic enum type for TransportMode properties  
_Allowed Values (Enum Members)_  

| Value | Description |
| ---- | --- |
| Shipping | Shipping value. Stored as '1'. <br /> _Database Value:_ '1' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Shipping' |
| RailwayTransport | RailwayTransport value. Stored as '2'. <br /> _Database Value:_ '2' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'RailwayTransport' |
| RoadTransport | RoadTransport value. Stored as '3'. <br /> _Database Value:_ '3' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'RoadTransport' |
| AirTransport | AirTransport value. Stored as '4'. <br /> _Database Value:_ '4' <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'AirTransport' |
| Mail | Mail value. Stored as '5'. <br /> _Database Value:_ '5' <br /> _Model Value:_ 4 <br /> _Domain API Value:_ 'Mail' |
| FixedTransportInstallations | FixedTransportInstallations value. Stored as '6'. <br /> _Database Value:_ '6' <br /> _Model Value:_ 5 <br /> _Domain API Value:_ 'FixedTransportInstallations' |
| RiverTransport | RiverTransport value. Stored as '7'. <br /> _Database Value:_ '7' <br /> _Model Value:_ 6 <br /> _Domain API Value:_ 'RiverTransport' |
| SelfPropelled | SelfPropelled value. Stored as '8'. <br /> _Database Value:_ '8' <br /> _Model Value:_ 7 <br /> _Domain API Value:_ 'SelfPropelled' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`obj.Lines.Select(c => SalesOrderLinesRepository.IntrastatTransportModeCodeAttribute.GetUntypedValue(c, False)).Distinct().OnlyIfSingle()`
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

### IsValidField

> True when the order is valid (e.g. released and not void). Used for internal processing. [Required] [Default(false)] [ReadOnly]

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### Notes

> Notes for this SalesOrder.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### PaymentDueDate

> The last term for the payment of the sales order. [Filter(ge;le)]

_Type_: **datetime (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`obj.DocumentDate.AddDays(Convert(IIF((obj.ShipToCustomer.DefaultPaymentTermDays != 0), obj.ShipToCustomer.DefaultPaymentTermDays, obj.Customer.DefaultPaymentTermDays), Double))`
### PaymentDueStartDate

> The date when the payment becomes due for documents with one installment. null when the document is with multiple installments.

_Type_: **datetime (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`obj.DocumentDate.AddDays(Convert(IIF((obj.ShipToCustomer.DefaultPaymentStartDays != 0), obj.ShipToCustomer.DefaultPaymentStartDays, obj.Customer.DefaultPaymentStartDays), Double))`
### RequiredDeliveryDate

> The required delivery date for all lines in the sales order. Initially calculated, based on either the Ship To Customer or Customer delivery term. [Filter(ge;le)]

_Type_: **date (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`obj.DocumentDate.AddDays(Convert(IIF((obj.ShipToCustomer.DefaultDeliveryTermDays != 0), obj.ShipToCustomer.DefaultDeliveryTermDays, obj.Customer.DefaultDeliveryTermDays), Double))`
`obj.Lines.Select(c => SalesOrderLinesRepository.RequiredDeliveryDateAttribute.GetUntypedValue(c, False)).Distinct().OnlyIfSingle()`
### ToDate

> When selling a service valid only for a period, denotes the end of the period. null means that it is unknown or N/A. (Introduced in version 20.1.100.0)

_Type_: **date (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`obj.Lines.Select(c => SalesOrderLinesRepository.LineToDateAttribute.GetUntypedValue(c, False)).Distinct().OnlyIfSingle()`

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

### Customer

> The primary customer, which placed the sales order. [Required] [Filter(multi eq)]

_Type_: **[Crm.Customers](Crm.Customers.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Deal

> The opportunity (deal) on which this order is based. [Filter(multi eq)]

_Type_: **[Crm.Presales.Deals](Crm.Presales.Deals.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### DealType

> Deal type to be passed to the invoice. If deal type in entered then the invoice creates VAT entry for this deal type. [Filter(multi eq)]

_Type_: **[Finance.Vat.DealTypes](Finance.Vat.DealTypes.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`obj.Lines.Select(c => c.LineDealType).Distinct().OnlyIfSingle()`
### Dealer

> The external dealer, associated with the sales order. [Filter(multi eq)]

_Type_: **[Crm.Dealers](Crm.Dealers.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### DistributionChannel

> The distribution channel, that is used to deliver the products. [Filter(multi eq)]

_Type_: **[Crm.Marketing.DistributionChannels](Crm.Marketing.DistributionChannels.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`obj.ShipToCustomer.DefaultDistributionChannel.IfNullThen(obj.Customer.DefaultDistributionChannel).IfNullThen(obj.DistributionChannel)`
### DocumentCurrency

> The currency of the document; e.g. the currency of the amounts in the document. [Required] [Filter(multi eq)]

_Type_: **[General.Currencies](General.Currencies.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`obj.ShipToCustomer.DefaultCurrency.IfNullThen(obj.Customer.DefaultCurrency).IfNullThen(obj.DocumentCurrency).IfNullThen(obj.EnterpriseCompany.BaseCurrency)`

_Front-End Recalc Expressions:_  
`obj.ShipToCustomer.DefaultCurrency.IfNullThen(obj.Customer.DefaultCurrency).IfNullThen(obj.DocumentCurrency).IfNullThen(obj.EnterpriseCompany.BaseCurrency)`
### EndCustomerParty

> The end customer is the customer of the dealer. It is stored for information purposes only. The end customer may not have customer definition; any party can be used. [Filter(multi eq)] (Introduced in version 20.1.100.0)

_Type_: **[General.Contacts.Parties](General.Contacts.Parties.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`obj.Lines.Select(c => c.LineEndCustomerParty).Distinct().OnlyIfSingle()`
### FiscalPrinterPosDevice

> For POS sales, specifies the fiscal printer. null when the sales is not a POS sale. [Filter(multi eq)] (Introduced in version 19.1.100.0)

_Type_: **[Crm.Pos.Devices](Crm.Pos.Devices.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### IntrastatTransportCountry

> Country of origin of the transport company; used for Intrastat reporting. [Filter(multi eq)]

_Type_: **[General.Geography.Countries](General.Geography.Countries.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`obj.Lines.Select(c => c.IntrastatTransportCountry).Distinct().OnlyIfSingle()`
### PaymentAccount

> When not null, the payment account, where the payment is expected. null=no expectation for account. [Filter(multi eq)]

_Type_: **[Finance.Payments.PaymentAccounts](Finance.Payments.PaymentAccounts.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`DeterminePaymentAccount(obj.Transaction, obj.Customer, obj.ShipToCustomer, obj.PaymentType, obj.PaymentAccount)`
`obj.PaymentPlans.Select(c => c.PaymentAccount).Distinct().OnlyIfSingle()`
### PaymentType

> When not null specifies the payment type for the sales order. [Filter(multi eq)]

_Type_: **[Finance.Payments.PaymentTypes](Finance.Payments.PaymentTypes.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`obj.ShipToCustomer.DefaultPaymentType.IfNullThen(obj.Customer.DefaultPaymentType).IfNullThen(obj.PaymentType)`
`obj.PaymentPlans.Select(c => c.PaymentType).Distinct().OnlyIfSingle()`
### PosLocation

> For POS sales, specifies the POS location, in which the sale is performed. null when the sales is not a POS sale. [Filter(multi eq)] (Introduced in version 19.1.100.0)

_Type_: **[Crm.Pos.Locations](Crm.Pos.Locations.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### PosOperator

> For POS sales, specifies the POS operator, who created the sale. null when the sale is not a POS sale. [Filter(multi eq)] (Introduced in version 19.1.100.0)

_Type_: **[Crm.Pos.Operators](Crm.Pos.Operators.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### PosTerminal

> For POS sales, specifies the POS terminal, on which the sale is entered. null when the sales is not a POS sale. [Filter(multi eq)] (Introduced in version 19.1.100.0)

_Type_: **[Crm.Pos.Terminals](Crm.Pos.Terminals.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### PriceList

> The price list to be used for determining product prices in the lines. [Filter(multi eq)]

_Type_: **[Crm.PriceLists](Crm.PriceLists.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### ReturnForInvoice

> When specified indicates that some of the goods sold in the sales orders invoiced with Return_For_Invoice_Id are returned with the current document. [Filter(multi eq)]

_Type_: **[Crm.Invoicing.Invoices](Crm.Invoicing.Invoices.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### ReturnForSalesOrder

> When specified indicates that some of the goods sold in Return_For_Sales_Order_Id are returned with the current document. [Filter(multi eq;like)]

_Type_: **[Crm.Sales.SalesOrders](Crm.Sales.SalesOrders.md) (nullable)**  
_Supported Filters_: **Equals, Like, EqualsIn**  
_Supports Order By_: **False**  

### SalesPerson

> Internal company sales person. [Filter(multi eq)]

_Type_: **[Crm.SalesPersons](Crm.SalesPersons.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`DetermineSalesPerson(obj.Transaction, obj.EnterpriseCompany, new [] {obj.Customer, obj.ShipToCustomer})`
### ShipToCustomer

> The customer to whom to ship the sales order. Usually it is a customer entry for a sub-party of the primary customer. [Filter(multi eq)]

_Type_: **[Crm.Customers](Crm.Customers.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`DetermineShipToCustomer(obj.Transaction, obj.EnterpriseCompany, obj.EnterpriseCompanyLocation, obj.Customer, obj.ShipToCustomer)`
### ShipToPartyContactMechanism

> The contact mechanism (address) to whih to ship the sales order. [Filter(multi eq)]

_Type_: **[General.Contacts.PartyContactMechanisms](General.Contacts.PartyContactMechanisms.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`obj.ShipToCustomer.Party.DefaultContactMechanism.IfNullThen(obj.Customer.Party.DefaultContactMechanism)`
### Store

> The store from which to issue the sales order. null means that there is no store associated with the sales order or there are different stores for some of the lines. [Filter(multi eq)]

_Type_: **[Logistics.Inventory.Stores](Logistics.Inventory.Stores.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`obj.Lines.Select(c => c.LineStore).Distinct().OnlyIfSingle()`


## Business Rules

[!list erp.entity=Crm.Sales.SalesOrders erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Crm.Sales.SalesOrders erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Crm.Sales.SalesOrders erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_Sales_SalesOrders?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Crm_Sales_SalesOrders?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_Sales_Orders?$top=10>

