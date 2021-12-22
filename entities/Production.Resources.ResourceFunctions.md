---
uid: Production.Resources.ResourceFunctions
---
# Production.Resources.ResourceFunctions Entity

**Namespace:** [Production.Resources](Production.Resources.md)  

List of functions that a specific resource is able to perform. Entity: Prd_Resource_Functions

## Default Visualization
Default Display Text Format:  
_{Resource.Name}_  
Default Search Members:  
_Resource.Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[Production.Resources.Resources](Production.Resources.Resources.md)  
Aggregate Root:  
[Production.Resources.ResourceGroups](Production.Resources.ResourceGroups.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Production.Resources.ResourceFunctions.md#id) | guid |  
| [Notes](Production.Resources.ResourceFunctions.md#notes) | string (254) __nullable__ | User notes on the resource function. 
| [ObjectVersion](Production.Resources.ResourceFunctions.md#objectversion) | int32 |  

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Function](Production.Resources.ResourceFunctions.md#function) | [Functions](Production.Resources.Functions.md) | Function, which the resource can perform. `Required` `Filter(multi eq)` |
| [Resource](Production.Resources.ResourceFunctions.md#resource) | [Resources](Production.Resources.Resources.md) | The <see cref="Resource"/> to which this ResourceFunction belongs. `Required` `Filter(multi eq)` `Owner` |


## Attribute Details

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Notes

User notes on the resource function.

_Type_: **string (254) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  

### ObjectVersion

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  


## Reference Details

### Function

Function, which the resource can perform. `Required` `Filter(multi eq)`

_Type_: **[Functions](Production.Resources.Functions.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### Resource

The <see cref="Resource"/> to which this ResourceFunction belongs. `Required` `Filter(multi eq)` `Owner`

_Type_: **[Resources](Production.Resources.Resources.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  



## Business Rules

[!list limit=1000 erp.entity=Production.Resources.ResourceFunctions erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Production.Resources.ResourceFunctions erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Production_Resources_ResourceFunctions?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Production_Resources_ResourceFunctions?$top=10>

