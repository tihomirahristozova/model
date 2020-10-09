---
uid: Projects.TaskTypes
---
# Projects.TaskTypes Entity

Represents the different types of tasks, which can be included in the projects. Entity: Prj_Task_Types

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Description](Projects.TaskTypes.md#description) | [MultilanguageString](../data-types.md#multilanguagestring) (nullable) | Multilanguage description of the task type. 
| [DisplayOrder](Projects.TaskTypes.md#displayorder) | int32 | Display order position of the task. Lowest numbers are shown first (on top). [Required] [Default(1)] 
| [Icon](Projects.TaskTypes.md#icon) | byte[] (nullable) | Icon representing the task type. Preferrably 32x32 pixels. 
| [Id](Projects.TaskTypes.md#id) | guid |  
| [Name](Projects.TaskTypes.md#name) | [MultilanguageString](../data-types.md#multilanguagestring) | The multilanguage task type name. [Required] [Filter(multi eq;like)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [ProjectType](Projects.TaskTypes.md#projecttype) | [ProjectTypes](Projects.ProjectTypes.md) (nullable) | When not null, specifies that this task type can be used only for projects of the specified type. [Filter(multi eq)] |


## Attribute Details

### Description

Multilanguage description of the task type.

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring) (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### DisplayOrder

Display order position of the task. Lowest numbers are shown first (on top). [Required] [Default(1)]

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **1**  

### Icon

Icon representing the task type. Preferrably 32x32 pixels.

_Type_: **byte[] (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

The multilanguage task type name. [Required] [Filter(multi eq;like)]

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring)**  
_Supported Filters_: **Equals, Like, EqualsIn**  
_Supports Order By_: **False**  


## Reference Details

### ProjectType

When not null, specifies that this task type can be used only for projects of the specified type. [Filter(multi eq)]

_Type_: **[ProjectTypes](Projects.ProjectTypes.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Projects.TaskTypes erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Projects.TaskTypes erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Projects_TaskTypes?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Projects_TaskTypes?$top=10>

