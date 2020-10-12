---
uid: General.Geography.Areas
---
# General.Geography.Areas Entity

Areas are user-defined division of the sales territories. Entity: Gen_Areas

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Code](General.Geography.Areas.md#code) | string | The unique code of the Area. [Required] [Filter(eq;like)] [ORD] 
| [FullPath](General.Geography.Areas.md#fullpath) | string (nullable) | Full path to the area, starting with '/' and containing the area codes of all parent areas using '/' as separator and terminator. For example root area with code 'BG' would have full path = '/BG/'. [Filter(eq;like)] [ReadOnly] 
| [Id](General.Geography.Areas.md#id) | guid |  
| [Name](General.Geography.Areas.md#name) | [MultilanguageString](../data-types.md#multilanguagestring) | The name of this Area. [Required] [Filter(eq;like)] [ORD] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Parent](General.Geography.Areas.md#parent) | [Areas](General.Geography.Areas.md) (nullable) | Parent area in the hierarchy. [Filter(multi eq)] |


## Attribute Details

### Code

The unique code of the Area. [Required] [Filter(eq;like)] [ORD]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  

### FullPath

Full path to the area, starting with '/' and containing the area codes of all parent areas using '/' as separator and terminator. For example root area with code 'BG' would have full path = '/BG/'. [Filter(eq;like)] [ReadOnly]

_Type_: **string (nullable)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

The name of this Area. [Required] [Filter(eq;like)] [ORD]

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  


## Reference Details

### Parent

Parent area in the hierarchy. [Filter(multi eq)]

_Type_: **[Areas](General.Geography.Areas.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=General.Geography.Areas erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.Geography.Areas erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_Geography_Areas?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_Geography_Areas?$top=10>

