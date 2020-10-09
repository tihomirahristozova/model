---
uid: Projects.ProjectRiskDiscussion
---
# Projects.ProjectRiskDiscussion

Contains discussions on project risks. Entity: Prj_Project_Risk_Discussion

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [ContributionTime](Projects.ProjectRiskDiscussion.md#contributiontime) | datetime | The time, when the message was contributed. [Required] [Default(Now)] [Filter(eq)] [ReadOnly] 
| [Id](Projects.ProjectRiskDiscussion.md#id) | guid |  
| [LastEditTime](Projects.ProjectRiskDiscussion.md#lastedittime) | datetime (nullable) | Contains the last edit time of the message. null if the message was never edited. [Filter(eq)] [ReadOnly] 
| [Message](Projects.ProjectRiskDiscussion.md#message) | string | The contents of the message. [Required] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [ContributedByUser](Projects.ProjectRiskDiscussion.md#contributedbyuser) | [Users](Systems.Security.Users.md) | The user, who contributed (wrote) the message. [Required] [Filter(multi eq)] [ReadOnly] |
| [ProjectRisk](Projects.ProjectRiskDiscussion.md#projectrisk) | [ProjectRisks](Projects.ProjectRisks.md) | The [ProjectRisk](Projects.ProjectRiskDiscussion.md#projectrisk) to which this ProjectRiskDiscussion belongs. [Required] [Filter(multi eq)] [Owner] |


## Attribute Details

### ContributionTime

> The time, when the message was contributed. [Required] [Default(Now)] [Filter(eq)] [ReadOnly]

_Type_: **datetime**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **CurrentDateTime**  

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### LastEditTime

> Contains the last edit time of the message. null if the message was never edited. [Filter(eq)] [ReadOnly]

_Type_: **datetime (nullable)**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

### Message

> The contents of the message. [Required]

_Type_: **string**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### ContributedByUser

> The user, who contributed (wrote) the message. [Required] [Filter(multi eq)] [ReadOnly]

_Type_: **[Users](Systems.Security.Users.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### ProjectRisk

> The [ProjectRisk](Projects.ProjectRiskDiscussion.md#projectrisk) to which this ProjectRiskDiscussion belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[ProjectRisks](Projects.ProjectRisks.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Projects.ProjectRiskDiscussion erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Projects.ProjectRiskDiscussion erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Projects.ProjectRiskDiscussion erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Projects_ProjectRiskDiscussion?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Projects_ProjectRiskDiscussion?$top=10>

