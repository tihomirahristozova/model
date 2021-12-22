---
uid: General.DocumentComments
---
# General.DocumentComments Entity

**Namespace:** [General](General.md)  

Contains user comments for documents. Entity: Gen_Document_Comments

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
| [Comment](General.DocumentComments.md#comment) | string (254) | The user comment. `Required` 
| [CommentTimestamp](General.DocumentComments.md#commenttimestamp) | datetime | The exact timestamp of the comment. `Required` `Default(Now)` 
| [Id](General.DocumentComments.md#id) | guid |  
| [ObjectVersion](General.DocumentComments.md#objectversion) | int32 |  

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [AssignToUser](General.DocumentComments.md#assigntouser) | [Users](Systems.Security.Users.md) (nullable) | When not null means that the comment is also an assignment of the document to another user. Upon saving the comment, the system assigns the document to the specified user. `Filter(multi eq)` |
| [Document](General.DocumentComments.md#document) | [Documents](General.Documents.md) | The document to which to attach the comment. `Required` `Filter(multi eq)` `Owner` |
| [User](General.DocumentComments.md#user) | [Users](Systems.Security.Users.md) | The user, who created the comment. `Required` `Filter(multi eq)` |


## Attribute Details

### Comment

The user comment. `Required`

_Type_: **string (254)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  

### CommentTimestamp

The exact timestamp of the comment. `Required` `Default(Now)`

_Type_: **datetime**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **CurrentDateTime**  

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

### AssignToUser

When not null means that the comment is also an assignment of the document to another user. Upon saving the comment, the system assigns the document to the specified user. `Filter(multi eq)`

_Type_: **[Users](Systems.Security.Users.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### Document

The document to which to attach the comment. `Required` `Filter(multi eq)` `Owner`

_Type_: **[Documents](General.Documents.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  

### User

The user, who created the comment. `Required` `Filter(multi eq)`

_Type_: **[Users](Systems.Security.Users.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list limit=1000 erp.entity=General.DocumentComments erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=General.DocumentComments erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_DocumentComments?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_DocumentComments?$top=10>

