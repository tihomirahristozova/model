---
uid: General.DocumentFileAttachments
---
# General.DocumentFileAttachments Entity

Contains files, attached to the documents. Entity: Gen_Document_File_Attachments

Default Display Text Format:  
_{FileName:T}_  
Default Search Member:  
_FileName_  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [EmbeddedFileContents](General.DocumentFileAttachments.md#embeddedfilecontents) | byte[] (nullable) | The contents of the embedded file. null when the file is linked. 
| [FileName](General.DocumentFileAttachments.md#filename) | string | The display name of the file. Initially set to the file name (without path) of the linked or the embedded file. [Required] 
| [Id](General.DocumentFileAttachments.md#id) | guid |  
| [IsLinked](General.DocumentFileAttachments.md#islinked) | boolean | True when the document is linked (ony file name is kept). false when the document is embedded. [Required] [Default(false)] [Filter(eq)] 
| [LinkedFilePath](General.DocumentFileAttachments.md#linkedfilepath) | string (nullable) | Path to the linked file. null when the file is embedded. 
| [Notes](General.DocumentFileAttachments.md#notes) | string (nullable) | Notes for this DocumentFileAttachment. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Document](General.DocumentFileAttachments.md#document) | [Documents](General.Documents.md) | The [Document](General.DocumentFileAttachments.md#document) to which this DocumentFileAttachment belongs. [Required] [Filter(multi eq)] [Owner] |


## Attribute Details

### EmbeddedFileContents

The contents of the embedded file. null when the file is linked.

_Type_: **byte[] (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### FileName

The display name of the file. Initially set to the file name (without path) of the linked or the embedded file. [Required]

_Type_: **string**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### IsLinked

True when the document is linked (ony file name is kept). false when the document is embedded. [Required] [Default(false)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### LinkedFilePath

Path to the linked file. null when the file is embedded.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Notes

Notes for this DocumentFileAttachment.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### Document

The [Document](General.DocumentFileAttachments.md#document) to which this DocumentFileAttachment belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Documents](General.Documents.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=General.DocumentFileAttachments erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.DocumentFileAttachments erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_DocumentFileAttachments?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_DocumentFileAttachments?$top=10>

