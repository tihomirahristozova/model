# General.DocumentVersions

History of each saved version of each document. Entity: Gen_Document_Versions

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](General.DocumentVersions.md#Id) | guid |  
| [DocumentData](General.DocumentVersions.md#DocumentData) | byte[] (nullable) | Compressed representation of the document data. Valid when Document Data Format = D (deflate compressed). [ReadOnly] 
| [DocumentDataFormat](General.DocumentVersions.md#DocumentDataFormat) | string | The format of the saved document data. 'U' - uncompressed and stored in Document Data XML; 'D' - Deflate compressed and stored in Document Data. [Required] [Default("U")] [ReadOnly] 
| [DocumentDataXML](General.DocumentVersions.md#DocumentDataXML) | string (nullable) | The uncompressed XML representation of the document data, including the document row, the header row and all types of lines. Valid when Document Data Format = U (uncompressed). [ReadOnly] 
| [State](General.DocumentVersions.md#State) | [General.DocumentVersionsRepository.State](General.DocumentVersions.md#State) | The state of the document by the time it was saved. [Required] [Default(0)] [Filter(multi eq)] [ReadOnly] 
| [UpdateTime](General.DocumentVersions.md#UpdateTime) | datetime | The date and time when this version was saved. [Required] [Default(Now)] [Filter(ge;le)] [ORD] [ReadOnly] 
| [UpdateUser](General.DocumentVersions.md#UpdateUser) | string | The login name of the user that saved this version. [Required] [Filter(eq;like)] [ReadOnly] 
| [Version](General.DocumentVersions.md#Version) | int32 | The version number that is stored in this row. [Required] [Filter(eq;ge;le)] [ReadOnly] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Document](General.DocumentVersions.md#Document) | [General.Documents](General.Documents.md) | The document whoose version is stored in this row. [Required] [Filter(multi eq)] [ReadOnly] [Owner] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### DocumentData

> Compressed representation of the document data. Valid when Document Data Format = D (deflate compressed). [ReadOnly]

_Type_: **byte[] (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### DocumentDataFormat

> The format of the saved document data. 'U' - uncompressed and stored in Document Data XML; 'D' - Deflate compressed and stored in Document Data. [Required] [Default("U")] [ReadOnly]

_Type_: **string**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **U**  

### DocumentDataXML

> The uncompressed XML representation of the document data, including the document row, the header row and all types of lines. Valid when Document Data Format = U (uncompressed). [ReadOnly]

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### State

> The state of the document by the time it was saved. [Required] [Default(0)] [Filter(multi eq)] [ReadOnly]

_Type_: **[General.DocumentVersionsRepository.State](General.DocumentVersions.md#State)**  
Allowed values for the [State](General.DocumentVersions.md#State) data attribute  
_Allowed Values (Enum Members)_  

| Value | Description |
| ---- | --- |
| New | New value. Stored as 0. <br /> _Database Value:_ 0 <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'New' |
| Corrective | Corrective value. Stored as 5. <br /> _Database Value:_ 5 <br /> _Model Value:_ 5 <br /> _Domain API Value:_ 'Corrective' |
| Planned | Planned value. Stored as 10. <br /> _Database Value:_ 10 <br /> _Model Value:_ 10 <br /> _Domain API Value:_ 'Planned' |
| FirmPlanned | FirmPlanned value. Stored as 20. <br /> _Database Value:_ 20 <br /> _Model Value:_ 20 <br /> _Domain API Value:_ 'FirmPlanned' |
| Released | Released value. Stored as 30. <br /> _Database Value:_ 30 <br /> _Model Value:_ 30 <br /> _Domain API Value:_ 'Released' |
| Completed | Completed value. Stored as 40. <br /> _Database Value:_ 40 <br /> _Model Value:_ 40 <br /> _Domain API Value:_ 'Completed' |
| Closed | Closed value. Stored as 50. <br /> _Database Value:_ 50 <br /> _Model Value:_ 50 <br /> _Domain API Value:_ 'Closed' |

_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### UpdateTime

> The date and time when this version was saved. [Required] [Default(Now)] [Filter(ge;le)] [ORD] [ReadOnly]

_Type_: **datetime**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **True**  
_Default Value_: **CurrentDateTime**  

### UpdateUser

> The login name of the user that saved this version. [Required] [Filter(eq;like)] [ReadOnly]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### Version

> The version number that is stored in this row. [Required] [Filter(eq;ge;le)] [ReadOnly]

_Type_: **int32**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  


## Reference Details

### Document

> The document whoose version is stored in this row. [Required] [Filter(multi eq)] [ReadOnly] [Owner]

_Type_: **[General.Documents](General.Documents.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=General.DocumentVersions erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.DocumentVersions erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=General.DocumentVersions erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_DocumentVersions?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_DocumentVersions?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Gen_Document_Versions?$top=10>

