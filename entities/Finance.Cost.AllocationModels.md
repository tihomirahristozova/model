---
uid: Finance.Cost.AllocationModels
---
# Finance.Cost.AllocationModels

User-defined models for cost allocation. Entity: Cost_Allocation_Models

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Finance.Cost.AllocationModels.md#Id) | guid |  
| [CostAllocationModelName](Finance.Cost.AllocationModels.md#CostAllocationModelName) | string | Multilanguage allocation model name. [Required] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Currency](Finance.Cost.AllocationModels.md#Currency) | [General.Currencies](General.Currencies.md) | The currency in which the calculation is done. This is applied to the production and the results. [Required] [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### CostAllocationModelName

> Multilanguage allocation model name. [Required]

_Type_: **string**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### Currency

> The currency in which the calculation is done. This is applied to the production and the results. [Required] [Filter(multi eq)]

_Type_: **[General.Currencies](General.Currencies.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Finance.Cost.AllocationModels erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Finance.Cost.AllocationModels erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Finance.Cost.AllocationModels erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Cost_AllocationModels?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Cost_AllocationModels?$top=10>

