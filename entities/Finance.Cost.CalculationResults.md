---
uid: Finance.Cost.CalculationResults
---
# Finance.Cost.CalculationResults

Contains the results of cost calculations. Entity: Cost_Calculation_Results

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Finance.Cost.CalculationResults.md#Id) | guid |  
| [FullCost](Finance.Cost.CalculationResults.md#FullCost) | decimal | The full cost of the specified quantity. [Required] [Default(0)] 
| [LineNo](Finance.Cost.CalculationResults.md#LineNo) | int32 | Consecutive number of the line within the calculation. [Required] 
| [ProjectId](Finance.Cost.CalculationResults.md#ProjectId) | guid (nullable) | The Project to which the cost was allocated. When null, the cost was not allocated to any specific Project. [Filter(multi eq)] 
| [Quantity](Finance.Cost.CalculationResults.md#Quantity) | decimal | The quantity of the product. [Required] [Default(0)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Calculation](Finance.Cost.CalculationResults.md#Calculation) | [Finance.Cost.Calculations](Finance.Cost.Calculations.md) | The [Calculation](Finance.Cost.CalculationResults.md#Calculation) to which this CalculationResult belongs. [Required] [Filter(multi eq)] [Owner] |
| [Lot](Finance.Cost.CalculationResults.md#Lot) | [Logistics.Inventory.Lots](Logistics.Inventory.Lots.md) (nullable) | The Lot to which the cost was allocated. When null, the cost was not allocated to any specific Lot. [Filter(multi eq)] |
| [Product](Finance.Cost.CalculationResults.md#Product) | [General.Products.Products](General.Products.Products.md) | The Product to which the cost was allocated. When null, the cost was not allocated to any specific Product. [Required] [Filter(multi eq)] |
| [ProfitCenter](Finance.Cost.CalculationResults.md#ProfitCenter) | [Finance.Accounting.ProfitCenters](Finance.Accounting.ProfitCenters.md) (nullable) | The Profit Center to which the cost was allocated. When null, the cost was not allocated to any specific Profit Center. [Filter(multi eq)] |
| [SalesOrder](Finance.Cost.CalculationResults.md#SalesOrder) | [Crm.Sales.SalesOrders](Crm.Sales.SalesOrders.md) (nullable) | The Sales Order to which the cost was allocated. When null, the cost was not allocated to any specific Sales Order. [Filter(multi eq)] |
| [Workgroup](Finance.Cost.CalculationResults.md#Workgroup) | [Production.Resources.Workgroups](Production.Resources.Workgroups.md) (nullable) | The Workgroup to which the cost was allocated. When null, the cost was not allocated to any specific Workgroup. [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### FullCost

> The full cost of the specified quantity. [Required] [Default(0)]

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
`(obj.Calculation.Results.Select(c => c.LineNo).DefaultIfEmpty(0).Max() + 10)`

_Front-End Recalc Expressions:_  
`(obj.Calculation.Results.Select(c => c.LineNo).DefaultIfEmpty(0).Max() + 10)`
### ProjectId

> The Project to which the cost was allocated. When null, the cost was not allocated to any specific Project. [Filter(multi eq)]

_Type_: **guid (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Quantity

> The quantity of the product. [Required] [Default(0)]

_Type_: **decimal**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  


## Reference Details

### Calculation

> The [Calculation](Finance.Cost.CalculationResults.md#Calculation) to which this CalculationResult belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Finance.Cost.Calculations](Finance.Cost.Calculations.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Lot

> The Lot to which the cost was allocated. When null, the cost was not allocated to any specific Lot. [Filter(multi eq)]

_Type_: **[Logistics.Inventory.Lots](Logistics.Inventory.Lots.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Product

> The Product to which the cost was allocated. When null, the cost was not allocated to any specific Product. [Required] [Filter(multi eq)]

_Type_: **[General.Products.Products](General.Products.Products.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### ProfitCenter

> The Profit Center to which the cost was allocated. When null, the cost was not allocated to any specific Profit Center. [Filter(multi eq)]

_Type_: **[Finance.Accounting.ProfitCenters](Finance.Accounting.ProfitCenters.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### SalesOrder

> The Sales Order to which the cost was allocated. When null, the cost was not allocated to any specific Sales Order. [Filter(multi eq)]

_Type_: **[Crm.Sales.SalesOrders](Crm.Sales.SalesOrders.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Workgroup

> The Workgroup to which the cost was allocated. When null, the cost was not allocated to any specific Workgroup. [Filter(multi eq)]

_Type_: **[Production.Resources.Workgroups](Production.Resources.Workgroups.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Finance.Cost.CalculationResults erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Finance.Cost.CalculationResults erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Finance.Cost.CalculationResults erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Cost_CalculationResults?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Cost_CalculationResults?$top=10>

