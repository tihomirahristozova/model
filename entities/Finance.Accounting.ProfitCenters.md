# Finance.Accounting.ProfitCenters

Defines company profit centers and their relative weight for automatic balance transfers from cost centers. Entity: Acc_Profit_Centers

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Finance.Accounting.ProfitCenters.md#Id) | guid |  
| [Notes](Finance.Accounting.ProfitCenters.md#Notes) | string (nullable) | Notes for this ProfitCenter. 
| [Name](Finance.Accounting.ProfitCenters.md#Name) | string | The name of this ProfitCenter. [Required] [Filter(like)] 
| [RelativeWeight](Finance.Accounting.ProfitCenters.md#RelativeWeight) | decimal | The weight of this profit center, relative to the other profit centers within the same parent. The weight is used during profit distribution calculations. The sum of weights of all profit centers within a parent does not need to be 100, the ratio of total weight over weight is used. [Required] [Default(1)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Parent](Finance.Accounting.ProfitCenters.md#Parent) | [Finance.Accounting.ProfitCenters](Finance.Accounting.ProfitCenters.md) (nullable) | Parent profit center, null if this is root profit center. [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### Notes

> Notes for this ProfitCenter.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Name

> The name of this ProfitCenter. [Required] [Filter(like)]

_Type_: **string**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### RelativeWeight

> The weight of this profit center, relative to the other profit centers within the same parent. The weight is used during profit distribution calculations. The sum of weights of all profit centers within a parent does not need to be 100, the ratio of total weight over weight is used. [Required] [Default(1)]

_Type_: **decimal**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **1**  


## Reference Details

### Parent

> Parent profit center, null if this is root profit center. [Filter(multi eq)]

_Type_: **[Finance.Accounting.ProfitCenters](Finance.Accounting.ProfitCenters.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Finance.Accounting.ProfitCenters erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Finance.Accounting.ProfitCenters erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Finance.Accounting.ProfitCenters erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Accounting_ProfitCenters?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Accounting_ProfitCenters?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Acc_Profit_Centers?$top=10>

