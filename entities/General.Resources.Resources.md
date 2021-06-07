---
uid: General.Resources.Resources
---
# General.Resources.Resources Entity

**Namespace:** [General.Resources](General.Resources.md)  

Enterprise resources, categorized by groups. Entity: Gen_Resources

## Default Visualization
Default Display Text Format:  
_{Name:T}_  
Default Search Member:  
_Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[General.Resources.ResourceGroups](General.Resources.ResourceGroups.md)  
Aggregate Root:  
[General.Resources.ResourceGroups](General.Resources.ResourceGroups.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](General.Resources.Resources.md#id) | guid |  
| [Name](General.Resources.Resources.md#name) | [MultilanguageString](../data-types.md#multilanguagestring) | Resource name. Unique within the resource group. `Required` `Filter(eq;like)` 
| [Notes](General.Resources.Resources.md#notes) | string (max) __nullable__ | Notes for this Resource. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [CostingCurrency](General.Resources.Resources.md#costingcurrency) | [Currencies](General.Currencies.md) (nullable) | The currency in which resource costs are specified. Required only if resource costs will be specified. `Filter(multi eq)` |
| [ResourceGroup](General.Resources.Resources.md#resourcegroup) | [ResourceGroups](General.Resources.ResourceGroups.md) | The `ResourceGroup`(General.Resources.Resources.md#resourcegroup) to which this Resource belongs. `Required` `Filter(multi eq)` `Owner` |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Availability | [ResourceAvailability](General.Resources.ResourceAvailability.md) | List of `ResourceAvailability`(General.Resources.ResourceAvailability.md) child objects, based on the `General.Resources.ResourceAvailability.Resource`(General.Resources.ResourceAvailability.md#resource) back reference 
| CostRates | [ResourceCostRates](General.Resources.ResourceCostRates.md) | List of `ResourceCostRate`(General.Resources.ResourceCostRates.md) child objects, based on the `General.Resources.ResourceCostRate.Resource`(General.Resources.ResourceCostRates.md#resource) back reference 
| Instances | [ResourceInstances](General.Resources.ResourceInstances.md) | List of `ResourceInstance`(General.Resources.ResourceInstances.md) child objects, based on the `General.Resources.ResourceInstance.Resource`(General.Resources.ResourceInstances.md#resource) back reference 


## Attribute Details

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

Resource name. Unique within the resource group. `Required` `Filter(eq;like)`

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### Notes

Notes for this Resource.

_Type_: **string (max) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  


## Reference Details

### CostingCurrency

The currency in which resource costs are specified. Required only if resource costs will be specified. `Filter(multi eq)`

_Type_: **[Currencies](General.Currencies.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### ResourceGroup

The `ResourceGroup`(General.Resources.Resources.md#resourcegroup) to which this Resource belongs. `Required` `Filter(multi eq)` `Owner`

_Type_: **[ResourceGroups](General.Resources.ResourceGroups.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  



## Business Rules

[!list erp.entity=General.Resources.Resources erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.Resources.Resources erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_Resources_Resources?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_Resources_Resources?$top=10>

