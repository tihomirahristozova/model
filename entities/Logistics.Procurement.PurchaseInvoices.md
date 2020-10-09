---
uid: Logistics.Procurement.PurchaseInvoices
---
# Logistics.Procurement.PurchaseInvoices

Contains purchase invoice headers. Entity: Scm_Purchase_Invoices

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [ApplyDate](Logistics.Procurement.PurchaseInvoices.md#applydate) | date | Specifies the date on which to create the VAT ledger entry for this purchase invoice. Usually, this date is equal to the document date, except when the document is received too late to be applied on its original document date. [Required] [Filter(ge;le)] 
| [CompleteTime](Logistics.Procurement.PurchaseInvoices.md#completetime) | datetime (nullable) | Exact time, when the document was last completed[Filter(ge;le)] 
| [CreationTime](Logistics.Procurement.PurchaseInvoices.md#creationtime) | datetime | Date/Time when the document was created [Required][Filter(ge;le)] 
| [CreationUser](Logistics.Procurement.PurchaseInvoices.md#creationuser) | string | The login name of the user, who created the document [Required][Filter(like)] 
| [CreditNoteReason](Logistics.Procurement.PurchaseInvoices.md#creditnotereason) | string (nullable) | Reason for the debit/credit note. 
| [DeliveryTermsCode](Logistics.Procurement.PurchaseInvoices.md#deliverytermscode) | [DeliveryTerms](Logistics.Procurement.PurchaseInvoices.md#deliverytermscode) (nullable) | Mode of delivery, like CIF, FOB, etc. Used also in Intrastat reporting. 
| [DocumentDate](Logistics.Procurement.PurchaseInvoices.md#documentdate) | datetime | The date on which the document was issued [Required][Filter(eq;ge;le)][ORD] 
| [DocumentNo](Logistics.Procurement.PurchaseInvoices.md#documentno) | string | Document number, unique within Document_Type_Id [Required][Filter(eq;like)][ORD] 
| [DocumentNotes](Logistics.Procurement.PurchaseInvoices.md#documentnotes) | string (nullable) | Notes for this Document 
| [DocumentVersion](Logistics.Procurement.PurchaseInvoices.md#documentversion) | int32 | [Filter(eq;ge;le)] 
| [EntityName](Logistics.Procurement.PurchaseInvoices.md#entityname) | string | The entity name of the document equal to the entity name of the document type.[Filter(eq)] [ORD] 
| [Id](Logistics.Procurement.PurchaseInvoices.md#id) | guid |  
| [IntrastatTransaction<br />NatureCode](Logistics.Procurement.PurchaseInvoices.md#intrastattransactionnaturecode) | [TransactionNature](Logistics.Procurement.PurchaseInvoices.md#intrastattransactionnaturecode) (nullable) | Transaction nature; used for Intrastat reporting. 
| [IntrastatTransportModeCode](Logistics.Procurement.PurchaseInvoices.md#intrastattransportmodecode) | [TransportMode](Logistics.Procurement.PurchaseInvoices.md#intrastattransportmodecode) (nullable) | Transport mode; used for Intrastat reporting. 
| [IsReleased](Logistics.Procurement.PurchaseInvoices.md#isreleased) | boolean | True if the document is not void and its state is released or greater. [Required] [Default(false)] [Filter(eq)] [ReadOnly] 
| [IsSingleExecution](Logistics.Procurement.PurchaseInvoices.md#issingleexecution) | boolean | Specifies whether the document is a single execution of its order document. [Required] [Default(false)] [Filter(eq)] [ReadOnly] 
| [ParentDocument<br />RelationshipType](Logistics.Procurement.PurchaseInvoices.md#parentdocumentrelationshiptype) | [ParentDocument<br />RelationshipType](Logistics.Procurement.PurchaseInvoices.md#parentdocumentrelationshiptype) (nullable) | Type of relationship between the current document and the parent document(s). Affects the constraints for execution/completion for the documents. Possible values: 'S' = 'Subtask', 'N' = 'Next task'. 
| [PaymentDueDate](Logistics.Procurement.PurchaseInvoices.md#paymentduedate) | datetime (nullable) | Due date for paying the invoice. null means to use the default . [Filter(ge;le)] 
| [PlanningOnly](Logistics.Procurement.PurchaseInvoices.md#planningonly) | boolean (nullable) | Indicates that the document is used only for planning (and as consequence its state cannot be greater than Planned) [Required] 
| [ReadOnly](Logistics.Procurement.PurchaseInvoices.md#readonly) | boolean | True - the document is read only; false - the document is not read only [Required] 
| [ReferenceDate](Logistics.Procurement.PurchaseInvoices.md#referencedate) | datetime (nullable) | The date to which this document refers, i.e. when the action really occurred. If null, Document_Date is taken [Filter(ge;le)] 
| [ReferenceDocumentNo](Logistics.Procurement.PurchaseInvoices.md#referencedocumentno) | string (nullable) | The number of the document (issued by the other party), which was the reason for the creation of the current document. The numebr should be unique within the party documents [Filter(eq;like)] 
| [ReleaseTime](Logistics.Procurement.PurchaseInvoices.md#releasetime) | datetime (nullable) | Exact time, when the document was first released [Filter(ge;le)] 
| [State](Logistics.Procurement.PurchaseInvoices.md#state) | [DocumentState](Logistics.Procurement.PurchaseInvoices.md#state) | 0=New;5=Corrective;10=Computer Planned;20=Human Planned;30=Released;40=Completed;50=Closed [Required][Filter(eq;ge;le)] 
| [VATCashReportingMode](Logistics.Procurement.PurchaseInvoices.md#vatcashreportingmode) | boolean | When True, indicates, that this invoice uses the special 'Cash reporting mode' when creating VAT ledger entries. [Required] [Default(false)] [Filter(multi eq)] 
| [VATNotes](Logistics.Procurement.PurchaseInvoices.md#vatnotes) | string (nullable) | Description of the operation that will be entered in the VAT ledgers. 
| [Void](Logistics.Procurement.PurchaseInvoices.md#void) | boolean | True if the document is null and void [Required][Filter(eq)] 
| [VoidReason](Logistics.Procurement.PurchaseInvoices.md#voidreason) | string (nullable) | Reason for voiding the document, entered by the user 
| [VoidTime](Logistics.Procurement.PurchaseInvoices.md#voidtime) | datetime (nullable) | Date/time when the document has become void 
| [VoidUser](Logistics.Procurement.PurchaseInvoices.md#voiduser) | string (nullable) | The user who voided the document 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [AccessKey](Logistics.Procurement.PurchaseInvoices.md#accesskey) | [AccessKeys](Systems.Security.AccessKeys.md) (nullable) | The access key, containing the user permissions for this document. null means that all users have unlimited permissions |
| [AdjustedDocument](Logistics.Procurement.PurchaseInvoices.md#adjusteddocument) | [Documents](General.Documents.md) (nullable) | The primary document, which the current document adjusts. null when this is not an adjustment document |
| [AssignedToUser](Logistics.Procurement.PurchaseInvoices.md#assignedtouser) | [Users](Systems.Security.Users.md) (nullable) | The user to which this document is assigned for handling. null means that the document is not assigned to specific user |
| [CostCenter](Logistics.Procurement.PurchaseInvoices.md#costcenter) | [CostCenters](Finance.Accounting.CostCenters.md) (nullable) | Cost center for which the amount from this document will be accounted. [Filter(multi eq)] |
| [CreditNoteOriginal<br />PurchaseInvoice](Logistics.Procurement.PurchaseInvoices.md#creditnoteoriginalpurchaseinvoice) | [PurchaseInvoices](Logistics.Procurement.PurchaseInvoices.md) (nullable) | The original invoice, which is debited/credited with this note. [Filter(multi eq)] |
| [CurrencyDirectory](Logistics.Procurement.PurchaseInvoices.md#currencydirectory) | [CurrencyDirectories](General.CurrencyDirectories.md) (nullable) | The currency directory, containing all the convertion rates, used by the document. null means that the document does not need currency convertions |
| [DealType](Logistics.Procurement.PurchaseInvoices.md#dealtype) | [DealTypes](Finance.Vat.DealTypes.md) (nullable) | Deal type for this purchase invoice. If deal type in entered then VAT entry is created for this deal type. [Filter(multi eq)] |
| [DocumentCurrency](Logistics.Procurement.PurchaseInvoices.md#documentcurrency) | [Currencies](General.Currencies.md) | The currency of the unit prices and amounts in the document. [Required] [Filter(multi eq)] |
| [DocumentType](Logistics.Procurement.PurchaseInvoices.md#documenttype) | [DocumentTypes](General.DocumentTypes.md) | The user defined type of the document. Determines document behaviour, properties, additional amounts, validation, generations, etc. [Required] |
| [EnterpriseCompany](Logistics.Procurement.PurchaseInvoices.md#enterprisecompany) | [EnterpriseCompanies](General.EnterpriseCompanies.md) | The enterprise company which issued the document [Required] |
| [EnterpriseCompanyLocation](Logistics.Procurement.PurchaseInvoices.md#enterprisecompanylocation) | [CompanyLocations](General.Contacts.CompanyLocations.md) (nullable) | The enterprise company location which issued the document. null means that there is only one location within the enterprise company and locations are not used |
| [FromCompanyDivision](Logistics.Procurement.PurchaseInvoices.md#fromcompanydivision) | [CompanyDivisions](General.Contacts.CompanyDivisions.md) (nullable) | The division of the company, issuing the document. null when the document is not issued by any specific division |
| [FromParty](Logistics.Procurement.PurchaseInvoices.md#fromparty) | [Parties](General.Contacts.Parties.md) | The party which issued the document [Required] |
| [IntrastatDestinationRegion](Logistics.Procurement.PurchaseInvoices.md#intrastatdestinationregion) | [AdministrativeRegions](General.Geography.AdministrativeRegions.md) (nullable) | Region, which is the final destination of the goods. Used for Intrastat reporting. When this is non-null, it applies to the whole document. [Filter(multi eq)] |
| [IntrastatTransportCountry](Logistics.Procurement.PurchaseInvoices.md#intrastattransportcountry) | [Countries](General.Geography.Countries.md) (nullable) | Country of origin of the transport company; used for Intrastat reporting. [Filter(multi eq)] |
| [MasterDocument](Logistics.Procurement.PurchaseInvoices.md#masterdocument) | [Documents](General.Documents.md) | In a multi-document tree, this is the root document, that created the whole tree. If this is the root it is equal to Id [Required] |
| [Parent](Logistics.Procurement.PurchaseInvoices.md#parent) | [Documents](General.Documents.md) (nullable) | In a multi-document tree, this is the direct parent document. If this is the root it is null |
| [PaymentAccount](Logistics.Procurement.PurchaseInvoices.md#paymentaccount) | [PaymentAccounts](Finance.Payments.PaymentAccounts.md) (nullable) | When not null, specifies the default payment account for the payment order. [Filter(multi eq)] |
| [PaymentType](Logistics.Procurement.PurchaseInvoices.md#paymenttype) | [PaymentTypes](Finance.Payments.PaymentTypes.md) (nullable) | The payment type to be used. null is allowed only temporary and should be specified if payment order is to be generated. [Filter(multi eq)] |
| [PrimeCauseDocument](Logistics.Procurement.PurchaseInvoices.md#primecausedocument) | [Documents](General.Documents.md) (nullable) | The document that is the prime cause for creation of the current document |
| [PurchaseOrder](Logistics.Procurement.PurchaseInvoices.md#purchaseorder) | [PurchaseOrders](Logistics.Procurement.PurchaseOrders.md) (nullable) | The purchase order that was sent to the supplier and is the base for the invoice. null means there is no linked PO and 3 way check won't be performed. [Filter(multi eq)] |
| [PurchasePriceList](Logistics.Procurement.PurchaseInvoices.md#purchasepricelist) | [PurchasePriceLists](Logistics.Procurement.PurchasePriceLists.md) (nullable) | The price list, which, when non-null, is used to automatically load unit prices of the products, when entering the invoice manually. [Filter(multi eq)] |
| [ReceivingOrder](Logistics.Procurement.PurchaseInvoices.md#receivingorder) | [ReceivingOrders](Logistics.Procurement.ReceivingOrders.md) (nullable) | The receiving order for the goods that were invoiced. The id is used for 2 or 3 way quantity check. null means that there is no linked RO and the 2 or 3 way check will not include the RO. [Filter(multi eq)] |
| [ResponsiblePerson](Logistics.Procurement.PurchaseInvoices.md#responsibleperson) | [Persons](General.Contacts.Persons.md) (nullable) | The person that is responsible for this order or transaction. It could be the sales person, the orderer, etc. |
| [ReverseOfDocument](Logistics.Procurement.PurchaseInvoices.md#reverseofdocument) | [Documents](General.Documents.md) (nullable) | The document which the current document is reverse of |
| [SaleDealType](Logistics.Procurement.PurchaseInvoices.md#saledealtype) | [DealTypes](Finance.Vat.DealTypes.md) (nullable) | Sale deal type for this purchase invoice. If sale deal type in entered then Sales VAT entry is created for this deal type. [Filter(multi eq)] |
| [Sequence](Logistics.Procurement.PurchaseInvoices.md#sequence) | [Sequences](General.Sequences.md) (nullable) | The sequence that will be used to give new numbers to the documents of this type |
| [Supplier](Logistics.Procurement.PurchaseInvoices.md#supplier) | [Suppliers](Logistics.Procurement.Suppliers.md) | The supplier of the purchase, who is issuing the document. [Required] [Filter(multi eq)] |
| [ToCompanyDivision](Logistics.Procurement.PurchaseInvoices.md#tocompanydivision) | [CompanyDivisions](General.Contacts.CompanyDivisions.md) | The division of the company, receiving the document. null when the document is not received by any specific division |
| [ToParty](Logistics.Procurement.PurchaseInvoices.md#toparty) | [Parties](General.Contacts.Parties.md) (nullable) | The party which should receive the document |
| [UserStatus](Logistics.Procurement.PurchaseInvoices.md#userstatus) | [DocumentTypeUserStatuses](General.DocumentTypeUserStatuses.md) (nullable) | The user status of this document if applicable for this document type. null means unknown or not yet set |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Comments | [DocumentComments](General.DocumentComments.md) | List of [DocumentComment](General.DocumentComments.md) child objects, based on the [DocumentComment.Document](General.DocumentComments.md#document) back reference 
| DistributedAmounts | [DocumentDistributedAmounts](General.DocumentDistributedAmounts.md) | List of [DocumentDistributed<br />Amount](General.DocumentDistributedAmounts.md) child objects, based on the [DocumentDistributedAmount.Document](General.DocumentDistributedAmounts.md#document) back nce 
| DocumentAmounts | [DocumentAmounts](General.DocumentAmounts.md) | List of [DocumentAmount](General.DocumentAmounts.md) child objects, based on the [DocumentAmount.Document](General.DocumentAmounts.md#document) back reference 
| FileAttachments | [DocumentFileAttachments](General.DocumentFileAttachments.md) | List of [DocumentFileAttachment](General.DocumentFileAttachments.md) child objects, based on the [DocumentFileAttachment.Document](General.DocumentFileAttachments.md#document) back reference 
| LineAmounts | [DocumentLineAmounts](General.DocumentLineAmounts.md) | List of [DocumentLineAmount](General.DocumentLineAmounts.md) child objects, based on the [DocumentLineAmount.Document](General.DocumentLineAmounts.md#document) back reference 
| Lines | [PurchaseInvoiceLines](Logistics.Procurement.PurchaseInvoiceLines.md) | List of [PurchaseInvoiceLine](Logistics.Procurement.PurchaseInvoiceLines.md) child objects, based on the [Logistics.Procurement.PurchaseInvoiceLine.PurchaseInvoice](Logistics.Procurement.PurchaseInvoiceLines.md#purchaseinvoice) back reference 
| Prints | [DocumentPrints](General.DocumentPrints.md) | List of [DocumentPrint](General.DocumentPrints.md) child objects, based on the [DocumentPrint.Document](General.DocumentPrints.md#document) back reference 
| StateChanges | [DocumentStateChanges](General.DocumentStateChanges.md) | List of [DocumentStateChange](General.DocumentStateChanges.md) child objects, based on the [DocumentStateChange.Document](General.DocumentStateChanges.md#document) back reference 
| Versions | [DocumentVersions](General.DocumentVersions.md) | List of [DocumentVersion](General.Documents.md#documentversion) child objects, based on the [DocumentVersion.Document](General.DocumentVersions.md#document) back reference 


## Attribute Details

### ApplyDate

> Specifies the date on which to create the VAT ledger entry for this purchase invoice. Usually, this date is equal to the document date, except when the document is received too late to be applied on its original document date. [Required] [Filter(ge;le)]

_Type_: **date**  
_Supported Filters_: **GreaterThanOrLessThan**  
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

### CreditNoteReason

> Reason for the debit/credit note.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### DeliveryTermsCode

> Mode of delivery, like CIF, FOB, etc. Used also in Intrastat reporting.

_Type_: **[DeliveryTerms](Logistics.Procurement.PurchaseInvoices.md#deliverytermscode) (nullable)**  
Generic enum type for DeliveryTerms properties  
_Allowed Values (Finance.Intrastat.DeliveryTerms Enum Members)_  

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

### IntrastatTransactionNatureCode

> Transaction nature; used for Intrastat reporting.

_Type_: **[TransactionNature](Logistics.Procurement.PurchaseInvoices.md#intrastattransactionnaturecode) (nullable)**  
Generic enum type for TransactionNature properties  
_Allowed Values (Finance.Intrastat.TransactionNature Enum Members)_  

| Value | Description |
| ---- | --- |
| OutrightPurchaseOrSale | OutrightPurchaseOrSale value. Stored as '11'. <br /> _Database Value:_ '11' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'OutrightPurchaseOrSale' |
| SupplyForSale | SupplyForSale value. Stored as '12'. <br /> _Database Value:_ '12' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'SupplyForSale' |
| BarterTrade | BarterTrade value. Stored as '13'. <br /> _Database Value:_ '13' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'BarterTrade' |
| FinancialLeasing | FinancialLeasing value. Stored as '14'. <br /> _Database Value:_ '14' <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'FinancialLeasing' |
| OtherTransactions | OtherTransactions value. Stored as '19'. <br /> _Database Value:_ '19' <br /> _Model Value:_ 4 <br /> _Domain API Value:_ 'OtherTransactions' |
| ReturnStokilizing | ReturnStokilizing value. Stored as '21'. <br /> _Database Value:_ '21' <br /> _Model Value:_ 5 <br /> _Domain API Value:_ 'ReturnStokilizing' |
| ReplacementFor<br />ReturnedGoods | ReplacementFor<br />ReturnedGoods value. Stored as '22'. <br /> _Database Value:_ '22' <br /> _Model Value:_ 6 <br /> _Domain API Value:_ 'ReplacementFor<br />ReturnedGoods' |
| ReplacementOfGoods<br />NotBeingReturned | ReplacementOfGoods<br />NotBeingReturned value. Stored as '23'. <br /> _Database Value:_ '23' <br /> _Model Value:_ 7 <br /> _Domain API Value:_ 'ReplacementOfGoods<br />NotBeingReturned' |
| ReturnOrExchange<br />OfOtherGoods | ReturnOrExchange<br />OfOtherGoods value. Stored as '29'. <br /> _Database Value:_ '29' <br /> _Model Value:_ 8 <br /> _Domain API Value:_ 'ReturnOrExchange<br />OfOtherGoods' |
| SpecificTransactions | SpecificTransactions value. Stored as '60'. <br /> _Database Value:_ '60' <br /> _Model Value:_ 9 <br /> _Domain API Value:_ 'SpecificTransactions' |
| OperationsOnJointProjects | OperationsOnJointProjects value. Stored as '70'. <br /> _Database Value:_ '70' <br /> _Model Value:_ 10 <br /> _Domain API Value:_ 'OperationsOnJointProjects' |
| TransactionsOf<br />ConstructionMaterials<br />AndEquipment | TransactionsOf<br />ConstructionMaterials<br />AndEquipment value. Stored as '80'. <br /> _Database Value:_ '80' <br /> _Model Value:_ 11 <br /> _Domain API Value:_ 'TransactionsOf<br />ConstructionMaterials<br />AndEquipment' |
| OtherTransactionsLeasing | OtherTransactionsLeasing value. Stored as '91'. <br /> _Database Value:_ '91' <br /> _Model Value:_ 12 <br /> _Domain API Value:_ 'OtherTransactionsLeasing' |
| OtherTransactionsOther | OtherTransactionsOther value. Stored as '99'. <br /> _Database Value:_ '99' <br /> _Model Value:_ 13 <br /> _Domain API Value:_ 'OtherTransactionsOther' |
| DealsThatInclude<br />PropertyTransfers<br />WithoutFinancial<br />CompensationOr<br />CompensationIn<br />Kind | DealsThatInclude<br />PropertyTransfers<br />WithoutFinancial<br />CompensationOr<br />CompensationIn<br />Kind value. Stored as '30'. <br /> _Database Value:_ '30' <br /> _Model Value:_ 14 <br /> _Domain API Value:_ 'DealsThatInclude<br />PropertyTransfers<br />WithoutFinancial<br />CompensationOr<br />CompensationIn<br />Kind' |
| GoodsThatAreExpected<br />ToBeReturnedTo<br />Sender | GoodsThatAreExpected<br />ToBeReturnedTo<br />Sender value. Stored as '41'. <br /> _Database Value:_ '41' <br /> _Model Value:_ 15 <br /> _Domain API Value:_ 'GoodsThatAreExpected<br />ToBeReturnedTo<br />Sender' |
| GoodsThatAreNot<br />ExpectedToBeReturned<br />ToSender | GoodsThatAreNot<br />ExpectedToBeReturned<br />ToSender value. Stored as '42'. <br /> _Database Value:_ '42' <br /> _Model Value:_ 16 <br /> _Domain API Value:_ 'GoodsThatAreNot<br />ExpectedToBeReturned<br />ToSender' |
| GoodsThatAreReturned<br />ToSender | GoodsThatAreReturned<br />ToSender value. Stored as '51'. <br /> _Database Value:_ '51' <br /> _Model Value:_ 17 <br /> _Domain API Value:_ 'GoodsThatAreReturned<br />ToSender' |
| GoodsThatAreNot<br />ReturnedToSender | GoodsThatAreNot<br />ReturnedToSender value. Stored as '52'. <br /> _Database Value:_ '52' <br /> _Model Value:_ 18 <br /> _Domain API Value:_ 'GoodsThatAreNot<br />ReturnedToSender' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### IntrastatTransportModeCode

> Transport mode; used for Intrastat reporting.

_Type_: **[TransportMode](Logistics.Procurement.PurchaseInvoices.md#intrastattransportmodecode) (nullable)**  
Generic enum type for TransportMode properties  
_Allowed Values (Finance.Intrastat.TransportMode Enum Members)_  

| Value | Description |
| ---- | --- |
| Shipping | Shipping value. Stored as '1'. <br /> _Database Value:_ '1' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Shipping' |
| RailwayTransport | RailwayTransport value. Stored as '2'. <br /> _Database Value:_ '2' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'RailwayTransport' |
| RoadTransport | RoadTransport value. Stored as '3'. <br /> _Database Value:_ '3' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'RoadTransport' |
| AirTransport | AirTransport value. Stored as '4'. <br /> _Database Value:_ '4' <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'AirTransport' |
| Mail | Mail value. Stored as '5'. <br /> _Database Value:_ '5' <br /> _Model Value:_ 4 <br /> _Domain API Value:_ 'Mail' |
| FixedTransport<br />Installations | FixedTransport<br />Installations value. Stored as '6'. <br /> _Database Value:_ '6' <br /> _Model Value:_ 5 <br /> _Domain API Value:_ 'FixedTransport<br />Installations' |
| RiverTransport | RiverTransport value. Stored as '7'. <br /> _Database Value:_ '7' <br /> _Model Value:_ 6 <br /> _Domain API Value:_ 'RiverTransport' |
| SelfPropelled | SelfPropelled value. Stored as '8'. <br /> _Database Value:_ '8' <br /> _Model Value:_ 7 <br /> _Domain API Value:_ 'SelfPropelled' |

_Supported Filters_: **NotFilterable**  
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

### ParentDocumentRelationshipType

> Type of relationship between the current document and the parent document(s). Affects the constraints for execution/completion for the documents. Possible values: 'S' = 'Subtask', 'N' = 'Next task'.

_Type_: **[ParentDocument<br />RelationshipType](Logistics.Procurement.PurchaseInvoices.md#parentdocumentrelationshiptype) (nullable)**  
Relationship between parent and child documents  
_Allowed Values (General.ParentDocumentRelationshipType Enum Members)_  

| Value | Description |
| ---- | --- |
| Subtask | The child document is a sub-task of the parent document. (Complete child to complete parent) <br /> _Database Value:_ 'S' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Subtask' |
| NextTask | The child document is next task of the parent document. (Complete parent to complete child) <br /> _Database Value:_ 'N' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'NextTask' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### PaymentDueDate

> Due date for paying the invoice. null means to use the default . [Filter(ge;le)]

_Type_: **datetime (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
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

_Type_: **[DocumentState](Logistics.Procurement.PurchaseInvoices.md#state)**  
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

### VATCashReportingMode

> When True, indicates, that this invoice uses the special 'Cash reporting mode' when creating VAT ledger entries. [Required] [Default(false)] [Filter(multi eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### VATNotes

> Description of the operation that will be entered in the VAT ledgers.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
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

### CostCenter

> Cost center for which the amount from this document will be accounted. [Filter(multi eq)]

_Type_: **[CostCenters](Finance.Accounting.CostCenters.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### CreditNoteOriginalPurchaseInvoice

> The original invoice, which is debited/credited with this note. [Filter(multi eq)]

_Type_: **[PurchaseInvoices](Logistics.Procurement.PurchaseInvoices.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### CurrencyDirectory

> The currency directory, containing all the convertion rates, used by the document. null means that the document does not need currency convertions

_Type_: **[CurrencyDirectories](General.CurrencyDirectories.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### DealType

> Deal type for this purchase invoice. If deal type in entered then VAT entry is created for this deal type. [Filter(multi eq)]

_Type_: **[DealTypes](Finance.Vat.DealTypes.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### DocumentCurrency

> The currency of the unit prices and amounts in the document. [Required] [Filter(multi eq)]

_Type_: **[Currencies](General.Currencies.md)**  
_Supported Filters_: **Equals, EqualsIn**  

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

### IntrastatDestinationRegion

> Region, which is the final destination of the goods. Used for Intrastat reporting. When this is non-null, it applies to the whole document. [Filter(multi eq)]

_Type_: **[AdministrativeRegions](General.Geography.AdministrativeRegions.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### IntrastatTransportCountry

> Country of origin of the transport company; used for Intrastat reporting. [Filter(multi eq)]

_Type_: **[Countries](General.Geography.Countries.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### MasterDocument

> In a multi-document tree, this is the root document, that created the whole tree. If this is the root it is equal to Id [Required]

_Type_: **[Documents](General.Documents.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### Parent

> In a multi-document tree, this is the direct parent document. If this is the root it is null

_Type_: **[Documents](General.Documents.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### PaymentAccount

> When not null, specifies the default payment account for the payment order. [Filter(multi eq)]

_Type_: **[PaymentAccounts](Finance.Payments.PaymentAccounts.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### PaymentType

> The payment type to be used. null is allowed only temporary and should be specified if payment order is to be generated. [Filter(multi eq)]

_Type_: **[PaymentTypes](Finance.Payments.PaymentTypes.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### PrimeCauseDocument

> The document that is the prime cause for creation of the current document

_Type_: **[Documents](General.Documents.md) (nullable)**  
_Supported Filters_: **EqualsIn**  

### PurchaseOrder

> The purchase order that was sent to the supplier and is the base for the invoice. null means there is no linked PO and 3 way check won't be performed. [Filter(multi eq)]

_Type_: **[PurchaseOrders](Logistics.Procurement.PurchaseOrders.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### PurchasePriceList

> The price list, which, when non-null, is used to automatically load unit prices of the products, when entering the invoice manually. [Filter(multi eq)]

_Type_: **[PurchasePriceLists](Logistics.Procurement.PurchasePriceLists.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### ReceivingOrder

> The receiving order for the goods that were invoiced. The id is used for 2 or 3 way quantity check. null means that there is no linked RO and the 2 or 3 way check will not include the RO. [Filter(multi eq)]

_Type_: **[ReceivingOrders](Logistics.Procurement.ReceivingOrders.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### ResponsiblePerson

> The person that is responsible for this order or transaction. It could be the sales person, the orderer, etc.

_Type_: **[Persons](General.Contacts.Persons.md) (nullable)**  
_Supported Filters_: **EqualsIn**  

### ReverseOfDocument

> The document which the current document is reverse of

_Type_: **[Documents](General.Documents.md) (nullable)**  
_Supported Filters_: **EqualsIn**  

### SaleDealType

> Sale deal type for this purchase invoice. If sale deal type in entered then Sales VAT entry is created for this deal type. [Filter(multi eq)]

_Type_: **[DealTypes](Finance.Vat.DealTypes.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### Sequence

> The sequence that will be used to give new numbers to the documents of this type

_Type_: **[Sequences](General.Sequences.md) (nullable)**  
_Supported Filters_: **EqualsIn**  

### Supplier

> The supplier of the purchase, who is issuing the document. [Required] [Filter(multi eq)]

_Type_: **[Suppliers](Logistics.Procurement.Suppliers.md)**  
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

[!list erp.entity=Logistics.Procurement.PurchaseInvoices erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Logistics.Procurement.PurchaseInvoices erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Logistics.Procurement.PurchaseInvoices erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_Procurement_PurchaseInvoices?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_Procurement_PurchaseInvoices?$top=10>

