---
uid: Finance.Cost.CalculationCosts
---
# Finance.Cost.CalculationCosts

Contains the calculated costs allocated to the different Cost Types. Entity: Cost_Calculation_Costs

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Finance.Cost.CalculationCosts.md#Id) | guid |  
| [Amount](Finance.Cost.CalculationCosts.md#Amount) | decimal | The allocated amount of costs in the currency of the calculation. [Required] [Default(0)] 
| [LineNo](Finance.Cost.CalculationCosts.md#LineNo) | int32 | Consecutive number of the line within the calculation. [Required] 
| [ProjectId](Finance.Cost.CalculationCosts.md#ProjectId) | guid (nullable) | The Project, which absorbed the cost. [Filter(multi eq)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Calculation](Finance.Cost.CalculationCosts.md#Calculation) | [Finance.Cost.Calculations](Finance.Cost.Calculations.md) | The [Calculation](Finance.Cost.CalculationCosts.md#Calculation) to which this CalculationCost belongs. [Required] [Filter(multi eq)] [Owner] |
| [CostCenter](Finance.Cost.CalculationCosts.md#CostCenter) | [Finance.Accounting.CostCenters](Finance.Accounting.CostCenters.md) (nullable) | The Cost Center, which absorbed the cost. [Filter(multi eq)] |
| [CostType](Finance.Cost.CalculationCosts.md#CostType) | [Finance.Cost.CostTypes](Finance.Cost.CostTypes.md) | The Cost Type, which absorbed the cost. [Required] [Filter(multi eq)] |
| [Lot](Finance.Cost.CalculationCosts.md#Lot) | [Logistics.Inventory.Lots](Logistics.Inventory.Lots.md) (nullable) | The Lot, which absorbed the cost. [Filter(multi eq)] |
| [Product](Finance.Cost.CalculationCosts.md#Product) | [General.Products.Products](General.Products.Products.md) (nullable) | The Product, which absorbed the cost. [Filter(multi eq)] |
| [SalesOrder](Finance.Cost.CalculationCosts.md#SalesOrder) | [Crm.Sales.SalesOrders](Crm.Sales.SalesOrders.md) (nullable) | The Sales Order, which absorbed the cost. [Filter(multi eq)] |
| [Workgroup](Finance.Cost.CalculationCosts.md#Workgroup) | [Production.Resources.Workgroups](Production.Resources.Workgroups.md) (nullable) | The Workgroup, which absorbed the cost. [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### Amount

> The allocated amount of costs in the currency of the calculation. [Required] [Default(0)]

_Type_: **decimal**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### LineNo

> Consecutive number of the line within the calculation. [Required]

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`(obj.Calculation.Costs.Select(c => c.LineNo).DefaultIfEmpty(0).Max() + 10)`

_Front-End Recalc Expressions:_  
`(obj.Calculation.Costs.Select(c => c.LineNo).DefaultIfEmpty(0).Max() + 10)`
### ProjectId

> The Project, which absorbed the cost. [Filter(multi eq)]

_Type_: **guid (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  


## Reference Details

### Calculation

> The [Calculation](Finance.Cost.CalculationCosts.md#Calculation) to which this CalculationCost belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Finance.Cost.Calculations](Finance.Cost.Calculations.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### CostCenter

> The Cost Center, which absorbed the cost. [Filter(multi eq)]

_Type_: **[Finance.Accounting.CostCenters](Finance.Accounting.CostCenters.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### CostType

> The Cost Type, which absorbed the cost. [Required] [Filter(multi eq)]

_Type_: **[Finance.Cost.CostTypes](Finance.Cost.CostTypes.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Lot

> The Lot, which absorbed the cost. [Filter(multi eq)]

_Type_: **[Logistics.Inventory.Lots](Logistics.Inventory.Lots.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Product

> The Product, which absorbed the cost. [Filter(multi eq)]

_Type_: **[General.Products.Products](General.Products.Products.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### SalesOrder

> The Sales Order, which absorbed the cost. [Filter(multi eq)]

_Type_: **[Crm.Sales.SalesOrders](Crm.Sales.SalesOrders.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Workgroup

> The Workgroup, which absorbed the cost. [Filter(multi eq)]

_Type_: **[Production.Resources.Workgroups](Production.Resources.Workgroups.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Finance.Cost.CalculationCosts erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Finance.Cost.CalculationCosts erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Finance.Cost.CalculationCosts erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Cost_CalculationCosts?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Cost_CalculationCosts?$top=10>

