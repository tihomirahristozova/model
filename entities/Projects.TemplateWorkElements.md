---
uid: Projects.TemplateWorkElements
---
# Projects.TemplateWorkElements Entity

**Namespace:** [Projects](Projects.md)  

Contains project work elements, which shall be copied to projects, based on the specified template. Entity: Prj_Template_Work_Elements

## Default Visualization
Default Display Text Format:  
_{ProjectTemplate.ProjectTemplateName:T}_  
Default Search Member:  
_ProjectTemplate.ProjectTemplateName_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[Projects.Templates](Projects.Templates.md)  
Aggregate Root:  
[Projects.Templates](Projects.Templates.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Projects.TemplateWorkElements.md#id) | guid |  

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [ProjectTemplate](Projects.TemplateWorkElements.md#projecttemplate) | [Templates](Projects.Templates.md) | The `Template`(Projects.Templates.md) to which this TemplateWorkElement belongs. `Required` `Filter(multi eq)` `Owner` |
| [ProjectTypeWorkElement](Projects.TemplateWorkElements.md#projecttypeworkelement) | [TypeWorkElements](Projects.TypeWorkElements.md) | The work element from the project type, which shall be copied as work element in new projects, based on this template. `Required` `Filter(multi eq)` |


## Attribute Details

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  


## Reference Details

### ProjectTemplate

The `Template`(Projects.Templates.md) to which this TemplateWorkElement belongs. `Required` `Filter(multi eq)` `Owner`

_Type_: **[Templates](Projects.Templates.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Can filter by attributes of referenced entity_: **True**  

### ProjectTypeWorkElement

The work element from the project type, which shall be copied as work element in new projects, based on this template. `Required` `Filter(multi eq)`

_Type_: **[TypeWorkElements](Projects.TypeWorkElements.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Projects.TemplateWorkElements erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Projects.TemplateWorkElements erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Projects_TemplateWorkElements?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Projects_TemplateWorkElements?$top=10>

