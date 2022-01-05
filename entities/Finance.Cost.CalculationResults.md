---
uid: Finance.Cost.CalculationResults
---
# Finance.Cost.CalculationResults Entity

**Namespace:** [Finance.Cost](Finance.Cost.md)  

Contains the results of cost calculations. Entity: Cost_Calculation_Results

## Default Visualization
Default Display Text Format:  
_{Calculation.EntityName}_  
Default Search Members:  
_Calculation.EntityName_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[Finance.Cost.Calculations](Finance.Cost.Calculations.md)  
Aggregate Root:  
[Finance.Cost.Calculations](Finance.Cost.Calculations.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [FullCost](Finance.Cost.CalculationResults.md#fullcost) | decimal (14, 2) | The full cost of the specified quantity. `Required` `Default(0)` 
| [Id](Finance.Cost.CalculationResults.md#id) | guid |  
| [LineNo](Finance.Cost.CalculationResults.md#lineno) | int32 | Consecutive number of the line within the calculation. `Required` 
| [ObjectVersion](Finance.Cost.CalculationResults.md#objectversion) | int32 |  
| [ProjectId](Finance.Cost.CalculationResults.md#projectid) | guid __nullable__ | The Project to which the cost was allocated. When null, the cost was not allocated to any specific Project. `Filter(multi eq)` 
| [Quantity](Finance.Cost.CalculationResults.md#quantity) | decimal (14, 3) | The quantity of the product. `Required` `Default(0)` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Calculation](Finance.Cost.CalculationResults.md#calculation) | [Calculations](Finance.Cost.Calculations.md) | The <see cref="Calculation"/> to which this CalculationResult belongs. `Required` `Filter(multi eq)` `Owner` |
| [Lot](Finance.Cost.CalculationResults.md#lot) | [Lots](Logistics.Inventory.Lots.md) (nullable) | The Lot to which the cost was allocated. When null, the cost was not allocated to any specific Lot. `Filter(multi eq)` |
| [Product](Finance.Cost.CalculationResults.md#product) | [Products](General.Products.Products.md) | The Product to which the cost was allocated. When null, the cost was not allocated to any specific Product. `Required` `Filter(multi eq)` |
| [ProfitCenter](Finance.Cost.CalculationResults.md#profitcenter) | [ProfitCenters](Finance.Accounting.ProfitCenters.md) (nullable) | The Profit Center to which the cost was allocated. When null, the cost was not allocated to any specific Profit Center. `Filter(multi eq)` |
| [SalesOrder](Finance.Cost.CalculationResults.md#salesorder) | [SalesOrders](Crm.Sales.SalesOrders.md) (nullable) | The Sales Order to which the cost was allocated. When null, the cost was not allocated to any specific Sales Order. `Filter(multi eq)` |
| [Workgroup](Finance.Cost.CalculationResults.md#workgroup) | [Workgroups](Production.Resources.Workgroups.md) (nullable) | The Workgroup to which the cost was allocated. When null, the cost was not allocated to any specific Workgroup. `Filter(multi eq)` |


## Attribute Details

### FullCost

The full cost of the specified quantity. `Required` `Default(0)`

_Type_: **decimal (14, 2)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  

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
`( obj.Calculation.Results.Select( c => c.LineNo).DefaultIfEmpty( 0).Max( ) + 10)`

_Front-End Recalc Expressions:_  
`( obj.Calculation.Results.Select( c => c.LineNo).DefaultIfEmpty( 0).Max( ) + 10)`
### ObjectVersion

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  

### ProjectId

The Project to which the cost was allocated. When null, the cost was not allocated to any specific Project. `Filter(multi eq)`

_Type_: **guid __nullable__**  
_Supported Filters_: **Equals, EqualsIn**  

### Quantity

The quantity of the product. `Required` `Default(0)`

_Type_: **decimal (14, 3)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  


## Reference Details

### Calculation

The <see cref="Calculation"/> to which this CalculationResult belongs. `Required` `Filter(multi eq)` `Owner`

_Type_: **[Calculations](Finance.Cost.Calculations.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  

### Lot

The Lot to which the cost was allocated. When null, the cost was not allocated to any specific Lot. `Filter(multi eq)`

_Type_: **[Lots](Logistics.Inventory.Lots.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### Product

The Product to which the cost was allocated. When null, the cost was not allocated to any specific Product. `Required` `Filter(multi eq)`

_Type_: **[Products](General.Products.Products.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### ProfitCenter

The Profit Center to which the cost was allocated. When null, the cost was not allocated to any specific Profit Center. `Filter(multi eq)`

_Type_: **[ProfitCenters](Finance.Accounting.ProfitCenters.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### SalesOrder

The Sales Order to which the cost was allocated. When null, the cost was not allocated to any specific Sales Order. `Filter(multi eq)`

_Type_: **[SalesOrders](Crm.Sales.SalesOrders.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### Workgroup

The Workgroup to which the cost was allocated. When null, the cost was not allocated to any specific Workgroup. `Filter(multi eq)`

_Type_: **[Workgroups](Production.Resources.Workgroups.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  


## API Methods

Methods that can be invoked in public APIs.

### GetAllowedCustomPropertyValues

Gets the allowed values for the specified custom property for this entity object.              If supported the result is ordered by property value. Some property value sources does not support ordering.  
_Return Type_: **Collection Of [CustomPropertyValue](../data-types.md#general.custompropertyvalue)**  
_Declaring Type_: **EntityObject**  
_Domain API Request_: **GET**  

**Parameters**  
  * **customPropertyCode**  
    The code of the custom property  
    _Type_: string  

  * **search**  
    The search text - searches by value or description  
    _Type_: string  
     _Optional_: True  
    _Default Value_: null  

  * **exactMatch**  
    If true the search text should be equal to the property value  
    _Type_: boolean  
     _Optional_: True  
    _Default Value_: False  

  * **orderByDescription**  
    If true the result is ordered by Description instead of Value. Note that ordering is not always possible.  
    _Type_: boolean  
     _Optional_: True  
    _Default Value_: False  

  * **top**  
    The top clause - default is 10  
    _Type_: int32  
     _Optional_: True  
    _Default Value_: 10  

  * **skip**  
    The skip clause - default is 0  
    _Type_: int32  
     _Optional_: True  
    _Default Value_: 0  



## Business Rules

[!list limit=1000 erp.entity=Finance.Cost.CalculationResults erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Finance.Cost.CalculationResults erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Cost_CalculationResults?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Cost_CalculationResults?$top=10>

