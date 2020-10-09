---
uid: General.DocumentDistributedAmounts
---
# General.DocumentDistributedAmounts Entity

Contains the amounts which are distributed by the system over the document lines as a result of additional amount calculations. Entity: Gen_Document_Distributed_Amounts

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Amount](General.DocumentDistributedAmounts.md#amount) | [Amount](../data-types.md#amount) | The amount which has beed distributed over the current line. The amount is in the currency of the document. [Currency: GetDocumentCurrency()] [Required] [Filter(ge;le)] 
| [DocumentLineId](General.DocumentDistributedAmounts.md#documentlineid) | guid (nullable) | The Id of the line over which the amount is distributed. [Filter(multi eq)] 
| [Id](General.DocumentDistributedAmounts.md#id) | guid |  

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Document](General.DocumentDistributedAmounts.md#document) | [Documents](General.Documents.md) | The [Document](General.DocumentDistributedAmounts.md#document) to which this DocumentDistributedAmount belongs. [Required] [Filter(multi eq)] [Owner] |
| [DocumentAmountType](General.DocumentDistributedAmounts.md#documentamounttype) | [DocumentAmountTypes](General.DocumentAmountTypes.md) | The type of amount which is distributed. [Required] [Filter(multi eq)] |
| [ReferencedDocument](General.DocumentDistributedAmounts.md#referenceddocument) | [Documents](General.Documents.md) (nullable) | In not null the Document_Line_Id is a line of the document with Referenced_Document_Id. [Filter(multi eq)] |


## Attribute Details

### Amount

The amount which has beed distributed over the current line. The amount is in the currency of the document. [Currency: GetDocumentCurrency()] [Required] [Filter(ge;le)]

_Type_: **[Amount](../data-types.md#amount)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### DocumentLineId

The Id of the line over which the amount is distributed. [Filter(multi eq)]

_Type_: **guid (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  


## Reference Details

### Document

The [Document](General.DocumentDistributedAmounts.md#document) to which this DocumentDistributedAmount belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Documents](General.Documents.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### DocumentAmountType

The type of amount which is distributed. [Required] [Filter(multi eq)]

_Type_: **[DocumentAmountTypes](General.DocumentAmountTypes.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### ReferencedDocument

In not null the Document_Line_Id is a line of the document with Referenced_Document_Id. [Filter(multi eq)]

_Type_: **[Documents](General.Documents.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  



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

