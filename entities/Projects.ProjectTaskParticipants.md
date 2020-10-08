---
uid: Projects.ProjectTaskParticipants
---
# Projects.ProjectTaskParticipants

Contains the participants in the project tasks. Entity: Prj_Project_Task_Participants

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Projects.ProjectTaskParticipants.md#id) | guid |  
| [Notes](Projects.ProjectTaskParticipants.md#notes) | string (nullable) | Notes for this ProjectTaskParticipant. 
| [NotifyOnStatusChange](Projects.ProjectTaskParticipants.md#notifyonstatuschange) | boolean | Specifies whether the participant should be notified on task status changes. [Required] [Default(true)] 
| [WorkLoadPercent](Projects.ProjectTaskParticipants.md#workloadpercent) | decimal | The planned work load (in percents) of the participant for this task. [Required] [Default(1)] [Filter(eq)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [ParticipantPerson](Projects.ProjectTaskParticipants.md#participantperson) | [General.Contacts.Persons](General.Contacts.Persons.md) | The person, who is planned to participate in the project task. [Required] [Filter(multi eq)] |
| [ProjectTask](Projects.ProjectTaskParticipants.md#projecttask) | [Projects.ProjectTasks](Projects.ProjectTasks.md) | The project task for which the participant is planned. [Required] [Filter(multi eq)] [Owner] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Notes

> Notes for this ProjectTaskParticipant.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### NotifyOnStatusChange

> Specifies whether the participant should be notified on task status changes. [Required] [Default(true)]

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### WorkLoadPercent

> The planned work load (in percents) of the participant for this task. [Required] [Default(1)] [Filter(eq)]

_Type_: **decimal**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **1**  


## Reference Details

### ParticipantPerson

> The person, who is planned to participate in the project task. [Required] [Filter(multi eq)]

_Type_: **[General.Contacts.Persons](General.Contacts.Persons.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### ProjectTask

> The project task for which the participant is planned. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Projects.ProjectTasks](Projects.ProjectTasks.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Projects.ProjectTaskParticipants erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Projects.ProjectTaskParticipants erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Projects.ProjectTaskParticipants erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Projects_ProjectTaskParticipants?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Projects_ProjectTaskParticipants?$top=10>

