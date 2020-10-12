---
uid: General.Resources.ResourceInstances
---
# General.Resources.ResourceInstances Entity

Represents concrete instances of resources. Entity: Gen_Resource_Instances

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Code](General.Resources.ResourceInstances.md#code) | string | Code of the instance, unique within the resource. [Required] [Filter(eq;like)] 
| [Id](General.Resources.ResourceInstances.md#id) | guid |  
| [Name](General.Resources.ResourceInstances.md#name) | string | Multilanguage resource instance name. [Required] [Filter(eq;like)] 
| [Notes](General.Resources.ResourceInstances.md#notes) | string (nullable) | Notes for this ResourceInstance. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Asset](General.Resources.ResourceInstances.md#asset) | [Assets](Finance.Assets.Assets.md) (nullable) | The asset, which is represented by this resource instance. null, when the resource instance is not an asset. [Filter(multi eq)] |
| [Party](General.Resources.ResourceInstances.md#party) | [Parties](General.Contacts.Parties.md) (nullable) | The party, which is represented by this resource instance. null, when the resource instance is not a party. [Filter(multi eq)] |
| [Resource](General.Resources.ResourceInstances.md#resource) | [Resources](General.Resources.Resources.md) | The resource of which this is instance. [Required] [Filter(multi eq)] [Owner] |


## Attribute Details

### Code

Code of the instance, unique within the resource. [Required] [Filter(eq;like)]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

Multilanguage resource instance name. [Required] [Filter(eq;like)]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### Notes

Notes for this ResourceInstance.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### Asset

The asset, which is represented by this resource instance. null, when the resource instance is not an asset. [Filter(multi eq)]

_Type_: **[Assets](Finance.Assets.Assets.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### Party

The party, which is represented by this resource instance. null, when the resource instance is not a party. [Filter(multi eq)]

_Type_: **[Parties](General.Contacts.Parties.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### Resource

The resource of which this is instance. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Resources](General.Resources.Resources.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=General.Resources.ResourceInstances erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.Resources.ResourceInstances erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_Resources_ResourceInstances?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_Resources_ResourceInstances?$top=10>

