---
uid: Applications.Fleet.CrewMembers
---
# Applications.Fleet.CrewMembers Entity

**Namespace:** [Applications.Fleet](Applications.Fleet.md)  

Contains the memnbers of vehicle crews. Entity: Fleet_Crew_Members

## Default Visualization
Default Display Text Format:  
_{Crew.Name:T}_  
Default Search Member:  
_Crew.Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[Applications.Fleet.Crews](Applications.Fleet.Crews.md)  
Aggregate Root:  
[General.EnterpriseCompanies](General.EnterpriseCompanies.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Applications.Fleet.CrewMembers.md#id) | guid |  
| [Notes](Applications.Fleet.CrewMembers.md#notes) | string (nullable) | Notes for this CrewMember. 
| [OrdinalPos](Applications.Fleet.CrewMembers.md#ordinalpos) | int32 (nullable) | Ordinal position. Ordinal_Pos=0 has special meaning - this is the crew leader. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Crew](Applications.Fleet.CrewMembers.md#crew) | [Crews](Applications.Fleet.Crews.md) | The crew to which this member belongs. [Required] [Filter(multi eq)] [Owner] |
| [Person](Applications.Fleet.CrewMembers.md#person) | [Persons](General.Contacts.Persons.md) | The crew member person. [Required] [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Notes

Notes for this CrewMember.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### OrdinalPos

Ordinal position. Ordinal_Pos=0 has special meaning - this is the crew leader.

_Type_: **int32 (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### Crew

The crew to which this member belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Crews](Applications.Fleet.Crews.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### Person

The crew member person. [Required] [Filter(multi eq)]

_Type_: **[Persons](General.Contacts.Persons.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Applications.Fleet.CrewMembers erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Applications.Fleet.CrewMembers erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_Fleet_CrewMembers?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_Fleet_CrewMembers?$top=10>

