---
uid: Finance.Cost.DistributionCosts
---
# Finance.Cost.DistributionCosts Entity

The cost types and their amounts which are distributed by a Cost Distribution document. Entity: Cost_Distribution_Costs

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [AmountBase](Finance.Cost.DistributionCosts.md#amountbase) | [Amount](../data-types.md#amount) | The cost (in base currency) which should be distributed. [Currency: CostDistribution.EnterpriseCompany.BaseCurrency] [Required] [Filter(eq)] 
| [Id](Finance.Cost.DistributionCosts.md#id) | guid |  
| [Notes](Finance.Cost.DistributionCosts.md#notes) | string (nullable) | Notes for this DistributionCost. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [CostDistribution](Finance.Cost.DistributionCosts.md#costdistribution) | [Distributions](Finance.Cost.Distributions.md) | The [Distribution](Finance.Cost.Distributions.md) to which this DistributionCost belongs. [Required] [Filter(multi eq)] [Owner] |
| [CostType](Finance.Cost.DistributionCosts.md#costtype) | [CostTypes](Finance.Cost.CostTypes.md) | The type of the cost, which will be distributed. [Required] [Filter(multi eq)] |


## Attribute Details

### AmountBase

The cost (in base currency) which should be distributed. [Currency: CostDistribution.EnterpriseCompany.BaseCurrency] [Required] [Filter(eq)]

_Type_: **[Amount](../data-types.md#amount)**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Notes

Notes for this DistributionCost.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### CostDistribution

The [Distribution](Finance.Cost.Distributions.md) to which this DistributionCost belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Distributions](Finance.Cost.Distributions.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### CostType

The type of the cost, which will be distributed. [Required] [Filter(multi eq)]

_Type_: **[CostTypes](Finance.Cost.CostTypes.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Finance.Cost.DistributionCosts erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Finance.Cost.DistributionCosts erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Finance.Cost.DistributionCosts erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Cost_DistributionCosts?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Cost_DistributionCosts?$top=10>

