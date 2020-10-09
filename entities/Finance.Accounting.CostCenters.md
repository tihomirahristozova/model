---
uid: Finance.Accounting.CostCenters
---
# Finance.Accounting.CostCenters Entity

Defines cost centers and their relation to profit centers. Entity: Acc_Cost_Centers

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Finance.Accounting.CostCenters.md#id) | guid |  
| [Name](Finance.Accounting.CostCenters.md#name) | string | The name of this CostCenter. [Required] [Filter(like)] 
| [Notes](Finance.Accounting.CostCenters.md#notes) | string (nullable) | Notes for this CostCenter. 
| [RelativeWeight](Finance.Accounting.CostCenters.md#relativeweight) | decimal | The weight of this cost center, relative to the other cost centers within the same parent. The weight is used during cost distribution calculations. The sum of weights of all cost centers within a parent does not need to be 100, the ratio of total weight over weight is used. [Required] [Default(1)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Parent](Finance.Accounting.CostCenters.md#parent) | [CostCenters](Finance.Accounting.CostCenters.md) (nullable) | Parent cost center, null if this is root cost center. [Filter(multi eq)] |
| [TransferCostToProfitCenter](Finance.Accounting.CostCenters.md#transfercosttoprofitcenter) | [ProfitCenters](Finance.Accounting.ProfitCenters.md) (nullable) | Points to the profit center to which to transfer the cost. Valid only for leaf cost centers. [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

The name of this CostCenter. [Required] [Filter(like)]

_Type_: **string**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### Notes

Notes for this CostCenter.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### RelativeWeight

The weight of this cost center, relative to the other cost centers within the same parent. The weight is used during cost distribution calculations. The sum of weights of all cost centers within a parent does not need to be 100, the ratio of total weight over weight is used. [Required] [Default(1)]

_Type_: **decimal**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **1**  


## Reference Details

### Parent

Parent cost center, null if this is root cost center. [Filter(multi eq)]

_Type_: **[CostCenters](Finance.Accounting.CostCenters.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### TransferCostToProfitCenter

Points to the profit center to which to transfer the cost. Valid only for leaf cost centers. [Filter(multi eq)]

_Type_: **[ProfitCenters](Finance.Accounting.ProfitCenters.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Finance.Accounting.CostCenters erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Finance.Accounting.CostCenters erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Finance.Accounting.CostCenters erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Accounting_CostCenters?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Accounting_CostCenters?$top=10>

