---
uid: Projects.TemplateRisks
---
# Projects.TemplateRisks Entity

**Namespace:** [Projects](Projects.md)  

Contains project risks, which will be copied to projects, based on the template. Entity: Prj_Template_Risks

## Default Visualization
Default Display Text Format:  
_{RiskName:T}_  
Default Search Member:  
_RiskName_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[Projects.Templates](Projects.Templates.md)  
Aggregate Root:  
[Projects.Templates](Projects.Templates.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Description](Projects.TemplateRisks.md#description) | string (max) __nullable__ | The description of this TemplateRisk. 
| [Id](Projects.TemplateRisks.md#id) | guid |  
| [ImpactPercent](Projects.TemplateRisks.md#impactpercent) | decimal (3, 2) | The impact of the risk to the project, expressed as percentage of the total project value. `Required` `Default(0)` 
| [ProbabilityPercent](Projects.TemplateRisks.md#probabilitypercent) | decimal (3, 2) | The probability of the risk occurring. `Required` `Default(0)` 
| [RiskName](Projects.TemplateRisks.md#riskname) | string (254) | The name of the risk. `Required` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [ProjectTemplate](Projects.TemplateRisks.md#projecttemplate) | [Templates](Projects.Templates.md) | The `Template`(Projects.Templates.md) to which this TemplateRisk belongs. `Required` `Filter(multi eq)` `Owner` |


## Attribute Details

### Description

The description of this TemplateRisk.

_Type_: **string (max) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### ImpactPercent

The impact of the risk to the project, expressed as percentage of the total project value. `Required` `Default(0)`

_Type_: **decimal (3, 2)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### ProbabilityPercent

The probability of the risk occurring. `Required` `Default(0)`

_Type_: **decimal (3, 2)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### RiskName

The name of the risk. `Required`

_Type_: **string (254)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  


## Reference Details

### ProjectTemplate

The `Template`(Projects.Templates.md) to which this TemplateRisk belongs. `Required` `Filter(multi eq)` `Owner`

_Type_: **[Templates](Projects.Templates.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Can filter by attributes of referenced entity_: **True**  



## Business Rules

[!list erp.entity=Projects.TemplateRisks erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Projects.TemplateRisks erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Projects_TemplateRisks?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Projects_TemplateRisks?$top=10>

