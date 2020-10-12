---
uid: General.PropertiesCategories
---
# General.PropertiesCategories Entity

Categories of properties. Entity: Gen_Properties_Categories

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](General.PropertiesCategories.md#id) | guid |  
| [Name](General.PropertiesCategories.md#name) | [MultilanguageString](../data-types.md#multilanguagestring) | The name of this PropertiesCategory. [Required] [Filter(eq;like)] [ORD] 


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

The name of this PropertiesCategory. [Required] [Filter(eq;like)] [ORD]

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  



## Business Rules

[!list erp.entity=General.PropertiesCategories erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.PropertiesCategories erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_PropertiesCategories?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_PropertiesCategories?$top=10>

