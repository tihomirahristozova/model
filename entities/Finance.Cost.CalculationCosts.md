---
uid: Finance.Cost.CalculationCosts
---
# Finance.Cost.CalculationCosts Entity

Contains the calculated costs allocated to the different Cost Types. Entity: Cost_Calculation_Costs

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Amount](Finance.Cost.CalculationCosts.md#amount) | decimal | The allocated amount of costs in the currency of the calculation. [Required] [Default(0)] 
| [Id](Finance.Cost.CalculationCosts.md#id) | guid |  
| [LineNo](Finance.Cost.CalculationCosts.md#lineno) | int32 | Consecutive number of the line within the calculation. [Required] 
| [ProjectId](Finance.Cost.CalculationCosts.md#projectid) | guid (nullable) | The Project, which absorbed the cost. [Filter(multi eq)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Calculation](Finance.Cost.CalculationCosts.md#calculation) | [Calculations](Finance.Cost.Calculations.md) | The [Calculation](Finance.Cost.CalculationCosts.md#calculation) to which this CalculationCost belongs. [Required] [Filter(multi eq)] [Owner] |
| [CostCenter](Finance.Cost.CalculationCosts.md#costcenter) | [CostCenters](Finance.Accounting.CostCenters.md) (nullable) | The Cost Center, which absorbed the cost. [Filter(multi eq)] |
| [CostType](Finance.Cost.CalculationCosts.md#costtype) | [CostTypes](Finance.Cost.CostTypes.md) | The Cost Type, which absorbed the cost. [Required] [Filter(multi eq)] |
| [Lot](Finance.Cost.CalculationCosts.md#lot) | [Lots](Logistics.Inventory.Lots.md) (nullable) | The Lot, which absorbed the cost. [Filter(multi eq)] |
| [Product](Finance.Cost.CalculationCosts.md#product) | [Products](General.Products.Products.md) (nullable) | The Product, which absorbed the cost. [Filter(multi eq)] |
| [SalesOrder](Finance.Cost.CalculationCosts.md#salesorder) | [SalesOrders](Crm.Sales.SalesOrders.md) (nullable) | The Sales Order, which absorbed the cost. [Filter(multi eq)] |
| [Workgroup](Finance.Cost.CalculationCosts.md#workgroup) | [Workgroups](Production.Resources.Workgroups.md) (nullable) | The Workgroup, which absorbed the cost. [Filter(multi eq)] |


## Attribute Details

### Amount

The allocated amount of costs in the currency of the calculation. [Required] [Default(0)]

_Type_: **decimal**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### LineNo

Consecutive number of the line within the calculation. [Required]

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`( obj.Calculation.Costs.Select( c => c.LineNo).DefaultIfEmpty( 0).Max( ) + 10)`

_Front-End Recalc Expressions:_  
`( obj.Calculation.Costs.Select( c => c.LineNo).DefaultIfEmpty( 0).Max( ) + 10)`
### ProjectId

The Project, which absorbed the cost. [Filter(multi eq)]

_Type_: **guid (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  


## Reference Details

### Calculation

The [Calculation](Finance.Cost.CalculationCosts.md#calculation) to which this CalculationCost belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Calculations](Finance.Cost.Calculations.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### CostCenter

The Cost Center, which absorbed the cost. [Filter(multi eq)]

_Type_: **[CostCenters](Finance.Accounting.CostCenters.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### CostType

The Cost Type, which absorbed the cost. [Required] [Filter(multi eq)]

_Type_: **[CostTypes](Finance.Cost.CostTypes.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### Lot

The Lot, which absorbed the cost. [Filter(multi eq)]

_Type_: **[Lots](Logistics.Inventory.Lots.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### Product

The Product, which absorbed the cost. [Filter(multi eq)]

_Type_: **[Products](General.Products.Products.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### SalesOrder

The Sales Order, which absorbed the cost. [Filter(multi eq)]

_Type_: **[SalesOrders](Crm.Sales.SalesOrders.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### Workgroup

The Workgroup, which absorbed the cost. [Filter(multi eq)]

_Type_: **[Workgroups](Production.Resources.Workgroups.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Finance.Cost.CalculationCosts erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Finance.Cost.CalculationCosts erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Cost_CalculationCosts?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Cost_CalculationCosts?$top=10>

