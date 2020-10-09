---
uid: Projects.TemplateWorkElements
---
# Projects.TemplateWorkElements

Contains project work elements, which shall be copied to projects, based on the specified template. Entity: Prj_Template_Work_Elements

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Projects.TemplateWorkElements.md#id) | guid |  

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [ProjectTemplate](Projects.TemplateWorkElements.md#projecttemplate) | [Templates](Projects.Templates.md) | The [Template](Projects.Templates.md) to which this TemplateWorkElement belongs. [Required] [Filter(multi eq)] [Owner] |
| [ProjectTypeWorkElement](Projects.TemplateWorkElements.md#projecttypeworkelement) | [TypeWorkElements](Projects.TypeWorkElements.md) | The work element from the project type, which shall be copied as work element in new projects, based on this template. [Required] [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  


## Reference Details

### ProjectTemplate

> The [Template](Projects.Templates.md) to which this TemplateWorkElement belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Templates](Projects.Templates.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### ProjectTypeWorkElement

> The work element from the project type, which shall be copied as work element in new projects, based on this template. [Required] [Filter(multi eq)]

_Type_: **[TypeWorkElements](Projects.TypeWorkElements.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Projects.TemplateWorkElements erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Projects.TemplateWorkElements erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Projects.TemplateWorkElements erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Projects_TemplateWorkElements?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Projects_TemplateWorkElements?$top=10>

