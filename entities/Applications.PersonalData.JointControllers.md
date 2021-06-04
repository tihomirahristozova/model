---
uid: Applications.PersonalData.JointControllers
---
# Applications.PersonalData.JointControllers Entity

**Namespace:** [Applications.PersonalData](Applications.PersonalData.md)  

Contains relationship between process and joint controllers. For processes with control role, these are the joint controllers. Otherwise, these are the joint controllers, on behalf of which the enterprise company processes the data. Entity: Pdm_Joint_Controllers (Introduced in version 18.2)

## Default Visualization
Default Display Text Format:  
_{PersonalDataProcess.Code}: {PersonalDataProcess.Name:T}_  
Default Search Member:  
_PersonalDataProcess.Code_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[Applications.PersonalData.PersonalDataProcesses](Applications.PersonalData.PersonalDataProcesses.md)  
Aggregate Root:  
[Applications.PersonalData.PersonalDataProcesses](Applications.PersonalData.PersonalDataProcesses.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Applications.PersonalData.JointControllers.md#id) | guid |  
| [Notes](Applications.PersonalData.JointControllers.md#notes) | string (max) __nullable__ | Should usually contain a short description of the role of the joint controller. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [JointControllerParty](Applications.PersonalData.JointControllers.md#jointcontrollerparty) | [Parties](General.Contacts.Parties.md) | The party, controlling the process. `Required` `Filter(multi eq)` |
| [PersonalDataProcess](Applications.PersonalData.JointControllers.md#personaldataprocess) | [PersonalDataProcesses](Applications.PersonalData.PersonalDataProcesses.md) | The process, which is managed jointly. `Required` `Filter(multi eq)` `Owner` |


## Attribute Details

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Notes

Should usually contain a short description of the role of the joint controller.

_Type_: **string (max) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  


## Reference Details

### JointControllerParty

The party, controlling the process. `Required` `Filter(multi eq)`

_Type_: **[Parties](General.Contacts.Parties.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### PersonalDataProcess

The process, which is managed jointly. `Required` `Filter(multi eq)` `Owner`

_Type_: **[PersonalDataProcesses](Applications.PersonalData.PersonalDataProcesses.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Can filter by attributes of referenced entity_: **True**  



## Business Rules

[!list erp.entity=Applications.PersonalData.JointControllers erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Applications.PersonalData.JointControllers erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_PersonalData_JointControllers?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_PersonalData_JointControllers?$top=10>

