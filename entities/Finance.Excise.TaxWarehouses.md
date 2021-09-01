---
uid: Finance.Excise.TaxWarehouses
---
# Finance.Excise.TaxWarehouses Entity

**Namespace:** [Finance.Excise](Finance.Excise.md)  

Contains excise-related data for warehouses (stores), which are defined as tax warehouses. Products subject to excise duties must be produced in tax warehouses. They can also be stored, under duty suspension, in these tax warehouses. Entity: Exc_Tax_Warehouses (Introduced in version 21.1.1.1)

## Default Visualization
Default Display Text Format:  
_{TaxWarehouseExciseNumber}_  
Default Search Member:  
_TaxWarehouseExciseNumber_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Finance.Excise.TaxWarehouses](Finance.Excise.TaxWarehouses.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Finance.Excise.TaxWarehouses.md#id) | guid |  
| [TaxWarehouseExciseNumber](Finance.Excise.TaxWarehouses.md#taxwarehouseexcisenumber) | string (32) | The excise identification number of the tax warehouse, issued by the competent authorities. `Required` `Default("-")` `Introduced in version 21.1.3.87` 
| [TraderExciseNumber](Finance.Excise.TaxWarehouses.md#traderexcisenumber) | string (32) | The excise identification number of the owner of the Tax Warehouse. `Required` `Default("-")` `Introduced in version 21.1.3.87` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Store](Finance.Excise.TaxWarehouses.md#store) | [Stores](Logistics.Inventory.Stores.md) | The base warehouse (store), which is declared as tax warehouse. `Required` `Filter(multi eq)` |


## Attribute Details

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### TaxWarehouseExciseNumber

The excise identification number of the tax warehouse, issued by the competent authorities. `Required` `Default("-")` `Introduced in version 21.1.3.87`

_Type_: **string (32)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **32**  
_Default Value_: **-**  

### TraderExciseNumber

The excise identification number of the owner of the Tax Warehouse. `Required` `Default("-")` `Introduced in version 21.1.3.87`

_Type_: **string (32)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **32**  
_Default Value_: **-**  


## Reference Details

### Store

The base warehouse (store), which is declared as tax warehouse. `Required` `Filter(multi eq)`

_Type_: **[Stores](Logistics.Inventory.Stores.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list limit=1000 erp.entity=Finance.Excise.TaxWarehouses erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Finance.Excise.TaxWarehouses erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Excise_TaxWarehouses?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Excise_TaxWarehouses?$top=10>

