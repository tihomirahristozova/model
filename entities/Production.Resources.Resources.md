---
uid: Production.Resources.Resources
---
# Production.Resources.Resources

Resource types available to production. Entity: Prd_Resources

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Production.Resources.Resources.md#Id) | guid |  
| [Notes](Production.Resources.Resources.md#Notes) | string (nullable) | User notes for the resource. 
| [Name](Production.Resources.Resources.md#Name) | string | Name of the resource. [Required] [Filter(like)] 
| [SetupDurationHours](Production.Resources.Resources.md#SetupDurationHours) | decimal | The usual duration of setup when changing production. [Required] [Default(0)] 
| [SetupScrapQuantity](Production.Resources.Resources.md#SetupScrapQuantity) | [Quantity](../data-types.md#Quantity) | The usual quantity of fixed scrap occurring when changing production. . [Unit: SetupScrapUnit] [Required] [Default(0)] 
| [StandardCostPerHour](Production.Resources.Resources.md#StandardCostPerHour) | [Amount](../data-types.md#Amount) (nullable) | Standard cost per hour for this resource. It participates in the calculation of standard cost for production recipes in which the current resource is used. [Currency: ResourceCurrency] 
| [StandardPricePerHour](Production.Resources.Resources.md#StandardPricePerHour) | [Amount](../data-types.md#Amount) (nullable) | Standard price per hour for this resource. It participates in the calculation of standard price for production recipes in which the current resource is used. [Currency: ResourceCurrency] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [PrimaryUnit](Production.Resources.Resources.md#PrimaryUnit) | [General.MeasurementUnits](General.MeasurementUnits.md) | Primary measurement unit for quantities of the resource. [Required] [Filter(multi eq)] |
| [ResourceCurrency](Production.Resources.Resources.md#ResourceCurrency) | [General.Currencies](General.Currencies.md) (nullable) | Currency for this resource. This currency applies for the standard price and cost per hour. [Filter(multi eq)] |
| [ResourceGroup](Production.Resources.Resources.md#ResourceGroup) | [Production.Resources.ResourceGroups](Production.Resources.ResourceGroups.md) | The Id of the containing resource group. [Required] [Filter(multi eq)] [Owner] |
| [SetupScrapUnit](Production.Resources.Resources.md#SetupScrapUnit) | [General.MeasurementUnits](General.MeasurementUnits.md) | The measurement units of Setup_Scrap_Quantity. [Required] [Filter(multi eq)] |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Functions | [Production.Resources.ResourceFunctions](Production.Resources.ResourceFunctions.md) | List of [ResourceFunction](Production.Resources.ResourceFunctions.md) child objects, based on the [Production.Resources.ResourceFunction.Resource](Production.Resources.ResourceFunctions.md#Resource) back reference 


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### Notes

> User notes for the resource.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Name

> Name of the resource. [Required] [Filter(like)]

_Type_: **string**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### SetupDurationHours

> The usual duration of setup when changing production. [Required] [Default(0)]

_Type_: **decimal**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### SetupScrapQuantity

> The usual quantity of fixed scrap occurring when changing production. . [Unit: SetupScrapUnit] [Required] [Default(0)]

_Type_: **[Quantity](../data-types.md#Quantity)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### StandardCostPerHour

> Standard cost per hour for this resource. It participates in the calculation of standard cost for production recipes in which the current resource is used. [Currency: ResourceCurrency]

_Type_: **[Amount](../data-types.md#Amount) (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### StandardPricePerHour

> Standard price per hour for this resource. It participates in the calculation of standard price for production recipes in which the current resource is used. [Currency: ResourceCurrency]

_Type_: **[Amount](../data-types.md#Amount) (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### PrimaryUnit

> Primary measurement unit for quantities of the resource. [Required] [Filter(multi eq)]

_Type_: **[General.MeasurementUnits](General.MeasurementUnits.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### ResourceCurrency

> Currency for this resource. This currency applies for the standard price and cost per hour. [Filter(multi eq)]

_Type_: **[General.Currencies](General.Currencies.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### ResourceGroup

> The Id of the containing resource group. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Production.Resources.ResourceGroups](Production.Resources.ResourceGroups.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### SetupScrapUnit

> The measurement units of Setup_Scrap_Quantity. [Required] [Filter(multi eq)]

_Type_: **[General.MeasurementUnits](General.MeasurementUnits.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Production.Resources.Resources erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Production.Resources.Resources erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Production.Resources.Resources erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Production_Resources_Resources?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Production_Resources_Resources?$top=10>

