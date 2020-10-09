---
uid: General.Resources.ResourceCostRates
---
# General.Resources.ResourceCostRates

Contains cost rates for different periods for resources. Each record is valid until the next From Date. Entity: Gen_Resource_Cost_Rates

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [FromDate](General.Resources.ResourceCostRates.md#fromdate) | date | Starting date of validity of the cost rate. The rate is valid until the next cost rate record with later date is defined. [Required] [Filter(eq;ge;le)] 
| [Id](General.Resources.ResourceCostRates.md#id) | guid |  
| [Notes](General.Resources.ResourceCostRates.md#notes) | string (nullable) | Notes for this ResourceCostRate. 
| [OvertimeRatePerHour](General.Resources.ResourceCostRates.md#overtimerateperhour) | [Amount](../data-types.md#amount) (nullable) | The overtime cost of the resource per hour in the resources costing currency. The overtime rate specifies the cost of the resource, when it is used outside the normal working schedule. null means that there is no special overtime rate and the standard rate should be applied. [Currency: Resource.CostingCurrency] [Filter(eq;like)] 
| [PerUseCost](General.Resources.ResourceCostRates.md#perusecost) | [Amount](../data-types.md#amount) | One-time cost for each usage of the resource in the resources costing currency. [Currency: Resource.CostingCurrency] [Required] [Default(0)] [Filter(eq;like)] 
| [StandardRatePerHour](General.Resources.ResourceCostRates.md#standardrateperhour) | [Amount](../data-types.md#amount) | The standard cost per hour of the resource in the resources costing currency. The standard cost is applied for resource usage during the normal working hours. [Currency: Resource.CostingCurrency] [Required] [Filter(eq;like)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [EnterpriseCompany](General.Resources.ResourceCostRates.md#enterprisecompany) | [EnterpriseCompanies](General.EnterpriseCompanies.md) | The enterprise company for which the cost is defined. [Required] [Filter(multi eq)] |
| [Resource](General.Resources.ResourceCostRates.md#resource) | [Resources](General.Resources.Resources.md) | The resource for which the cost rate is defined. [Required] [Filter(multi eq)] [Owner] |


## Attribute Details

### FromDate

> Starting date of validity of the cost rate. The rate is valid until the next cost rate record with later date is defined. [Required] [Filter(eq;ge;le)]

_Type_: **date**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Notes

> Notes for this ResourceCostRate.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### OvertimeRatePerHour

> The overtime cost of the resource per hour in the resources costing currency. The overtime rate specifies the cost of the resource, when it is used outside the normal working schedule. null means that there is no special overtime rate and the standard rate should be applied. [Currency: Resource.CostingCurrency] [Filter(eq;like)]

_Type_: **[Amount](../data-types.md#amount) (nullable)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### PerUseCost

> One-time cost for each usage of the resource in the resources costing currency. [Currency: Resource.CostingCurrency] [Required] [Default(0)] [Filter(eq;like)]

_Type_: **[Amount](../data-types.md#amount)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### StandardRatePerHour

> The standard cost per hour of the resource in the resources costing currency. The standard cost is applied for resource usage during the normal working hours. [Currency: Resource.CostingCurrency] [Required] [Filter(eq;like)]

_Type_: **[Amount](../data-types.md#amount)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  


## Reference Details

### EnterpriseCompany

> The enterprise company for which the cost is defined. [Required] [Filter(multi eq)]

_Type_: **[EnterpriseCompanies](General.EnterpriseCompanies.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### Resource

> The resource for which the cost rate is defined. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Resources](General.Resources.Resources.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=General.Resources.ResourceCostRates erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.Resources.ResourceCostRates erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=General.Resources.ResourceCostRates erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_Resources_ResourceCostRates?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_Resources_ResourceCostRates?$top=10>

