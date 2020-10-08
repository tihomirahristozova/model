---
uid: Finance.Cost.DistributionOutputs
---
# Finance.Cost.DistributionOutputs

Contains the output data for the specified period. This is the output on which cost is distributed. Entity: Cost_Distribution_Outputs

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Finance.Cost.DistributionOutputs.md#id) | guid |  
| [LineNo](Finance.Cost.DistributionOutputs.md#lineno) | int32 | Unique (within the document), consecutive line number of the output. [Required] 
| [WeightCoefficient](Finance.Cost.DistributionOutputs.md#weightcoefficient) | decimal | The weight coefficient for prorate distribution of cost over the current line. [Required] [Default(1)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [CostDistribution](Finance.Cost.DistributionOutputs.md#costdistribution) | [Finance.Cost.Distributions](Finance.Cost.Distributions.md) | The [Distribution](Finance.Cost.Distributions.md) to which this DistributionOutput belongs. [Required] [Filter(multi eq)] [Owner] |
| [StoreTransactionLine](Finance.Cost.DistributionOutputs.md#storetransactionline) | [Logistics.Inventory.StoreTransactionLines](Logistics.Inventory.StoreTransactionLines.md) | The store transaction line, for which costs will be distributed. [Required] [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### LineNo

> Unique (within the document), consecutive line number of the output. [Required]

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`(obj.CostDistribution.Outputs.Select(c => c.LineNo).DefaultIfEmpty(0).Max() + 10)`

_Front-End Recalc Expressions:_  
`(obj.CostDistribution.Outputs.Select(c => c.LineNo).DefaultIfEmpty(0).Max() + 10)`
### WeightCoefficient

> The weight coefficient for prorate distribution of cost over the current line. [Required] [Default(1)]

_Type_: **decimal**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **1**  


## Reference Details

### CostDistribution

> The [Distribution](Finance.Cost.Distributions.md) to which this DistributionOutput belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Finance.Cost.Distributions](Finance.Cost.Distributions.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### StoreTransactionLine

> The store transaction line, for which costs will be distributed. [Required] [Filter(multi eq)]

_Type_: **[Logistics.Inventory.StoreTransactionLines](Logistics.Inventory.StoreTransactionLines.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Finance.Cost.DistributionOutputs erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Finance.Cost.DistributionOutputs erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Finance.Cost.DistributionOutputs erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Cost_DistributionOutputs?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Cost_DistributionOutputs?$top=10>

