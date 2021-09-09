---
uid: Finance.Cost.CalculationProductOutputs
---
# Finance.Cost.CalculationProductOutputs Entity

**Namespace:** [Finance.Cost](Finance.Cost.md)  

Represents costs allocated to product outputs. Entity: Cost_Calculation_Product_Outputs

## Default Visualization
Default Display Text Format:  
_{Calculation.DocumentType.TypeName:T} {Calculation.DocumentNo}_  
Default Search Member:  
_Calculation.DocumentType.TypeName_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[Finance.Cost.Calculations](Finance.Cost.Calculations.md)  
Aggregate Root:  
[Finance.Cost.Calculations](Finance.Cost.Calculations.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Finance.Cost.CalculationProductOutputs.md#id) | guid |  
| [LineNo](Finance.Cost.CalculationProductOutputs.md#lineno) | int32 | Consecutive number of the line within the calculation. `Required` 
| [ProjectId](Finance.Cost.CalculationProductOutputs.md#projectid) | guid __nullable__ | The Project, which absorbed the cost. `Filter(multi eq)` 
| [Quantity](Finance.Cost.CalculationProductOutputs.md#quantity) | decimal (18, 3) | The quantity produced. `Required` `Default(0)` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Calculation](Finance.Cost.CalculationProductOutputs.md#calculation) | [Calculations](Finance.Cost.Calculations.md) | The `Calculation`(Finance.Cost.CalculationProductOutputs.md#calculation) to which this CalculationProductOutput belongs. `Required` `Filter(multi eq)` `Owner` |
| [Lot](Finance.Cost.CalculationProductOutputs.md#lot) | [Lots](Logistics.Inventory.Lots.md) (nullable) | The Lot, which absorbed the cost. `Filter(multi eq)` |
| [Parent](Finance.Cost.CalculationProductOutputs.md#parent) | [CalculationProductOutputs](Finance.Cost.CalculationProductOutputs.md) (nullable) | When not null specifies the parent output, whose cost is "absorbed" within the current output. `Filter(multi eq)` |
| [Product](Finance.Cost.CalculationProductOutputs.md#product) | [Products](General.Products.Products.md) | The Product, which absorbed the cost. `Required` `Filter(multi eq)` |
| [ProfitCenter](Finance.Cost.CalculationProductOutputs.md#profitcenter) | [ProfitCenters](Finance.Accounting.ProfitCenters.md) (nullable) | The Profit Center, which absorbed the cost. `Filter(multi eq)` |
| [SalesOrder](Finance.Cost.CalculationProductOutputs.md#salesorder) | [SalesOrders](Crm.Sales.SalesOrders.md) (nullable) | The Sales Order, which absorbed the cost. `Filter(multi eq)` |
| [Workgroup](Finance.Cost.CalculationProductOutputs.md#workgroup) | [Workgroups](Production.Resources.Workgroups.md) (nullable) | The Workgroup, which absorbed the cost. `Filter(multi eq)` |
| [WorkOrder](Finance.Cost.CalculationProductOutputs.md#workorder) | [WorkOrders](Production.ShopFloor.WorkOrders.md) (nullable) | The Work Order, which absorbed the cost. `Filter(multi eq)` |


## Attribute Details

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### LineNo

Consecutive number of the line within the calculation. `Required`

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`( obj.Calculation.ProductOutputs.Select( c => c.LineNo).DefaultIfEmpty( 0).Max( ) + 10)`

_Front-End Recalc Expressions:_  
`( obj.Calculation.ProductOutputs.Select( c => c.LineNo).DefaultIfEmpty( 0).Max( ) + 10)`
### ProjectId

The Project, which absorbed the cost. `Filter(multi eq)`

_Type_: **guid __nullable__**  
_Supported Filters_: **Equals, EqualsIn**  

### Quantity

The quantity produced. `Required` `Default(0)`

_Type_: **decimal (18, 3)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  


## Reference Details

### Calculation

The `Calculation`(Finance.Cost.CalculationProductOutputs.md#calculation) to which this CalculationProductOutput belongs. `Required` `Filter(multi eq)` `Owner`

_Type_: **[Calculations](Finance.Cost.Calculations.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  

### Lot

The Lot, which absorbed the cost. `Filter(multi eq)`

_Type_: **[Lots](Logistics.Inventory.Lots.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### Parent

When not null specifies the parent output, whose cost is "absorbed" within the current output. `Filter(multi eq)`

_Type_: **[CalculationProductOutputs](Finance.Cost.CalculationProductOutputs.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### Product

The Product, which absorbed the cost. `Required` `Filter(multi eq)`

_Type_: **[Products](General.Products.Products.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### ProfitCenter

The Profit Center, which absorbed the cost. `Filter(multi eq)`

_Type_: **[ProfitCenters](Finance.Accounting.ProfitCenters.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### SalesOrder

The Sales Order, which absorbed the cost. `Filter(multi eq)`

_Type_: **[SalesOrders](Crm.Sales.SalesOrders.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### Workgroup

The Workgroup, which absorbed the cost. `Filter(multi eq)`

_Type_: **[Workgroups](Production.Resources.Workgroups.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### WorkOrder

The Work Order, which absorbed the cost. `Filter(multi eq)`

_Type_: **[WorkOrders](Production.ShopFloor.WorkOrders.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list limit=1000 erp.entity=Finance.Cost.CalculationProductOutputs erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Finance.Cost.CalculationProductOutputs erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Cost_CalculationProductOutputs?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Cost_CalculationProductOutputs?$top=10>

