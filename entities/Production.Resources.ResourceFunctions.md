---
uid: Production.Resources.ResourceFunctions
---
# Production.Resources.ResourceFunctions

List of functions that a specific resource is able to perform. Entity: Prd_Resource_Functions

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Production.Resources.ResourceFunctions.md#Id) | guid |  
| [Notes](Production.Resources.ResourceFunctions.md#Notes) | string (nullable) | User notes on the resource function. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Function](Production.Resources.ResourceFunctions.md#Function) | [Production.Resources.Functions](Production.Resources.Functions.md) | Function, which the resource can perform. [Required] [Filter(multi eq)] |
| [Resource](Production.Resources.ResourceFunctions.md#Resource) | [Production.Resources.Resources](Production.Resources.Resources.md) | The [Resource](Production.Resources.ResourceFunctions.md#Resource) to which this ResourceFunction belongs. [Required] [Filter(multi eq)] [Owner] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### Notes

> User notes on the resource function.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### Function

> Function, which the resource can perform. [Required] [Filter(multi eq)]

_Type_: **[Production.Resources.Functions](Production.Resources.Functions.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Resource

> The [Resource](Production.Resources.ResourceFunctions.md#Resource) to which this ResourceFunction belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Production.Resources.Resources](Production.Resources.Resources.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Production.Resources.ResourceFunctions erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Production.Resources.ResourceFunctions erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Production.Resources.ResourceFunctions erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Production_Resources_ResourceFunctions?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Production_Resources_ResourceFunctions?$top=10>

