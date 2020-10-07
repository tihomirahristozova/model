# General.DocumentComments

Contains user comments for documents. Entity: Gen_Document_Comments

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](General.DocumentComments.md#Id) | guid |  
| [Comment](General.DocumentComments.md#Comment) | string | The user comment. [Required] 
| [CommentTimestamp](General.DocumentComments.md#CommentTimestamp) | datetime | The exact timestamp of the comment. [Required] [Default(Now)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [AssignToUser](General.DocumentComments.md#AssignToUser) | [Systems.Security.Users](Systems.Security.Users.md) (nullable) | When not null means that the comment is also an assignment of the document to another user. Upon saving the comment, the system assigns the document to the specified user. [Filter(multi eq)] |
| [Document](General.DocumentComments.md#Document) | [General.Documents](General.Documents.md) | The document to which to attach the comment. [Required] [Filter(multi eq)] [Owner] |
| [User](General.DocumentComments.md#User) | [Systems.Security.Users](Systems.Security.Users.md) | The user, who created the comment. [Required] [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### Comment

> The user comment. [Required]

_Type_: **string**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### CommentTimestamp

> The exact timestamp of the comment. [Required] [Default(Now)]

_Type_: **datetime**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **CurrentDateTime**  


## Reference Details

### AssignToUser

> When not null means that the comment is also an assignment of the document to another user. Upon saving the comment, the system assigns the document to the specified user. [Filter(multi eq)]

_Type_: **[Systems.Security.Users](Systems.Security.Users.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Document

> The document to which to attach the comment. [Required] [Filter(multi eq)] [Owner]

_Type_: **[General.Documents](General.Documents.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### User

> The user, who created the comment. [Required] [Filter(multi eq)]

_Type_: **[Systems.Security.Users](Systems.Security.Users.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=General.DocumentComments erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.DocumentComments erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=General.DocumentComments erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_DocumentComments?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_DocumentComments?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Gen_Document_Comments?$top=10>

