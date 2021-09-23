---
uid: Finance.Cost.AllocationModels
---
# Finance.Cost.AllocationModels Entity

**Namespace:** [Finance.Cost](Finance.Cost.md)  

User-defined models for cost allocation. Entity: Cost_Allocation_Models

## Default Visualization
Default Display Text Format:  
_{CostAllocationModelName:T}_  
Default Search Member:  
__  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Finance.Cost.AllocationModels](Finance.Cost.AllocationModels.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [CostAllocationModelName](Finance.Cost.AllocationModels.md#costallocationmodelname) | string (254) | Multilanguage allocation model name. `Required` 
| [Id](Finance.Cost.AllocationModels.md#id) | guid |  

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Currency](Finance.Cost.AllocationModels.md#currency) | [Currencies](General.Currencies.md) | The currency in which the calculation is done. This is applied to the production and the results. `Required` `Filter(multi eq)` |


## Attribute Details

### CostAllocationModelName

Multilanguage allocation model name. `Required`

_Type_: **string (254)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  


## Reference Details

### Currency

The currency in which the calculation is done. This is applied to the production and the results. `Required` `Filter(multi eq)`

_Type_: **[Currencies](General.Currencies.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list limit=1000 erp.entity=Finance.Cost.AllocationModels erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Finance.Cost.AllocationModels erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Cost_AllocationModels?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Cost_AllocationModels?$top=10>

