---
uid: Production.Resources.Functions
---
# Production.Resources.Functions Entity

**Namespace:** [Production.Resources](Production.Resources.md)  

Definition of the functions that the resources can perform. Entity: Prd_Functions

## Default Visualization
Default Display Text Format:  
_{Name}_  
Default Search Members:  
_Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[Production.Resources.FunctionGroups](Production.Resources.FunctionGroups.md)  
Aggregate Root:  
[Production.Resources.FunctionGroups](Production.Resources.FunctionGroups.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Production.Resources.Functions.md#id) | guid |  
| [Name](Production.Resources.Functions.md#name) | string (64) | The name of this Function. `Required` `Filter(like)` 
| [Notes](Production.Resources.Functions.md#notes) | string (254) __nullable__ | User comments on the function. 
| [RowVersion](Production.Resources.Functions.md#rowversion) | byte[] |  

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [FunctionGroup](Production.Resources.Functions.md#functiongroup) | [FunctionGroups](Production.Resources.FunctionGroups.md) | The <see cref="FunctionGroup"/> to which this Function belongs. `Required` `Filter(multi eq)` `Owner` |
| [PrimaryUnit](Production.Resources.Functions.md#primaryunit) | [MeasurementUnits](General.MeasurementUnits.md) | Primary measurement unit for measuring workload of the function. Resources that can perform the function should be measureable in this unit. `Required` `Filter(multi eq)` |


## Attribute Details

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

The name of this Function. `Required` `Filter(like)`

_Type_: **string (64)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  
_Maximum Length_: **64**  

### Notes

User comments on the function.

_Type_: **string (254) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  

### RowVersion

_Type_: **byte[]**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### FunctionGroup

The <see cref="FunctionGroup"/> to which this Function belongs. `Required` `Filter(multi eq)` `Owner`

_Type_: **[FunctionGroups](Production.Resources.FunctionGroups.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  

### PrimaryUnit

Primary measurement unit for measuring workload of the function. Resources that can perform the function should be measureable in this unit. `Required` `Filter(multi eq)`

_Type_: **[MeasurementUnits](General.MeasurementUnits.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list limit=1000 erp.entity=Production.Resources.Functions erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Production.Resources.Functions erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Production_Resources_Functions?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Production_Resources_Functions?$top=10>

