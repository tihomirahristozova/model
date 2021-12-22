---
uid: Production.Resources.OperationInstructions
---
# Production.Resources.OperationInstructions Entity

**Namespace:** [Production.Resources](Production.Resources.md)  

Long (full) instructions for performing an operation. The operations point to the instructions and one instruction can be used for different operations. Entity: Prd_Operation_Instructions

## Default Visualization
Default Display Text Format:  
_{Id}: {ObjectVersion}_  
Default Search Members:  
__  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Production.Resources.OperationInstructions](Production.Resources.OperationInstructions.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Description](Production.Resources.OperationInstructions.md#description) | string (254) __nullable__ | Short description or notes for the instructions. `Filter(like)` 
| [Id](Production.Resources.OperationInstructions.md#id) | guid |  
| [Instructions](Production.Resources.OperationInstructions.md#instructions) | byte[] __nullable__ | The operation instructions in OLE format. 
| [ObjectVersion](Production.Resources.OperationInstructions.md#objectversion) | int32 |  


## Attribute Details

### Description

Short description or notes for the instructions. `Filter(like)`

_Type_: **string (254) __nullable__**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  

### Instructions

The operation instructions in OLE format.

_Type_: **byte[] __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ObjectVersion

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  



## Business Rules

[!list limit=1000 erp.entity=Production.Resources.OperationInstructions erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Production.Resources.OperationInstructions erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Production_Resources_OperationInstructions?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Production_Resources_OperationInstructions?$top=10>

