---
uid: General.LinkTypes
---
# General.LinkTypes

Obsolete. Not used. Entity: Gen_Link_Types

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](General.LinkTypes.md#Id) | guid |  
| [FromDocTypeId](General.LinkTypes.md#FromDocTypeId) | guid (nullable) | From which type of documents the link originates. null means that it might originate from any document type. [Filter(multi eq)] 
| [Name](General.LinkTypes.md#Name) | string | Obsolete. Not used. [Required] 
| [ToDocTypeId](General.LinkTypes.md#ToDocTypeId) | guid (nullable) | To what type of documents the link points. null means that it might point to any document type. [Filter(multi eq)] 


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **True**  

### FromDocTypeId

> From which type of documents the link originates. null means that it might originate from any document type. [Filter(multi eq)]

_Type_: **guid (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Name

> Obsolete. Not used. [Required]

_Type_: **string**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ToDocTypeId

> To what type of documents the link points. null means that it might point to any document type. [Filter(multi eq)]

_Type_: **guid (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=General.LinkTypes erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.LinkTypes erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=General.LinkTypes erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_LinkTypes?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_LinkTypes?$top=10>

