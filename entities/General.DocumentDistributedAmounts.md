---
uid: General.DocumentDistributedAmounts
---
# General.DocumentDistributedAmounts Entity

**Namespace:** [General](General.md)  

Contains the amounts which are distributed by the system over the document lines as a result of additional amount calculations. Entity: Gen_Document_Distributed_Amounts

## Default Visualization
Default Display Text Format:  
_{Document.EntityName}_  
Default Search Members:  
_Document.EntityName_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[General.Documents](General.Documents.md)  
Aggregate Root:  
[General.Documents](General.Documents.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Amount](General.DocumentDistributedAmounts.md#amount) | [Amount (14, 2)](../data-types.md#amount) | The amount which has beed distributed over the current line. The amount is in the currency of the document. `Currency: GetDocumentCurrency()` `Required` `Filter(ge;le)` 
| [BaseAmount](General.DocumentDistributedAmounts.md#baseamount) | [Amount (14, 2)](../data-types.md#amount) __nullable__ | The calculated base amount for the line in document currency. The base amount is the base, over which the additional amounts are calculated. Null if the base amount is not stored (for amounts distributed in older versions of the system). . `Currency: GetDocumentCurrency()` `Introduced in version 22.1.4.44` 
| [DocumentLineId](General.DocumentDistributedAmounts.md#documentlineid) | guid __nullable__ | The Id of the line over which the amount is distributed. `Filter(multi eq)` 
| [Id](General.DocumentDistributedAmounts.md#id) | guid |  
| [ObjectVersion](General.DocumentDistributedAmounts.md#objectversion) | int32 |  

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Document](General.DocumentDistributedAmounts.md#document) | [Documents](General.Documents.md) | The <see cref="Document"/> to which this DocumentDistributedAmount belongs. `Required` `Filter(multi eq)` `Owner` |
| [DocumentAmountType](General.DocumentDistributedAmounts.md#documentamounttype) | [DocumentAmountTypes](General.DocumentAmountTypes.md) | The type of amount which is distributed. `Required` `Filter(multi eq)` |
| [ReferencedDocument](General.DocumentDistributedAmounts.md#referenceddocument) | [Documents](General.Documents.md) (nullable) | In not null the Document_Line_Id is a line of the document with Referenced_Document_Id. `Filter(multi eq)` |


## Attribute Details

### Amount

The amount which has beed distributed over the current line. The amount is in the currency of the document. `Currency: GetDocumentCurrency()` `Required` `Filter(ge;le)`

_Type_: **[Amount (14, 2)](../data-types.md#amount)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### BaseAmount

The calculated base amount for the line in document currency. The base amount is the base, over which the additional amounts are calculated. Null if the base amount is not stored (for amounts distributed in older versions of the system). . `Currency: GetDocumentCurrency()` `Introduced in version 22.1.4.44`

_Type_: **[Amount (14, 2)](../data-types.md#amount) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### DocumentLineId

The Id of the line over which the amount is distributed. `Filter(multi eq)`

_Type_: **guid __nullable__**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### ObjectVersion

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  


## Reference Details

### Document

The <see cref="Document"/> to which this DocumentDistributedAmount belongs. `Required` `Filter(multi eq)` `Owner`

_Type_: **[Documents](General.Documents.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  

### DocumentAmountType

The type of amount which is distributed. `Required` `Filter(multi eq)`

_Type_: **[DocumentAmountTypes](General.DocumentAmountTypes.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### ReferencedDocument

In not null the Document_Line_Id is a line of the document with Referenced_Document_Id. `Filter(multi eq)`

_Type_: **[Documents](General.Documents.md) (nullable)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list limit=1000 erp.entity=General.DocumentDistributedAmounts erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=General.DocumentDistributedAmounts erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_DocumentDistributedAmounts?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_DocumentDistributedAmounts?$top=10>

