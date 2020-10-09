---
uid: Applications.AssetManagement.TrackedParameters
---
# Applications.AssetManagement.TrackedParameters Entity

Parameters of assets, tracked for maintenance reasons, like car mileage, aircraft cycles, etc. Entity: Eam_Tracked_Parameters (Introduced in version 19.1)

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Code](Applications.AssetManagement.TrackedParameters.md#code) | string | Unique code of the asset parameter. [Required] [Filter(multi eq;like)] [ORD] 
| [Id](Applications.AssetManagement.TrackedParameters.md#id) | guid |  
| [IsActive](Applications.AssetManagement.TrackedParameters.md#isactive) | boolean | Specifies whether the parameter is active for choosing in drop downs. [Required] [Default(true)] [Filter(multi eq)] 
| [Name](Applications.AssetManagement.TrackedParameters.md#name) | [MultilanguageString](../data-types.md#multilanguagestring) | Multilanguage name of the asset parameter. [Required] [Filter(multi eq;like)] 
| [Notes](Applications.AssetManagement.TrackedParameters.md#notes) | string (nullable) | Notes for this TrackedParameter. [Filter(like)] 


## Attribute Details

### Code

Unique code of the asset parameter. [Required] [Filter(multi eq;like)] [ORD]

_Type_: **string**  
_Supported Filters_: **Equals, Like, EqualsIn**  
_Supports Order By_: **True**  

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### IsActive

Specifies whether the parameter is active for choosing in drop downs. [Required] [Default(true)] [Filter(multi eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### Name

Multilanguage name of the asset parameter. [Required] [Filter(multi eq;like)]

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring)**  
_Supported Filters_: **Equals, Like, EqualsIn**  
_Supports Order By_: **False**  

### Notes

Notes for this TrackedParameter. [Filter(like)]

_Type_: **string (nullable)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Applications.AssetManagement.TrackedParameters erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Applications.AssetManagement.TrackedParameters erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_AssetManagement_TrackedParameters?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_AssetManagement_TrackedParameters?$top=10>

