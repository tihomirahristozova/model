---
uid: Projects.ProjectRiskDiscussion
---
# Projects.ProjectRiskDiscussion

Contains discussions on project risks. Entity: Prj_Project_Risk_Discussion

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Projects.ProjectRiskDiscussion.md#Id) | guid |  
| [ContributionTime](Projects.ProjectRiskDiscussion.md#ContributionTime) | datetime | The time, when the message was contributed. [Required] [Default(Now)] [Filter(eq)] [ReadOnly] 
| [LastEditTime](Projects.ProjectRiskDiscussion.md#LastEditTime) | datetime (nullable) | Contains the last edit time of the message. null if the message was never edited. [Filter(eq)] [ReadOnly] 
| [Message](Projects.ProjectRiskDiscussion.md#Message) | string | The contents of the message. [Required] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [ContributedByUser](Projects.ProjectRiskDiscussion.md#ContributedByUser) | [Systems.Security.Users](Systems.Security.Users.md) | The user, who contributed (wrote) the message. [Required] [Filter(multi eq)] [ReadOnly] |
| [ProjectRisk](Projects.ProjectRiskDiscussion.md#ProjectRisk) | [Projects.ProjectRisks](Projects.ProjectRisks.md) | The [ProjectRisk](Projects.ProjectRiskDiscussion.md#ProjectRisk) to which this ProjectRiskDiscussion belongs. [Required] [Filter(multi eq)] [Owner] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### ContributionTime

> The time, when the message was contributed. [Required] [Default(Now)] [Filter(eq)] [ReadOnly]

_Type_: **datetime**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **CurrentDateTime**  

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

_Type_: **[Systems.Security.Users](Systems.Security.Users.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### ProjectRisk

> The [ProjectRisk](Projects.ProjectRiskDiscussion.md#ProjectRisk) to which this ProjectRiskDiscussion belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Projects.ProjectRisks](Projects.ProjectRisks.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



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

