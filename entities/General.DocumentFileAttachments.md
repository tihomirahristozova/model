---
uid: General.DocumentFileAttachments
---
# General.DocumentFileAttachments Entity

**Namespace:** [General](General.md)  

Contains files, attached to the documents. Entity: Gen_Document_File_Attachments

## Default Visualization
Default Display Text Format:  
_{FileName}_  
Default Search Members:  
_FileName_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[General.Documents](General.Documents.md)  
Aggregate Root:  
[General.Documents](General.Documents.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [EmbeddedFileContents](General.DocumentFileAttachments.md#embeddedfilecontents) | byte[] __nullable__ | The contents of the embedded file. null when the file is linked. 
| [FileName](General.DocumentFileAttachments.md#filename) | string (128) | The display name of the file. Initially set to the file name (without path) of the linked or the embedded file. `Required` 
| [Id](General.DocumentFileAttachments.md#id) | guid |  
| [IsLinked](General.DocumentFileAttachments.md#islinked) | boolean | True when the document is linked (ony file name is kept). false when the document is embedded. `Required` `Default(false)` `Filter(eq)` 
| [LinkedFilePath](General.DocumentFileAttachments.md#linkedfilepath) | string (254) __nullable__ | Path to the linked file. null when the file is embedded. 
| [Notes](General.DocumentFileAttachments.md#notes) | string (max) __nullable__ | Notes for this DocumentFileAttachment. 
| [RowVersion](General.DocumentFileAttachments.md#rowversion) | byte[] |  

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Document](General.DocumentFileAttachments.md#document) | [Documents](General.Documents.md) | The <see cref="Document"/> to which this DocumentFileAttachment belongs. `Required` `Filter(multi eq)` `Owner` |


## Attribute Details

### EmbeddedFileContents

The contents of the embedded file. null when the file is linked.

_Type_: **byte[] __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### FileName

The display name of the file. Initially set to the file name (without path) of the linked or the embedded file. `Required`

_Type_: **string (128)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **128**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### IsLinked

True when the document is linked (ony file name is kept). false when the document is embedded. `Required` `Default(false)` `Filter(eq)`

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### LinkedFilePath

Path to the linked file. null when the file is embedded.

_Type_: **string (254) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  

### Notes

Notes for this DocumentFileAttachment.

_Type_: **string (max) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  

### RowVersion

_Type_: **byte[]**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### Document

The <see cref="Document"/> to which this DocumentFileAttachment belongs. `Required` `Filter(multi eq)` `Owner`

_Type_: **[Documents](General.Documents.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  



## Business Rules

[!list limit=1000 erp.entity=General.DocumentFileAttachments erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=General.DocumentFileAttachments erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_DocumentFileAttachments?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_DocumentFileAttachments?$top=10>

