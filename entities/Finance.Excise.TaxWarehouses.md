---
uid: Finance.Excise.TaxWarehouses
---
# Finance.Excise.TaxWarehouses Entity

**Namespace:** [Finance.Excise](Finance.Excise.md)  

Contains excise-related data for warehouses (stores), which are defined as tax warehouses. Products subject to excise duties must be produced in tax warehouses. They can also be stored, under duty suspension, in these tax warehouses. Entity: Exc_Tax_Warehouses (Introduced in version 21.1.1.1)

## Default Visualization
Default Display Text Format:  
_{Name:T} : {TaxWarehouseExciseNumber}_  
Default Search Member:  
_Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Finance.Excise.TaxWarehouses](Finance.Excise.TaxWarehouses.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Finance.Excise.TaxWarehouses.md#id) | guid |  
| [Name](Finance.Excise.TaxWarehouses.md#name) | [MultilanguageString](../data-types.md#multilanguagestring) | Tax Warehouse Name (Multilanguage). `Required` `Filter(like)` `Introduced in version 21.1.3.93` 
| [TaxWarehouseExciseNumber](Finance.Excise.TaxWarehouses.md#taxwarehouseexcisenumber) | string (32) | The excise identification number of the tax warehouse, issued by the competent authorities. `Required` `Default("-")` `Introduced in version 21.1.3.87` 
| [TraderExciseNumber](Finance.Excise.TaxWarehouses.md#traderexcisenumber) | string (32) | The excise identification number of the owner of the Tax Warehouse. `Required` `Default("-")` `Introduced in version 21.1.3.87` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [EnterpriseCompany](Finance.Excise.TaxWarehouses.md#enterprisecompany) | [EnterpriseCompanies](General.EnterpriseCompanies.md) | The Enterprise company to which the tax warehouse belongs. `Required` `Filter(multi eq)` `Introduced in version 21.1.3.91` |


## Attribute Details

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

Tax Warehouse Name (Multilanguage). `Required` `Filter(like)` `Introduced in version 21.1.3.93`

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

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

### EnterpriseCompany

The Enterprise company to which the tax warehouse belongs. `Required` `Filter(multi eq)` `Introduced in version 21.1.3.91`

_Type_: **[EnterpriseCompanies](General.EnterpriseCompanies.md)**  
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

