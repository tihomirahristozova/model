---
uid: General.Documents.DocumentParties
---
# General.Documents.DocumentParties Entity

**Namespace:** [General.Documents](General.Documents.md)  

Represents a party associated to a document. Entity: Gen_Document_Parties (Introduced in version 22.1.4.46)

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
| [Id](General.Documents.DocumentParties.md#id) | guid |  
| [Notes](General.Documents.DocumentParties.md#notes) | string (max) __nullable__ | Notes for this DocumentParty. 
| [ObjectVersion](General.Documents.DocumentParties.md#objectversion) | int32 |  

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Document](General.Documents.DocumentParties.md#document) | [Documents](General.Documents.md) | The document in which the party plays a role. `Required` `Filter(multi eq)` `Owner` |
| [Party](General.Documents.DocumentParties.md#party) | [Parties](General.Contacts.Parties.md) | The party, which plays a role in the document. `Required` `Filter(multi eq)` |
| [Role](General.Documents.DocumentParties.md#role) | [DocumentPartyRoles](General.Documents.DocumentPartyRoles.md) | The role of the party in the document. `Required` `Filter(multi eq)` |


## Attribute Details

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Notes

Notes for this DocumentParty.

_Type_: **string (max) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  

### ObjectVersion

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  


## Reference Details

### Document

The document in which the party plays a role. `Required` `Filter(multi eq)` `Owner`

_Type_: **[Documents](General.Documents.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  

### Party

The party, which plays a role in the document. `Required` `Filter(multi eq)`

_Type_: **[Parties](General.Contacts.Parties.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### Role

The role of the party in the document. `Required` `Filter(multi eq)`

_Type_: **[DocumentPartyRoles](General.Documents.DocumentPartyRoles.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list limit=1000 erp.entity=General.Documents.DocumentParties erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=General.Documents.DocumentParties erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_Documents_DocumentParties?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_Documents_DocumentParties?$top=10>

