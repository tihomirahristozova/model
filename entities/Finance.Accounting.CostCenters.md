---
uid: Finance.Accounting.CostCenters
---
# Finance.Accounting.CostCenters Entity

**Namespace:** [Finance.Accounting](Finance.Accounting.md)  

Defines cost centers and their relation to profit centers. Entity: Acc_Cost_Centers

## Default Visualization
Default Display Text Format:  
_{Name}_  
Default Search Member:  
__  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Finance.Accounting.CostCenters](Finance.Accounting.CostCenters.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Finance.Accounting.CostCenters.md#id) | guid |  
| [Name](Finance.Accounting.CostCenters.md#name) | string (254) | The name of this CostCenter. `Required` `Filter(like)` 
| [Notes](Finance.Accounting.CostCenters.md#notes) | string (254) __nullable__ | Notes for this CostCenter. 
| [RelativeWeight](Finance.Accounting.CostCenters.md#relativeweight) | decimal (18, 4) | The weight of this cost center, relative to the other cost centers within the same parent. The weight is used during cost distribution calculations. The sum of weights of all cost centers within a parent does not need to be 100, the ratio of total weight over weight is used. `Required` `Default(1)` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Parent](Finance.Accounting.CostCenters.md#parent) | [CostCenters](Finance.Accounting.CostCenters.md) (nullable) | Parent cost center, null if this is root cost center. `Filter(multi eq)` |
| [TransferCostToProfitCenter](Finance.Accounting.CostCenters.md#transfercosttoprofitcenter) | [ProfitCenters](Finance.Accounting.ProfitCenters.md) (nullable) | Points to the profit center to which to transfer the cost. Valid only for leaf cost centers. `Filter(multi eq)` |


## Attribute Details

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

The name of this CostCenter. `Required` `Filter(like)`

_Type_: **string (254)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  

### Notes

Notes for this CostCenter.

_Type_: **string (254) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  

### RelativeWeight

The weight of this cost center, relative to the other cost centers within the same parent. The weight is used during cost distribution calculations. The sum of weights of all cost centers within a parent does not need to be 100, the ratio of total weight over weight is used. `Required` `Default(1)`

_Type_: **decimal (18, 4)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **1**  


## Reference Details

### Parent

Parent cost center, null if this is root cost center. `Filter(multi eq)`

_Type_: **[CostCenters](Finance.Accounting.CostCenters.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### TransferCostToProfitCenter

Points to the profit center to which to transfer the cost. Valid only for leaf cost centers. `Filter(multi eq)`

_Type_: **[ProfitCenters](Finance.Accounting.ProfitCenters.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list limit=1000 erp.entity=Finance.Accounting.CostCenters erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Finance.Accounting.CostCenters erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Accounting_CostCenters?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Accounting_CostCenters?$top=10>

