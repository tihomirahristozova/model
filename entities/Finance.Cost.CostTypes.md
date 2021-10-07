---
uid: Finance.Cost.CostTypes
---
# Finance.Cost.CostTypes Entity

**Namespace:** [Finance.Cost](Finance.Cost.md)  

Types of costs. Entity: Cost_Types

## Default Visualization
Default Display Text Format:  
_{Name}_  
Default Search Member:  
__  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Finance.Cost.CostTypes](Finance.Cost.CostTypes.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Code](Finance.Cost.CostTypes.md#code) | string (10) | Unique cost type code. Used for charting. `Required` `Filter(eq)` `ORD` 
| [Id](Finance.Cost.CostTypes.md#id) | guid |  
| [Name](Finance.Cost.CostTypes.md#name) | string (254) | Multilanguage cost type name. `Required` `Filter(like)` 


## Attribute Details

### Code

Unique cost type code. Used for charting. `Required` `Filter(eq)` `ORD`

_Type_: **string (10)**  
_Indexed_: **True**  
_Supported Filters_: **Equals**  
_Supports Order By_: **True**  
_Maximum Length_: **10**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

Multilanguage cost type name. `Required` `Filter(like)`

_Type_: **string (254)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  



## Business Rules

[!list limit=1000 erp.entity=Finance.Cost.CostTypes erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Finance.Cost.CostTypes erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Cost_CostTypes?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Cost_CostTypes?$top=10>

