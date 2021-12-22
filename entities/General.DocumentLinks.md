---
uid: General.DocumentLinks
---
# General.DocumentLinks Entity

**Namespace:** [General](General.md)  

Obsolete. Not used. Entity: Gen_Document_Links

## Default Visualization
Default Display Text Format:  
_{Id}: {ObjectVersion}_  
Default Search Members:  
__  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [General.DocumentLinks](General.DocumentLinks.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](General.DocumentLinks.md#id) | guid |  
| [ObjectVersion](General.DocumentLinks.md#objectversion) | int32 |  


## Attribute Details

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  

### ObjectVersion

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  



## Business Rules

[!list limit=1000 erp.entity=General.DocumentLinks erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=General.DocumentLinks erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_DocumentLinks?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_DocumentLinks?$top=10>

