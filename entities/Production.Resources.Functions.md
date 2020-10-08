---
uid: Production.Resources.Functions
---
# Production.Resources.Functions

Definition of the functions that the resources can perform. Entity: Prd_Functions

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Production.Resources.Functions.md#Id) | guid |  
| [Name](Production.Resources.Functions.md#Name) | string | The name of this Function. [Required] [Filter(like)] 
| [Notes](Production.Resources.Functions.md#Notes) | string (nullable) | User comments on the function. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [FunctionGroup](Production.Resources.Functions.md#FunctionGroup) | [Production.Resources.FunctionGroups](Production.Resources.FunctionGroups.md) | The [FunctionGroup](Production.Resources.Functions.md#FunctionGroup) to which this Function belongs. [Required] [Filter(multi eq)] [Owner] |
| [PrimaryUnit](Production.Resources.Functions.md#PrimaryUnit) | [General.MeasurementUnits](General.MeasurementUnits.md) | Primary measurement unit for measuring workload of the function. Resources that can perform the function should be measureable in this unit. [Required] [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### Name

> The name of this Function. [Required] [Filter(like)]

_Type_: **string**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### Notes

> User comments on the function.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### FunctionGroup

> The [FunctionGroup](Production.Resources.Functions.md#FunctionGroup) to which this Function belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Production.Resources.FunctionGroups](Production.Resources.FunctionGroups.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### PrimaryUnit

> Primary measurement unit for measuring workload of the function. Resources that can perform the function should be measureable in this unit. [Required] [Filter(multi eq)]

_Type_: **[General.MeasurementUnits](General.MeasurementUnits.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Production.Resources.Functions erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Production.Resources.Functions erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Production.Resources.Functions erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Production_Resources_Functions?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Production_Resources_Functions?$top=10>

