---
uid: Finance.Intrastat.Declarations
---
# Finance.Intrastat.Declarations Entity

Contains the headers of the Intrastat declarations, issued by the enterprise companies. Entity: Its_Declarations

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [CompleteTime](Finance.Intrastat.Declarations.md#completetime) | datetime (nullable) | Exact time, when the document was last completed[Filter(ge;le)] 
| [CreationTime](Finance.Intrastat.Declarations.md#creationtime) | datetime | Date/Time when the document was created [Required][Filter(ge;le)] 
| [CreationUser](Finance.Intrastat.Declarations.md#creationuser) | string | The login name of the user, who created the document [Required][Filter(like)] 
| [DeclarationFunction](Finance.Intrastat.Declarations.md#declarationfunction) | [DeclarationFunction](Finance.Intrastat.Declarations.md#declarationfunction) | Specifies whether this is a regular or corrective declaration. R=Regular, C=Corrective. [Required] [Default("R")] [Filter(eq)] 
| [DeclareStatisticalValues](Finance.Intrastat.Declarations.md#declarestatisticalvalues) | boolean | Does the declaration contain statistical values? true=Yes; false=No. [Required] [Default(false)] [Filter(multi eq)] 
| [DocumentDate](Finance.Intrastat.Declarations.md#documentdate) | datetime | The date on which the document was issued [Required][Filter(eq;ge;le)][ORD] 
| [DocumentNo](Finance.Intrastat.Declarations.md#documentno) | string | Document number, unique within Document_Type_Id [Required][Filter(eq;like)][ORD] 
| [DocumentNotes](Finance.Intrastat.Declarations.md#documentnotes) | string (nullable) | Notes for this Document 
| [DocumentVersion](Finance.Intrastat.Declarations.md#documentversion) | int32 | [Filter(eq;ge;le)] 
| [EntityName](Finance.Intrastat.Declarations.md#entityname) | string | The entity name of the document equal to the entity name of the document type.[Filter(eq)] [ORD] 
| [GoodsFlowDirection](Finance.Intrastat.Declarations.md#goodsflowdirection) | [GoodsFlowDirection](Finance.Intrastat.Declarations.md#goodsflowdirection) | The flow direction of the goods. A=Arrival, D=Dispatch. [Required] [Filter(eq)] 
| [Id](Finance.Intrastat.Declarations.md#id) | guid |  
| [IsReleased](Finance.Intrastat.Declarations.md#isreleased) | boolean | True if the document is not void and its state is released or greater. [Required] [Default(false)] [Filter(eq)] [ReadOnly] 
| [IsSingleExecution](Finance.Intrastat.Declarations.md#issingleexecution) | boolean | Specifies whether the document is a single execution of its order document. [Required] [Default(false)] [Filter(eq)] [ReadOnly] 
| [ParentDocument<br />RelationshipType](Finance.Intrastat.Declarations.md#parentdocumentrelationshiptype) | [ParentDocument<br />RelationshipType](Finance.Intrastat.Declarations.md#parentdocumentrelationshiptype) (nullable) | Type of relationship between the current document and the parent document(s). Affects the constraints for execution/completion for the documents. Possible values: 'S' = 'Subtask', 'N' = 'Next task'. 
| [PlanningOnly](Finance.Intrastat.Declarations.md#planningonly) | boolean (nullable) | Indicates that the document is used only for planning (and as consequence its state cannot be greater than Planned) [Required] 
| [PostalCode](Finance.Intrastat.Declarations.md#postalcode) | string | This field contains the postal code part of the submitter’s address. [Required] 
| [ReadOnly](Finance.Intrastat.Declarations.md#readonly) | boolean | True - the document is read only; false - the document is not read only [Required] 
| [ReferenceDate](Finance.Intrastat.Declarations.md#referencedate) | datetime (nullable) | The date to which this document refers, i.e. when the action really occurred. If null, Document_Date is taken [Filter(ge;le)] 
| [ReferenceDocumentNo](Finance.Intrastat.Declarations.md#referencedocumentno) | string (nullable) | The number of the document (issued by the other party), which was the reason for the creation of the current document. The numebr should be unique within the party documents [Filter(eq;like)] 
| [ReferenceMonth](Finance.Intrastat.Declarations.md#referencemonth) | [ReferenceMonth](Finance.Intrastat.Declarations.md#referencemonth) | Month, for which the declaration is prepared. [Required] [Filter(eq)] 
| [ReferenceYear](Finance.Intrastat.Declarations.md#referenceyear) | int16 | Year, for which the declaration is prepared. [Required] [Filter(eq)] 
| [ReleaseTime](Finance.Intrastat.Declarations.md#releasetime) | datetime (nullable) | Exact time, when the document was first released [Filter(ge;le)] 
| [State](Finance.Intrastat.Declarations.md#state) | [DocumentState](Finance.Intrastat.Declarations.md#state) | 0=New;5=Corrective;10=Computer Planned;20=Human Planned;30=Released;40=Completed;50=Closed [Required][Filter(eq;ge;le)] 
| [Void](Finance.Intrastat.Declarations.md#void) | boolean | True if the document is null and void [Required][Filter(eq)] 
| [VoidReason](Finance.Intrastat.Declarations.md#voidreason) | string (nullable) | Reason for voiding the document, entered by the user 
| [VoidTime](Finance.Intrastat.Declarations.md#voidtime) | datetime (nullable) | Date/time when the document has become void 
| [VoidUser](Finance.Intrastat.Declarations.md#voiduser) | string (nullable) | The user who voided the document 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [AccessKey](Finance.Intrastat.Declarations.md#accesskey) | [AccessKeys](Systems.Security.AccessKeys.md) (nullable) | The access key, containing the user permissions for this document. null means that all users have unlimited permissions |
| [AdjustedDocument](Finance.Intrastat.Declarations.md#adjusteddocument) | [Documents](General.Documents.md) (nullable) | The primary document, which the current document adjusts. null when this is not an adjustment document |
| [AssignedToUser](Finance.Intrastat.Declarations.md#assignedtouser) | [Users](Systems.Security.Users.md) (nullable) | The user to which this document is assigned for handling. null means that the document is not assigned to specific user |
| [AuthorizedPerson](Finance.Intrastat.Declarations.md#authorizedperson) | [Persons](General.Contacts.Persons.md) (nullable) | The authorized person who submits the intrastat declaration. [Filter(multi eq)] [Introduced in version 18.2] |
| [CurrencyDirectory](Finance.Intrastat.Declarations.md#currencydirectory) | [CurrencyDirectories](General.CurrencyDirectories.md) (nullable) | The currency directory, containing all the convertion rates, used by the document. null means that the document does not need currency convertions |
| [DocumentType](Finance.Intrastat.Declarations.md#documenttype) | [DocumentTypes](General.DocumentTypes.md) | The user defined type of the document. Determines document behaviour, properties, additional amounts, validation, generations, etc. [Required] |
| [EnterpriseCompany](Finance.Intrastat.Declarations.md#enterprisecompany) | [EnterpriseCompanies](General.EnterpriseCompanies.md) | The enterprise company which issued the document [Required] |
| [EnterpriseCompanyLocation](Finance.Intrastat.Declarations.md#enterprisecompanylocation) | [CompanyLocations](General.Contacts.CompanyLocations.md) (nullable) | The enterprise company location which issued the document. null means that there is only one location within the enterprise company and locations are not used |
| [FromCompanyDivision](Finance.Intrastat.Declarations.md#fromcompanydivision) | [CompanyDivisions](General.Contacts.CompanyDivisions.md) (nullable) | The division of the company, issuing the document. null when the document is not issued by any specific division |
| [FromParty](Finance.Intrastat.Declarations.md#fromparty) | [Parties](General.Contacts.Parties.md) | The party which issued the document [Required] |
| [MasterDocument](Finance.Intrastat.Declarations.md#masterdocument) | [Documents](General.Documents.md) | In a multi-document tree, this is the root document, that created the whole tree. If this is the root it is equal to Id [Required] |
| [Parent](Finance.Intrastat.Declarations.md#parent) | [Documents](General.Documents.md) (nullable) | In a multi-document tree, this is the direct parent document. If this is the root it is null |
| [PrimeCauseDocument](Finance.Intrastat.Declarations.md#primecausedocument) | [Documents](General.Documents.md) (nullable) | The document that is the prime cause for creation of the current document |
| [ResponsiblePerson](Finance.Intrastat.Declarations.md#responsibleperson) | [Persons](General.Contacts.Persons.md) (nullable) | The person that is responsible for this order or transaction. It could be the sales person, the orderer, etc. |
| [ReverseOfDocument](Finance.Intrastat.Declarations.md#reverseofdocument) | [Documents](General.Documents.md) (nullable) | The document which the current document is reverse of |
| [Sequence](Finance.Intrastat.Declarations.md#sequence) | [Sequences](General.Sequences.md) (nullable) | The sequence that will be used to give new numbers to the documents of this type |
| [ThirdDeclaringParty](Finance.Intrastat.Declarations.md#thirddeclaringparty) | [Companies](General.Contacts.Companies.md) | Third declaring party, which holds the electronic signature. This is the company which submits the declaration. [Required] [Filter(multi eq)] [Introduced in version 18.2] |
| [ToCompanyDivision](Finance.Intrastat.Declarations.md#tocompanydivision) | [CompanyDivisions](General.Contacts.CompanyDivisions.md) | The division of the company, receiving the document. null when the document is not received by any specific division |
| [ToParty](Finance.Intrastat.Declarations.md#toparty) | [Parties](General.Contacts.Parties.md) (nullable) | The party which should receive the document |
| [UserStatus](Finance.Intrastat.Declarations.md#userstatus) | [DocumentTypeUserStatuses](General.DocumentTypeUserStatuses.md) (nullable) | The user status of this document if applicable for this document type. null means unknown or not yet set |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Comments | [DocumentComments](General.DocumentComments.md) | List of [DocumentComment](General.DocumentComments.md) child objects, based on the [DocumentComment.Document](General.DocumentComments.md#document) back reference 
| DistributedAmounts | [DocumentDistributedAmounts](General.DocumentDistributedAmounts.md) | List of [DocumentDistributed<br />Amount](General.DocumentDistributedAmounts.md) child objects, based on the [DocumentDistributedAmount.Document](General.DocumentDistributedAmounts.md#document) back reference 
| DocumentAmounts | [DocumentAmounts](General.DocumentAmounts.md) |  
| FileAttachments | [DocumentFileAttachments](General.DocumentFileAttachments.md) | List of [DocumentFileAttachment](General.DocumentFileAttachments.md) child objects, based on the [DocumentFileAttachment.Document](General.DocumentFileAttachments.md#document) back reference 
| LineAmounts | [DocumentLineAmounts](General.DocumentLineAmounts.md) | List of [DocumentLineAmount](General.DocumentLineAmounts.md) child objects, based on the [DocumentLineAmount.Document](General.DocumentLineAmounts.md#document) back reference 
| Lines | [DeclarationLines](Finance.Intrastat.DeclarationLines.md) | List of [DeclarationLine](Finance.Intrastat.DeclarationLines.md) child objects, based on the [Finance.Intrastat.DeclarationLine.IntrastatDeclaration](Finance.Intrastat.DeclarationLines.md#intrastatdeclaration) back reference 
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

### DeclarationFunction

Specifies whether this is a regular or corrective declaration. R=Regular, C=Corrective. [Required] [Default("R")] [Filter(eq)]

_Type_: **[DeclarationFunction](Finance.Intrastat.Declarations.md#declarationfunction)**  
Allowed values for the [DeclarationFunction](Finance.Intrastat.Declarations.md#declarationfunction) data attribute  
_Allowed Values (Finance.Intrastat.DeclarationsRepository.DeclarationFunction Enum Members)_  

| Value | Description |
| ---- | --- |
| Regular | Regular value. Stored as 'R'. <br /> _Database Value:_ 'R' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Regular' |
| Corrective | Corrective value. Stored as 'C'. <br /> _Database Value:_ 'C' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'Corrective' |

_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **Regular**  

### DeclareStatisticalValues

Does the declaration contain statistical values? true=Yes; false=No. [Required] [Default(false)] [Filter(multi eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **False**  

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

### GoodsFlowDirection

The flow direction of the goods. A=Arrival, D=Dispatch. [Required] [Filter(eq)]

_Type_: **[GoodsFlowDirection](Finance.Intrastat.Declarations.md#goodsflowdirection)**  
Allowed values for the [GoodsFlowDirection](Finance.Intrastat.Declarations.md#goodsflowdirection) data attribute  
_Allowed Values (Finance.Intrastat.DeclarationsRepository.GoodsFlowDirection Enum Members)_  

| Value | Description |
| ---- | --- |
| Arrival | Arrival value. Stored as 'A'. <br /> _Database Value:_ 'A' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Arrival' |
| Dispatch | Dispatch value. Stored as 'D'. <br /> _Database Value:_ 'D' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'Dispatch' |

_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

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

Type of relationship between the current document and the parent document(s). Affects the constraints for execution/completion for the documents. Possible values: 'S' = 'Subtask', 'N' = 'Next task'.

_Type_: **[ParentDocument<br />RelationshipType](Finance.Intrastat.Declarations.md#parentdocumentrelationshiptype) (nullable)**  
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

### PostalCode

This field contains the postal code part of the submitter’s address. [Required]

_Type_: **string**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

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

### ReferenceMonth

Month, for which the declaration is prepared. [Required] [Filter(eq)]

_Type_: **[ReferenceMonth](Finance.Intrastat.Declarations.md#referencemonth)**  
Allowed values for the [ReferenceMonth](Finance.Intrastat.Declarations.md#referencemonth) data attribute  
_Allowed Values (Finance.Intrastat.DeclarationsRepository.ReferenceMonth Enum Members)_  

| Value | Description |
| ---- | --- |
| January | January value. Stored as 1. <br /> _Database Value:_ 1 <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'January' |
| February | February value. Stored as 2. <br /> _Database Value:_ 2 <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'February' |
| March | March value. Stored as 3. <br /> _Database Value:_ 3 <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'March' |
| April | April value. Stored as 4. <br /> _Database Value:_ 4 <br /> _Model Value:_ 4 <br /> _Domain API Value:_ 'April' |
| May | May value. Stored as 5. <br /> _Database Value:_ 5 <br /> _Model Value:_ 5 <br /> _Domain API Value:_ 'May' |
| June | June value. Stored as 6. <br /> _Database Value:_ 6 <br /> _Model Value:_ 6 <br /> _Domain API Value:_ 'June' |
| July | July value. Stored as 7. <br /> _Database Value:_ 7 <br /> _Model Value:_ 7 <br /> _Domain API Value:_ 'July' |
| August | August value. Stored as 8. <br /> _Database Value:_ 8 <br /> _Model Value:_ 8 <br /> _Domain API Value:_ 'August' |
| September | September value. Stored as 9. <br /> _Database Value:_ 9 <br /> _Model Value:_ 9 <br /> _Domain API Value:_ 'September' |
| October | October value. Stored as 10. <br /> _Database Value:_ 10 <br /> _Model Value:_ 10 <br /> _Domain API Value:_ 'October' |
| November | November value. Stored as 11. <br /> _Database Value:_ 11 <br /> _Model Value:_ 11 <br /> _Domain API Value:_ 'November' |
| December | December value. Stored as 12. <br /> _Database Value:_ 12 <br /> _Model Value:_ 12 <br /> _Domain API Value:_ 'December' |

_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

### ReferenceYear

Year, for which the declaration is prepared. [Required] [Filter(eq)]

_Type_: **int16**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

### ReleaseTime

Exact time, when the document was first released [Filter(ge;le)]

_Type_: **datetime (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### State

0=New;5=Corrective;10=Computer Planned;20=Human Planned;30=Released;40=Completed;50=Closed [Required][Filter(eq;ge;le)]

_Type_: **[DocumentState](Finance.Intrastat.Declarations.md#state)**  
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

### AuthorizedPerson

The authorized person who submits the intrastat declaration. [Filter(multi eq)] [Introduced in version 18.2]

_Type_: **[Persons](General.Contacts.Persons.md) (nullable)**  
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

### ThirdDeclaringParty

Third declaring party, which holds the electronic signature. This is the company which submits the declaration. [Required] [Filter(multi eq)] [Introduced in version 18.2]

_Type_: **[Companies](General.Contacts.Companies.md)**  
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

[!list erp.entity=Finance.Intrastat.Declarations erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Finance.Intrastat.Declarations erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Finance.Intrastat.Declarations erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Intrastat_Declarations?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Intrastat_Declarations?$top=10>

