---
uid: Finance.Excise.TaxWarehouses
---
# Finance.Excise.TaxWarehouses Entity

Contains excise-related data for warehouses (stores), which are defined as tax warehouses. Products subject to excise duties must be produced in tax warehouses. They can also be stored, under duty suspension, in these tax warehouses. Entity: Exc_Tax_Warehouses (Introduced in version 21.1.1.1)

Default Display Text Format:  
_{Id}_  
Default Search Member:  
_Id_  

Aggregate Tree:  
* [Finance.Excise.TaxWarehouses](Finance.Excise.TaxWarehouses.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Finance.Excise.TaxWarehouses.md#id) | guid |  

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Store](Finance.Excise.TaxWarehouses.md#store) | [Stores](Logistics.Inventory.Stores.md) | The base warehouse (store), which is declared as tax warehouse. [Required] [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  


## Reference Details

### Store

The base warehouse (store), which is declared as tax warehouse. [Required] [Filter(multi eq)]

_Type_: **[Stores](Logistics.Inventory.Stores.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Finance.Excise.TaxWarehouses erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Finance.Excise.TaxWarehouses erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Excise_TaxWarehouses?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Excise_TaxWarehouses?$top=10>

