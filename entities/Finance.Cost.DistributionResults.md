---
uid: Finance.Cost.DistributionResults
---
# Finance.Cost.DistributionResults

Contains the results of a cost distribution calculation. Entity: Cost_Distribution_Results

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Finance.Cost.DistributionResults.md#Id) | guid |  
| [DistributedAmountBase](Finance.Cost.DistributionResults.md#DistributedAmountBase) | [Amount](../data-types.md#Amount) | The amount (in base currency) of the distributed cost. The amount is calculated for the combination of output and cost type. [Currency: CostDistribution.EnterpriseCompany.BaseCurrency] [Required] 
| [LineNo](Finance.Cost.DistributionResults.md#LineNo) | int32 | Consecutive line number (within the cost distribution document) of the result. [Required] 
| [OutputLineNo](Finance.Cost.DistributionResults.md#OutputLineNo) | int32 | The line number (within the document) of the output over which the cost is distributed. [Required] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [CostDistribution](Finance.Cost.DistributionResults.md#CostDistribution) | [Finance.Cost.Distributions](Finance.Cost.Distributions.md) | The [Distribution](Finance.Cost.Distributions.md) to which this DistributionResult belongs. [Required] [Filter(multi eq)] [Owner] |
| [CostType](Finance.Cost.DistributionResults.md#CostType) | [Finance.Cost.CostTypes](Finance.Cost.CostTypes.md) | The cost type for which the current distribution is calculated. [Required] [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### DistributedAmountBase

> The amount (in base currency) of the distributed cost. The amount is calculated for the combination of output and cost type. [Currency: CostDistribution.EnterpriseCompany.BaseCurrency] [Required]

_Type_: **[Amount](../data-types.md#Amount)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### LineNo

> Consecutive line number (within the cost distribution document) of the result. [Required]

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`(obj.CostDistribution.Results.Select(c => c.LineNo).DefaultIfEmpty(0).Max() + 10)`

_Front-End Recalc Expressions:_  
`(obj.CostDistribution.Results.Select(c => c.LineNo).DefaultIfEmpty(0).Max() + 10)`
### OutputLineNo

> The line number (within the document) of the output over which the cost is distributed. [Required]

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### CostDistribution

> The [Distribution](Finance.Cost.Distributions.md) to which this DistributionResult belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Finance.Cost.Distributions](Finance.Cost.Distributions.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### CostType

> The cost type for which the current distribution is calculated. [Required] [Filter(multi eq)]

_Type_: **[Finance.Cost.CostTypes](Finance.Cost.CostTypes.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Finance.Cost.DistributionResults erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Finance.Cost.DistributionResults erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Finance.Cost.DistributionResults erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Cost_DistributionResults?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Cost_DistributionResults?$top=10>

