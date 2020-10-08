---
uid: Applications.PersonalData.JointControllers
---
# Applications.PersonalData.JointControllers

Contains relationship between process and joint controllers. For processes with control role, these are the joint controllers. Otherwise, these are the joint controllers, on behalf of which the enterprise company processes the data. Entity: Pdm_Joint_Controllers (Introduced in version 18.2.100.0)

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Applications.PersonalData.JointControllers.md#Id) | guid |  
| [Notes](Applications.PersonalData.JointControllers.md#Notes) | string (nullable) | Should usually contain a short description of the role of the joint controller. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [JointControllerParty](Applications.PersonalData.JointControllers.md#JointControllerParty) | [General.Contacts.Parties](General.Contacts.Parties.md) | The party, controlling the process. [Required] [Filter(multi eq)] |
| [PersonalDataProcess](Applications.PersonalData.JointControllers.md#PersonalDataProcess) | [Applications.PersonalData.PersonalDataProcesses](Applications.PersonalData.PersonalDataProcesses.md) | The process, which is managed jointly. [Required] [Filter(multi eq)] [Owner] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### Notes

> Should usually contain a short description of the role of the joint controller.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### JointControllerParty

> The party, controlling the process. [Required] [Filter(multi eq)]

_Type_: **[General.Contacts.Parties](General.Contacts.Parties.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### PersonalDataProcess

> The process, which is managed jointly. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Applications.PersonalData.PersonalDataProcesses](Applications.PersonalData.PersonalDataProcesses.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Applications.PersonalData.JointControllers erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Applications.PersonalData.JointControllers erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Applications.PersonalData.JointControllers erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_PersonalData_JointControllers?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_PersonalData_JointControllers?$top=10>

