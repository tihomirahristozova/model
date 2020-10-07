# Systems.Bpm.ProcessLanes

The process lanes categorize elements in the process and contain logic for executor selection. Entity: Bpm_Process_Lanes

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Systems.Bpm.ProcessLanes.md#Id) | guid |  
| [AssignByUserCondition](Systems.Bpm.ProcessLanes.md#AssignByUserCondition) | [Systems.Bpm.ProcessLanesRepository.AssignByUserCondition](Systems.Bpm.ProcessLanes.md#AssignByUserCondition) | Specifies direct assign action, based on User Condition. N=No direct assignment, only offer to users; R=Assign to random user; L=User with least tasks assigned. [Required] [Filter(eq;like)] 
| [IsSystemExecuted](Systems.Bpm.ProcessLanes.md#IsSystemExecuted) | boolean | When set, specifies that the lane allows only system executed tasks and will never have human user as executor. [Required] [Default(false)] [Filter(eq)] 
| [Locality](Systems.Bpm.ProcessLanes.md#Locality) | [Systems.Bpm.Locality](Systems.Bpm.ProcessLanes.md#Locality) | Process execution locality. Represents where the execution takes place and influences the selection of possible executors. For example, when L, the execution is private to the location, where the process originated. P=Same as parent; L=Location; C=Company; I=Intra-company. [Required] [Filter(eq;like)] 
| [Notes](Systems.Bpm.ProcessLanes.md#Notes) | string (nullable) | Notes for this ProcessLane. 
| [Name](Systems.Bpm.ProcessLanes.md#Name) | [MultilanguageString](../data-types/MultilanguageString.md) | Multilanguage lane name. [Required] [Filter(eq;like)] 
| [RestrictToSingleUser](Systems.Bpm.ProcessLanes.md#RestrictToSingleUser) | boolean | Specifies whether the lane would be restricted to the first user, who is assigned an activity in the lane. Subsequent tasks are directly assigned to that user. [Required] [Default(false)] [Filter(eq)] 
| [UserConditionFilterXml](Systems.Bpm.ProcessLanes.md#UserConditionFilterXml) | dataaccessfilter (nullable) | User defined filter, used to select possible executors of tasks in the lane. [Filter(eq;like)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [AssignByInstanceProperty](Systems.Bpm.ProcessLanes.md#AssignByInstanceProperty) | [General.CustomProperties](General.CustomProperties.md) (nullable) | When set, the user, specified in the instance property will be assigned the task. Mutually exclusive with Assign To User. [Filter(multi eq)] |
| [AssignToUser](Systems.Bpm.ProcessLanes.md#AssignToUser) | [Systems.Security.Users](Systems.Security.Users.md) (nullable) | When set, specifies that tasks from the lane are always assigned to specific user. [Filter(multi eq)] |
| [OfferToRole](Systems.Bpm.ProcessLanes.md#OfferToRole) | [Systems.Workflow.Roles](Systems.Workflow.Roles.md) (nullable) | When set, the tasks from the lane are offered for assignment to the users with the specified role and the same locality as the process instance. [Filter(multi eq)] |
| [Process](Systems.Bpm.ProcessLanes.md#Process) | [Systems.Bpm.Processes](Systems.Bpm.Processes.md) | The process to which this lane belongs. [Required] [Filter(multi eq)] [Owner] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### AssignByUserCondition

> Specifies direct assign action, based on User Condition. N=No direct assignment, only offer to users; R=Assign to random user; L=User with least tasks assigned. [Required] [Filter(eq;like)]

_Type_: **[Systems.Bpm.ProcessLanesRepository.AssignByUserCondition](Systems.Bpm.ProcessLanes.md#AssignByUserCondition)**  
Allowed values for the [AssignByUserCondition](Systems.Bpm.ProcessLanes.md#AssignByUserCondition) data attribute  
_Allowed Values (Enum Members)_  

| Value | Description |
| ---- | --- |
| NoDirectAssignment | NoDirectAssignment value. Stored as 'N'. <br /> _Database Value:_ 'N' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'NoDirectAssignment' |
| AssignToRandomUser | AssignToRandomUser value. Stored as 'R'. <br /> _Database Value:_ 'R' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'AssignToRandomUser' |
| UserWithLeastTasksAssigned | UserWithLeastTasksAssigned value. Stored as 'L'. <br /> _Database Value:_ 'L' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'UserWithLeastTasksAssigned' |

_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### IsSystemExecuted

> When set, specifies that the lane allows only system executed tasks and will never have human user as executor. [Required] [Default(false)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### Locality

> Process execution locality. Represents where the execution takes place and influences the selection of possible executors. For example, when L, the execution is private to the location, where the process originated. P=Same as parent; L=Location; C=Company; I=Intra-company. [Required] [Filter(eq;like)]

_Type_: **[Systems.Bpm.Locality](Systems.Bpm.ProcessLanes.md#Locality)**  
Generic enum type for Locality properties  
_Allowed Values (Enum Members)_  

| Value | Description |
| ---- | --- |
| Parent | Parent value. Stored as 'P'. <br /> _Database Value:_ 'P' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Parent' |
| Location | Location value. Stored as 'L'. <br /> _Database Value:_ 'L' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'Location' |
| Company | Company value. Stored as 'C'. <br /> _Database Value:_ 'C' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'Company' |
| IntraCompany | IntraCompany value. Stored as 'I'. <br /> _Database Value:_ 'I' <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'IntraCompany' |

_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### Notes

> Notes for this ProcessLane.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Name

> Multilanguage lane name. [Required] [Filter(eq;like)]

_Type_: **[MultilanguageString](../data-types/MultilanguageString.md)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### RestrictToSingleUser

> Specifies whether the lane would be restricted to the first user, who is assigned an activity in the lane. Subsequent tasks are directly assigned to that user. [Required] [Default(false)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### UserConditionFilterXml

> User defined filter, used to select possible executors of tasks in the lane. [Filter(eq;like)]

_Type_: **dataaccessfilter (nullable)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  


## Reference Details

### AssignByInstanceProperty

> When set, the user, specified in the instance property will be assigned the task. Mutually exclusive with Assign To User. [Filter(multi eq)]

_Type_: **[General.CustomProperties](General.CustomProperties.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### AssignToUser

> When set, specifies that tasks from the lane are always assigned to specific user. [Filter(multi eq)]

_Type_: **[Systems.Security.Users](Systems.Security.Users.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### OfferToRole

> When set, the tasks from the lane are offered for assignment to the users with the specified role and the same locality as the process instance. [Filter(multi eq)]

_Type_: **[Systems.Workflow.Roles](Systems.Workflow.Roles.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Process

> The process to which this lane belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Systems.Bpm.Processes](Systems.Bpm.Processes.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Systems.Bpm.ProcessLanes erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Systems.Bpm.ProcessLanes erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Systems.Bpm.ProcessLanes erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Systems_Bpm_ProcessLanes?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Systems_Bpm_ProcessLanes?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Bpm_Process_Lanes?$top=10>

