---
uid: Projects.ProjectRiskDiscussion
---
# Projects.ProjectRiskDiscussion Entity

**Namespace:** [Projects](Projects.md)  

Contains discussions on project risks. Entity: Prj_Project_Risk_Discussion

## Default Visualization
Default Display Text Format:  
_{ProjectRisk.RiskName:T}_  
Default Search Member:  
_ProjectRisk.RiskName_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[Projects.ProjectRisks](Projects.ProjectRisks.md)  
Aggregate Root:  
[Projects.Projects](Projects.Projects.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [ContributionTime](Projects.ProjectRiskDiscussion.md#contributiontime) | datetime | The time, when the message was contributed. `Required` `Default(Now)` `Filter(eq)` `ReadOnly` 
| [Id](Projects.ProjectRiskDiscussion.md#id) | guid |  
| [LastEditTime](Projects.ProjectRiskDiscussion.md#lastedittime) | datetime __nullable__ | Contains the last edit time of the message. null if the message was never edited. `Filter(eq)` `ReadOnly` 
| [Message](Projects.ProjectRiskDiscussion.md#message) | string (max) | The contents of the message. `Required` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [ContributedByUser](Projects.ProjectRiskDiscussion.md#contributedbyuser) | [Users](Systems.Security.Users.md) | The user, who contributed (wrote) the message. `Required` `Filter(multi eq)` `ReadOnly` |
| [ProjectRisk](Projects.ProjectRiskDiscussion.md#projectrisk) | [ProjectRisks](Projects.ProjectRisks.md) | The `ProjectRisk`(Projects.ProjectRiskDiscussion.md#projectrisk) to which this ProjectRiskDiscussion belongs. `Required` `Filter(multi eq)` `Owner` |


## Attribute Details

### ContributionTime

The time, when the message was contributed. `Required` `Default(Now)` `Filter(eq)` `ReadOnly`

_Type_: **datetime**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **CurrentDateTime**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### LastEditTime

Contains the last edit time of the message. null if the message was never edited. `Filter(eq)` `ReadOnly`

_Type_: **datetime __nullable__**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

### Message

The contents of the message. `Required`

_Type_: **string (max)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  


## Reference Details

### ContributedByUser

The user, who contributed (wrote) the message. `Required` `Filter(multi eq)` `ReadOnly`

_Type_: **[Users](Systems.Security.Users.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### ProjectRisk

The `ProjectRisk`(Projects.ProjectRiskDiscussion.md#projectrisk) to which this ProjectRiskDiscussion belongs. `Required` `Filter(multi eq)` `Owner`

_Type_: **[ProjectRisks](Projects.ProjectRisks.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  



## Business Rules

[!list erp.entity=Projects.ProjectRiskDiscussion erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Projects.ProjectRiskDiscussion erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Projects_ProjectRiskDiscussion?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Projects_ProjectRiskDiscussion?$top=10>

