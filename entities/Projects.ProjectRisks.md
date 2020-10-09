---
uid: Projects.ProjectRisks
---
# Projects.ProjectRisks

Contains risks, associated to projects. Entity: Prj_Project_Risks

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [CreateDate](Projects.ProjectRisks.md#createdate) | date | The creation date of the project risk. [Required] [Default(Now)] [Filter(eq)] 
| [Description](Projects.ProjectRisks.md#description) | string (nullable) | The description of this ProjectRisk. [Filter(like)] 
| [Id](Projects.ProjectRisks.md#id) | guid |  
| [ImpactPercent](Projects.ProjectRisks.md#impactpercent) | decimal | The impact of the risk to the project, expressed as percentage of the total project value. [Required] [Default(0)] 
| [ProbabilityPercent](Projects.ProjectRisks.md#probabilitypercent) | decimal | The probability of the risk occurring. [Required] [Default(0)] 
| [ResolutionStrategy](Projects.ProjectRisks.md#resolutionstrategy) | string (nullable) | The strategy chosen to handle the risk. [Filter(eq)] 
| [Resolved](Projects.ProjectRisks.md#resolved) | boolean | True if the risk is resolved. [Required] [Default(false)] [Filter(eq)] 
| [ResolveDate](Projects.ProjectRisks.md#resolvedate) | date (nullable) | The date on which the risk is resolved. [Filter(eq)] 
| [RiskName](Projects.ProjectRisks.md#riskname) | string | The short name of the risk. [Required] [Filter(multi eq)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Project](Projects.ProjectRisks.md#project) | [Projects](Projects.Projects.md) | The project for which this risk applies. [Required] [Filter(multi eq)] [Owner] |
| [ResponsiblePerson](Projects.ProjectRisks.md#responsibleperson) | [Persons](General.Contacts.Persons.md) (nullable) | The person who is responsible for handling the risk. [Filter(multi eq)] |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Discussion | [ProjectRiskDiscussion](Projects.ProjectRiskDiscussion.md) | List of [ProjectRiskDiscussion](Projects.ProjectRiskDiscussion.md) child objects, based on the [Projects.ProjectRiskDiscussion.ProjectRisk](Projects.ProjectRiskDiscussion.md#projectrisk) back reference 


## Attribute Details

### CreateDate

> The creation date of the project risk. [Required] [Default(Now)] [Filter(eq)]

_Type_: **date**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **CurrentDateTime**  

### Description

> The description of this ProjectRisk. [Filter(like)]

_Type_: **string (nullable)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### ImpactPercent

> The impact of the risk to the project, expressed as percentage of the total project value. [Required] [Default(0)]

_Type_: **decimal**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### ProbabilityPercent

> The probability of the risk occurring. [Required] [Default(0)]

_Type_: **decimal**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### ResolutionStrategy

> The strategy chosen to handle the risk. [Filter(eq)]

_Type_: **string (nullable)**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

### Resolved

> True if the risk is resolved. [Required] [Default(false)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### ResolveDate

> The date on which the risk is resolved. [Filter(eq)]

_Type_: **date (nullable)**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

### RiskName

> The short name of the risk. [Required] [Filter(multi eq)]

_Type_: **string**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  


## Reference Details

### Project

> The project for which this risk applies. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Projects](Projects.Projects.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### ResponsiblePerson

> The person who is responsible for handling the risk. [Filter(multi eq)]

_Type_: **[Persons](General.Contacts.Persons.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Projects.ProjectRisks erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Projects.ProjectRisks erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Projects.ProjectRisks erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Projects_ProjectRisks?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Projects_ProjectRisks?$top=10>

