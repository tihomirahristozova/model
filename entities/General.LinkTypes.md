---
uid: General.LinkTypes
---
# General.LinkTypes Entity

**Namespace:** [General](General.md)  

Obsolete. Not used. Entity: Gen_Link_Types

## Default Visualization
Default Display Text Format:  
_{Name:T}_  
Default Search Member:  
_Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [General.LinkTypes](General.LinkTypes.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [FromDocTypeId](General.LinkTypes.md#fromdoctypeid) | guid (nullable) | From which type of documents the link originates. null means that it might originate from any document type. [Filter(multi eq)] 
| [Id](General.LinkTypes.md#id) | guid |  
| [Name](General.LinkTypes.md#name) | string | Obsolete. Not used. [Required] 
| [ToDocTypeId](General.LinkTypes.md#todoctypeid) | guid (nullable) | To what type of documents the link points. null means that it might point to any document type. [Filter(multi eq)] 


## Attribute Details

### FromDocTypeId

From which type of documents the link originates. null means that it might originate from any document type. [Filter(multi eq)]

_Type_: **guid (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **NotFilterable**  

### Name

Obsolete. Not used. [Required]

_Type_: **string**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ToDocTypeId

To what type of documents the link points. null means that it might point to any document type. [Filter(multi eq)]

_Type_: **guid (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=General.LinkTypes erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.LinkTypes erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_LinkTypes?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_LinkTypes?$top=10>

