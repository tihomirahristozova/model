---
uid: General.Contacts.ActivityTimeIntervals
---
# General.Contacts.ActivityTimeIntervals Entity

**Namespace:** [General.Contacts](General.Contacts.md)  

History of work efforts for executing activities (timesheet). Entity: Cm_Activity_Time_Intervals

## Default Visualization
Default Display Text Format:  
_{Party.PartyName:T} : {Party.PartyCode}_  
Default Search Member:  
_Party.PartyName_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[General.Contacts.Parties](General.Contacts.Parties.md)  
Aggregate Root:  
[General.Contacts.Parties](General.Contacts.Parties.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Date](General.Contacts.ActivityTimeIntervals.md#date) | date | The date on which the work was performed. `Required` `Filter(eq;ge;le)` 
| [EndTime](General.Contacts.ActivityTimeIntervals.md#endtime) | time | The ending time of the time interval within 'Date'. `Required` `Filter(ge;le)` 
| [ExecutionCompletePercent](General.Contacts.ActivityTimeIntervals.md#executioncompletepercent) | decimal (3, 2) | Percent of task completed. `Required` `Default(0)` `Filter(ge;le)` 
| [Id](General.Contacts.ActivityTimeIntervals.md#id) | guid |  
| [Notes](General.Contacts.ActivityTimeIntervals.md#notes) | string (254) __nullable__ | Notes for the time interval. 
| [StartTime](General.Contacts.ActivityTimeIntervals.md#starttime) | time | The starting time of the time interval within 'Date'. `Required` `Filter(ge;le)` 
| [State](General.Contacts.ActivityTimeIntervals.md#state) | [DocumentState](General.Contacts.ActivityTimeIntervals.md#state) __nullable__ | The state of the primary activity in the moment the time interval was created. null when the state is unknown. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Activity](General.Contacts.ActivityTimeIntervals.md#activity) | [Activities](General.Contacts.Activities.md) | The activity for which the time interval is recorded. `Required` `Filter(multi eq)` |
| [Party](General.Contacts.ActivityTimeIntervals.md#party) | [Parties](General.Contacts.Parties.md) | The party for which the time interval is recorded. `Required` `Filter(multi eq)` `Owner` |
| [UserStatus](General.Contacts.ActivityTimeIntervals.md#userstatus) | [DocumentTypeUserStatuses](General.DocumentTypeUserStatuses.md) (nullable) | The user status of the primary activity in the moment the time interval was created. null when the user status is unknown. `Filter(multi eq)` |


## Attribute Details

### Date

The date on which the work was performed. `Required` `Filter(eq;ge;le)`

_Type_: **date**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### EndTime

The ending time of the time interval within 'Date'. `Required` `Filter(ge;le)`

_Type_: **time**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### ExecutionCompletePercent

Percent of task completed. `Required` `Default(0)` `Filter(ge;le)`

_Type_: **decimal (3, 2)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Notes

Notes for the time interval.

_Type_: **string (254) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  

### StartTime

The starting time of the time interval within 'Date'. `Required` `Filter(ge;le)`

_Type_: **time**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### State

The state of the primary activity in the moment the time interval was created. null when the state is unknown.

_Type_: **[DocumentState](General.Contacts.ActivityTimeIntervals.md#state) __nullable__**  
Enumeration of document system states  
_Allowed Values (General.DocumentState Enum Members)_  

| Value | Description |
| ---- | --- |
| New | New document, just created. Can be edited. (Stored as 0). <br /> _Database Value:_ 0 <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'New' |
| Adjustment | Document which adjusts other released documents. (Stored as 5). <br /> _Database Value:_ 5 <br /> _Model Value:_ 5 <br /> _Domain API Value:_ 'Adjustment' |
| Planned | Planned by the system for future releasing. (Stored as 10). <br /> _Database Value:_ 10 <br /> _Model Value:_ 10 <br /> _Domain API Value:_ 'Planned' |
| FirmPlanned | Planned by operator for future releasing. (Stored as 20). <br /> _Database Value:_ 20 <br /> _Model Value:_ 20 <br /> _Domain API Value:_ 'FirmPlanned' |
| Released | Released document. Changes can be applied only through adjustment documents. (Stored as 30). <br /> _Database Value:_ 30 <br /> _Model Value:_ 30 <br /> _Domain API Value:_ 'Released' |
| Completed | Work has completed. (Stored as 40). <br /> _Database Value:_ 40 <br /> _Model Value:_ 40 <br /> _Domain API Value:_ 'Completed' |
| Closed | The document is audited and closed. Adjustments are not allowed, but reopening is allowed. (Stored as 50). <br /> _Database Value:_ 50 <br /> _Model Value:_ 50 <br /> _Domain API Value:_ 'Closed' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### Activity

The activity for which the time interval is recorded. `Required` `Filter(multi eq)`

_Type_: **[Activities](General.Contacts.Activities.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### Party

The party for which the time interval is recorded. `Required` `Filter(multi eq)` `Owner`

_Type_: **[Parties](General.Contacts.Parties.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  

### UserStatus

The user status of the primary activity in the moment the time interval was created. null when the user status is unknown. `Filter(multi eq)`

_Type_: **[DocumentTypeUserStatuses](General.DocumentTypeUserStatuses.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list limit=1000 erp.entity=General.Contacts.ActivityTimeIntervals erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=General.Contacts.ActivityTimeIntervals erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_Contacts_ActivityTimeIntervals?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_Contacts_ActivityTimeIntervals?$top=10>

