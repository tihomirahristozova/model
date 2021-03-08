---
uid: General.Contacts.ActivityParticipants
---
# General.Contacts.ActivityParticipants Entity

**Namespace:** [General.Contacts](General.Contacts.md)  

Contains the additional participants in the activities. These are the participating users, besides the user to which the activitiy is assigned. Entity: Cm_Activity_Participants

## Default Visualization
Default Display Text Format:  
_{Activity.DocumentType.Code}:{Activity.DocumentNo} - {Activity.DocumentType.TypeName:T}_  
Default Search Member:  
_Activity.DocumentType.Code_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[General.Contacts.Activities](General.Contacts.Activities.md)  
Aggregate Root:  
[General.Contacts.Activities](General.Contacts.Activities.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](General.Contacts.ActivityParticipants.md#id) | guid |  
| [Notes](General.Contacts.ActivityParticipants.md#notes) | string (nullable) | Notes for this ActivityParticipant. 
| [WorkLoadPercent](General.Contacts.ActivityParticipants.md#workloadpercent) | decimal | The planned work load of the participant for this activity. `Required` `Default(1)` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Activity](General.Contacts.ActivityParticipants.md#activity) | [Activities](General.Contacts.Activities.md) | The `Activity`(General.Contacts.ActivityParticipants.md#activity) to which this ActivityParticipant belongs. `Required` `Filter(multi eq)` `Owner` |
| [ParticipantPerson](General.Contacts.ActivityParticipants.md#participantperson) | [Persons](General.Contacts.Persons.md) | The person, participating in an activity. `Required` `Filter(multi eq)` |


## Attribute Details

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Notes

Notes for this ActivityParticipant.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### WorkLoadPercent

The planned work load of the participant for this activity. `Required` `Default(1)`

_Type_: **decimal**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **1**  


## Reference Details

### Activity

The `Activity`(General.Contacts.ActivityParticipants.md#activity) to which this ActivityParticipant belongs. `Required` `Filter(multi eq)` `Owner`

_Type_: **[Activities](General.Contacts.Activities.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### ParticipantPerson

The person, participating in an activity. `Required` `Filter(multi eq)`

_Type_: **[Persons](General.Contacts.Persons.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=General.Contacts.ActivityParticipants erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.Contacts.ActivityParticipants erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_Contacts_ActivityParticipants?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_Contacts_ActivityParticipants?$top=10>

