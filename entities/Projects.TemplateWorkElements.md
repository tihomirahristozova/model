---
uid: Projects.TemplateWorkElements
---
# Projects.TemplateWorkElements

Contains project work elements, which shall be copied to projects, based on the specified template. Entity: Prj_Template_Work_Elements

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Projects.TemplateWorkElements.md#Id) | guid |  

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [ProjectTemplate](Projects.TemplateWorkElements.md#ProjectTemplate) | [Projects.Templates](Projects.Templates.md) | The [Template](Projects.Templates.md) to which this TemplateWorkElement belongs. [Required] [Filter(multi eq)] [Owner] |
| [ProjectTypeWorkElement](Projects.TemplateWorkElements.md#ProjectTypeWorkElement) | [Projects.TypeWorkElements](Projects.TypeWorkElements.md) | The work element from the project type, which shall be copied as work element in new projects, based on this template. [Required] [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  


## Reference Details

### ProjectTemplate

> The [Template](Projects.Templates.md) to which this TemplateWorkElement belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Projects.Templates](Projects.Templates.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### ProjectTypeWorkElement

> The work element from the project type, which shall be copied as work element in new projects, based on this template. [Required] [Filter(multi eq)]

_Type_: **[Projects.TypeWorkElements](Projects.TypeWorkElements.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



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

