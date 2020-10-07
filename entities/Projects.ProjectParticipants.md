# Projects.ProjectParticipants

Represents participant in a project, with a specific role. The same participant can participate multiple times in different roles. Entity: Prj_Project_Participants

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Projects.ProjectParticipants.md#Id) | guid |  
| [Notes](Projects.ProjectParticipants.md#Notes) | string (nullable) | Notes for this ProjectParticipant. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [ParticipantParty](Projects.ProjectParticipants.md#ParticipantParty) | [General.Contacts.Parties](General.Contacts.Parties.md) | The party Id of the participant. [Required] [Filter(multi eq)] |
| [Project](Projects.ProjectParticipants.md#Project) | [Projects.Projects](Projects.Projects.md) | The project in which the participant will participate. [Required] [Filter(multi eq)] [Owner] |
| [ProjectTypeRole](Projects.ProjectParticipants.md#ProjectTypeRole) | [Projects.TypeRoles](Projects.TypeRoles.md) (nullable) | The role which the participant will play in the project. null means that the role is undefined. [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### Notes

> Notes for this ProjectParticipant.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### ParticipantParty

> The party Id of the participant. [Required] [Filter(multi eq)]

_Type_: **[General.Contacts.Parties](General.Contacts.Parties.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Project

> The project in which the participant will participate. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Projects.Projects](Projects.Projects.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### ProjectTypeRole

> The role which the participant will play in the project. null means that the role is undefined. [Filter(multi eq)]

_Type_: **[Projects.TypeRoles](Projects.TypeRoles.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Projects.ProjectParticipants erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Projects.ProjectParticipants erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Projects.ProjectParticipants erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Projects_ProjectParticipants?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Projects_ProjectParticipants?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Prj_Project_Participants?$top=10>

