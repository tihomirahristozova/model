---
uid: General.Resources.Resources
---
# General.Resources.Resources

Enterprise resources, categorized by groups. Entity: Gen_Resources

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](General.Resources.Resources.md#Id) | guid |  
| [Notes](General.Resources.Resources.md#Notes) | string (nullable) | Notes for this Resource. 
| [Name](General.Resources.Resources.md#Name) | [MultilanguageString](../data-types.md#MultilanguageString) | Resource name. Unique within the resource group. [Required] [Filter(eq;like)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [CostingCurrency](General.Resources.Resources.md#CostingCurrency) | [General.Currencies](General.Currencies.md) (nullable) | The currency in which resource costs are specified. Required only if resource costs will be specified. [Filter(multi eq)] |
| [ResourceGroup](General.Resources.Resources.md#ResourceGroup) | [General.Resources.ResourceGroups](General.Resources.ResourceGroups.md) | The [ResourceGroup](General.Resources.Resources.md#ResourceGroup) to which this Resource belongs. [Required] [Filter(multi eq)] [Owner] |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Availability | [General.Resources.ResourceAvailability](General.Resources.ResourceAvailability.md) | List of [ResourceAvailability](General.Resources.ResourceAvailability.md) child objects, based on the [General.Resources.ResourceAvailability.Resource](General.Resources.ResourceAvailability.md#Resource) back reference 
| CostRates | [General.Resources.ResourceCostRates](General.Resources.ResourceCostRates.md) | List of [ResourceCostRate](General.Resources.ResourceCostRates.md) child objects, based on the [General.Resources.ResourceCostRate.Resource](General.Resources.ResourceCostRates.md#Resource) back reference 
| Instances | [General.Resources.ResourceInstances](General.Resources.ResourceInstances.md) | List of [ResourceInstance](General.Resources.ResourceInstances.md) child objects, based on the [General.Resources.ResourceInstance.Resource](General.Resources.ResourceInstances.md#Resource) back reference 


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### Notes

> Notes for this Resource.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Name

> Resource name. Unique within the resource group. [Required] [Filter(eq;like)]

_Type_: **[MultilanguageString](../data-types.md#MultilanguageString)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  


## Reference Details

### CostingCurrency

> The currency in which resource costs are specified. Required only if resource costs will be specified. [Filter(multi eq)]

_Type_: **[General.Currencies](General.Currencies.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### ResourceGroup

> The [ResourceGroup](General.Resources.Resources.md#ResourceGroup) to which this Resource belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[General.Resources.ResourceGroups](General.Resources.ResourceGroups.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=General.Resources.Resources erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.Resources.Resources erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=General.Resources.Resources erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_Resources_Resources?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_Resources_Resources?$top=10>

