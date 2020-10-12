---
uid: Projects.TemplateRisks
---
# Projects.TemplateRisks Entity

Contains project risks, which will be copied to projects, based on the template. Entity: Prj_Template_Risks

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Description](Projects.TemplateRisks.md#description) | string (nullable) | The description of this TemplateRisk. 
| [Id](Projects.TemplateRisks.md#id) | guid |  
| [ImpactPercent](Projects.TemplateRisks.md#impactpercent) | decimal | The impact of the risk to the project, expressed as percentage of the total project value. [Required] [Default(0)] 
| [ProbabilityPercent](Projects.TemplateRisks.md#probabilitypercent) | decimal | The probability of the risk occurring. [Required] [Default(0)] 
| [RiskName](Projects.TemplateRisks.md#riskname) | string | The name of the risk. [Required] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [ProjectTemplate](Projects.TemplateRisks.md#projecttemplate) | [Templates](Projects.Templates.md) | The [Template](Projects.Templates.md) to which this TemplateRisk belongs. [Required] [Filter(multi eq)] [Owner] |


## Attribute Details

### Description

The description of this TemplateRisk.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### ImpactPercent

The impact of the risk to the project, expressed as percentage of the total project value. [Required] [Default(0)]

_Type_: **decimal**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### ProbabilityPercent

The probability of the risk occurring. [Required] [Default(0)]

_Type_: **decimal**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### RiskName

The name of the risk. [Required]

_Type_: **string**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### ProjectTemplate

The [Template](Projects.Templates.md) to which this TemplateRisk belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Templates](Projects.Templates.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Projects.TemplateRisks erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Projects.TemplateRisks erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Projects_TemplateRisks?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Projects_TemplateRisks?$top=10>

