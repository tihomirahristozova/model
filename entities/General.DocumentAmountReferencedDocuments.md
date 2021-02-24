---
uid: General.DocumentAmountReferencedDocuments
---
# General.DocumentAmountReferencedDocuments Entity

Contains the documents which are referenced by each document amount. Entity: Gen_Document_Amount_Referenced_Documents

Default Display Text Format:  
_{DocumentAmount.Document.DocumentType.Code}:{DocumentAmount.Document.DocumentNo} - {DocumentAmount.Document.DocumentType.TypeName:T}_  
Default Search Member:  
_DocumentAmount.Document.DocumentType.Code_  

[Aggregate](xref:aggregates) Parent:  
[General.DocumentAmounts](General.DocumentAmounts.md)  
[Aggregate](xref:aggregates) Root:  
[General.Documents](General.Documents.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](General.DocumentAmountReferencedDocuments.md#id) | guid |  

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [DocumentAmount](General.DocumentAmountReferencedDocuments.md#documentamount) | [DocumentAmounts](General.DocumentAmounts.md) | The document amount for which the referenced document is specified. [Required] [Filter(multi eq)] [Owner] |
| [ReferencedDocument](General.DocumentAmountReferencedDocuments.md#referenceddocument) | [Documents](General.Documents.md) | The document which is referenced by the document amount. [Required] [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  


## Reference Details

### DocumentAmount

The document amount for which the referenced document is specified. [Required] [Filter(multi eq)] [Owner]

_Type_: **[DocumentAmounts](General.DocumentAmounts.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  

### ReferencedDocument

The document which is referenced by the document amount. [Required] [Filter(multi eq)]

_Type_: **[Documents](General.Documents.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=General.DocumentAmountReferencedDocuments erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.DocumentAmountReferencedDocuments erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_DocumentAmountReferencedDocuments?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_DocumentAmountReferencedDocuments?$top=10>

