---
uid: Projects.Templates
---
# Projects.Templates Entity

Contains templates for creating new projects. Entity: Prj_Templates

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Projects.Templates.md#id) | guid |  
| [Notes](Projects.Templates.md#notes) | string (nullable) | Notes for this Template. 
| [ProjectTemplateName](Projects.Templates.md#projecttemplatename) | string | The name of the project template. [Required] 

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Risks | [TemplateRisks](Projects.TemplateRisks.md) | List of [TemplateRisk](Projects.TemplateRisks.md) child objects, based on the [Projects.TemplateRisk.ProjectTemplate](Projects.TemplateRisks.md#projecttemplate) back reference 
| WorkElements | [TemplateWorkElements](Projects.TemplateWorkElements.md) | List of [TemplateWorkElement](Projects.TemplateWorkElements.md) child objects, based on the [Projects.TemplateWorkElement.ProjectTemplate](Projects.TemplateWorkElements.md#projecttemplate) back reference 


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Notes

> Notes for this Template.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ProjectTemplateName

> The name of the project template. [Required]

_Type_: **string**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Projects.Templates erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Projects.Templates erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Projects.Templates erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Projects_Templates?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Projects_Templates?$top=10>

