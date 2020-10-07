# General.DocumentDistributedAmounts

Contains the amounts which are distributed by the system over the document lines as a result of additional amount calculations. Entity: Gen_Document_Distributed_Amounts

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](General.DocumentDistributedAmounts.md#Id) | guid |  
| [Amount](General.DocumentDistributedAmounts.md#Amount) | [Amount](../data-types/Amount.md) | The amount which has beed distributed over the current line. The amount is in the currency of the document. [Currency: GetDocumentCurrency()] [Required] [Filter(ge;le)] 
| [DocumentLineId](General.DocumentDistributedAmounts.md#DocumentLineId) | guid (nullable) | The Id of the line over which the amount is distributed. [Filter(multi eq)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [DocumentAmountType](General.DocumentDistributedAmounts.md#DocumentAmountType) | [General.DocumentAmountTypes](General.DocumentAmountTypes.md) | The type of amount which is distributed. [Required] [Filter(multi eq)] |
| [Document](General.DocumentDistributedAmounts.md#Document) | [General.Documents](General.Documents.md) | The [Document](General.DocumentDistributedAmounts.md#Document) to which this DocumentDistributedAmount belongs. [Required] [Filter(multi eq)] [Owner] |
| [ReferencedDocument](General.DocumentDistributedAmounts.md#ReferencedDocument) | [General.Documents](General.Documents.md) (nullable) | In not null the Document_Line_Id is a line of the document with Referenced_Document_Id. [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### Amount

> The amount which has beed distributed over the current line. The amount is in the currency of the document. [Currency: GetDocumentCurrency()] [Required] [Filter(ge;le)]

_Type_: **[Amount](../data-types/Amount.md)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### DocumentLineId

> The Id of the line over which the amount is distributed. [Filter(multi eq)]

_Type_: **guid (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  


## Reference Details

### DocumentAmountType

> The type of amount which is distributed. [Required] [Filter(multi eq)]

_Type_: **[General.DocumentAmountTypes](General.DocumentAmountTypes.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Document

> The [Document](General.DocumentDistributedAmounts.md#Document) to which this DocumentDistributedAmount belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[General.Documents](General.Documents.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### ReferencedDocument

> In not null the Document_Line_Id is a line of the document with Referenced_Document_Id. [Filter(multi eq)]

_Type_: **[General.Documents](General.Documents.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=General.DocumentDistributedAmounts erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.DocumentDistributedAmounts erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=General.DocumentDistributedAmounts erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_DocumentDistributedAmounts?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_DocumentDistributedAmounts?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Gen_Document_Distributed_Amounts?$top=10>

