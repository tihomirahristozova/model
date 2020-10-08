---
uid: Applications.AssetManagement.TrackedParameters
---
# Applications.AssetManagement.TrackedParameters

Parameters of assets, tracked for maintenance reasons, like car mileage, aircraft cycles, etc. Entity: Eam_Tracked_Parameters (Introduced in version 19.1.100.0)

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Applications.AssetManagement.TrackedParameters.md#Id) | guid |  
| [IsActive](Applications.AssetManagement.TrackedParameters.md#IsActive) | boolean | Specifies whether the parameter is active for choosing in drop downs. [Required] [Default(true)] [Filter(multi eq)] 
| [Notes](Applications.AssetManagement.TrackedParameters.md#Notes) | string (nullable) | Notes for this TrackedParameter. [Filter(like)] 
| [Code](Applications.AssetManagement.TrackedParameters.md#Code) | string | Unique code of the asset parameter. [Required] [Filter(multi eq;like)] [ORD] 
| [Name](Applications.AssetManagement.TrackedParameters.md#Name) | [MultilanguageString](../data-types.md#MultilanguageString) | Multilanguage name of the asset parameter. [Required] [Filter(multi eq;like)] 


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### IsActive

> Specifies whether the parameter is active for choosing in drop downs. [Required] [Default(true)] [Filter(multi eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### Notes

> Notes for this TrackedParameter. [Filter(like)]

_Type_: **string (nullable)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### Code

> Unique code of the asset parameter. [Required] [Filter(multi eq;like)] [ORD]

_Type_: **string**  
_Supported Filters_: **Equals, Like, EqualsIn**  
_Supports Order By_: **True**  

### Name

> Multilanguage name of the asset parameter. [Required] [Filter(multi eq;like)]

_Type_: **[MultilanguageString](../data-types.md#MultilanguageString)**  
_Supported Filters_: **Equals, Like, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Applications.AssetManagement.TrackedParameters erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Applications.AssetManagement.TrackedParameters erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Applications.AssetManagement.TrackedParameters erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_AssetManagement_TrackedParameters?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_AssetManagement_TrackedParameters?$top=10>

