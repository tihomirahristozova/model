# Projects.ProjectTasks

Represents one task of a project. Entity: Prj_Project_Tasks

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Projects.ProjectTasks.md#Id) | guid |  
| [BudgetLaborAmount](Projects.ProjectTasks.md#BudgetLaborAmount) | [Amount](../data-types/Amount.md) (nullable) | Budgeted amount for the labor for the task in the currency of the project. The material is calculated separately. null means that budgeting for the item is not calculated. [Currency: Project.BudgetingCurrency] 
| [FinishDateTime](Projects.ProjectTasks.md#FinishDateTime) | datetime | The date and time when the task is planned to finish. [Required] [Default(Now)] [Filter(eq;ge;le)] 
| [Notes](Projects.ProjectTasks.md#Notes) | string (nullable) | Notes for this ProjectTask. 
| [PlannedDurationHours](Projects.ProjectTasks.md#PlannedDurationHours) | decimal | Planned duration of the task in hours. The hours are allocated in the time interval between Start Date Time and Finish Date Time. [Required] [Default(0)] 
| [ProjectTaskNo](Projects.ProjectTasks.md#ProjectTaskNo) | int32 | Consecutive task number, unique within the project. [Required] 
| [StartDateTime](Projects.ProjectTasks.md#StartDateTime) | datetime | The date and time when the task is planned to start. [Required] [Default(Now)] [Filter(eq;ge;le)] 
| [TaskName](Projects.ProjectTasks.md#TaskName) | string | The short name of the task. It is best practice to contain the target of the task. [Required] [Filter(multi eq;like)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Activity](Projects.ProjectTasks.md#Activity) | [General.Contacts.Activities](General.Contacts.Activities.md) (nullable) | The Id of the Cm_Activity created for this task. null means that activity is still not created. [Filter(multi eq)] |
| [Project](Projects.ProjectTasks.md#Project) | [Projects.Projects](Projects.Projects.md) | The project, to which this task belongs. [Required] [Filter(multi eq)] |
| [ProjectWorkElement](Projects.ProjectTasks.md#ProjectWorkElement) | [Projects.ProjectWorkElements](Projects.ProjectWorkElements.md) | The work element under which the task is filed. [Required] [Filter(multi eq)] |
| [Resource](Projects.ProjectTasks.md#Resource) | [Projects.Resources](Projects.Resources.md) (nullable) | The resource, which is required for the task. null means - do not plan any resource. [Filter(multi eq)] |
| [ResponsibleParty](Projects.ProjectTasks.md#ResponsibleParty) | [General.Contacts.Parties](General.Contacts.Parties.md) (nullable) | The responsible party. Usually a person and usually one of the project participants. null means that responsible is not yet determined. [Filter(multi eq)] |
| [TaskType](Projects.ProjectTasks.md#TaskType) | [Projects.TaskTypes](Projects.TaskTypes.md) | The type of the task. Determines the work type of the tasks, default billing rules, etc. [Required] [Filter(multi eq)] |
| [WorkType](Projects.ProjectTasks.md#WorkType) | [Projects.TypeWorkTypes](Projects.TypeWorkTypes.md) (nullable) | Type of work to be done. null means that type of work is undetermined yet. [Filter(multi eq)] |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Dependancies | [Projects.ProjectTaskDependancies](Projects.ProjectTaskDependancies.md) | List of [ProjectTaskDependancy](Projects.ProjectTaskDependancies.md) child objects, based on the [Projects.ProjectTaskDependancy.ProjectTask](Projects.ProjectTaskDependancies.md#ProjectTask) back reference 
| Materials | [Projects.ProjectTaskMaterials](Projects.ProjectTaskMaterials.md) | List of [ProjectTaskMaterial](Projects.ProjectTaskMaterials.md) child objects, based on the [Projects.ProjectTaskMaterial.ProjectTask](Projects.ProjectTaskMaterials.md#ProjectTask) back reference 
| Participants | [Projects.ProjectTaskParticipants](Projects.ProjectTaskParticipants.md) | List of [ProjectTaskParticipant](Projects.ProjectTaskParticipants.md) child objects, based on the [Projects.ProjectTaskParticipant.ProjectTask](Projects.ProjectTaskParticipants.md#ProjectTask) back reference 
| Resources | [Projects.ProjectTaskResources](Projects.ProjectTaskResources.md) | List of [ProjectTaskResource](Projects.ProjectTaskResources.md) child objects, based on the [Projects.ProjectTaskResource.ProjectTask](Projects.ProjectTaskResources.md#ProjectTask) back reference 


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### BudgetLaborAmount

> Budgeted amount for the labor for the task in the currency of the project. The material is calculated separately. null means that budgeting for the item is not calculated. [Currency: Project.BudgetingCurrency]

_Type_: **[Amount](../data-types/Amount.md) (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`IIF(((obj.PlannedDurationHours != 0) AndAlso (obj.WorkType != null)), obj.CalculateBudgetLaborAmount(), new Amount(0, obj.Project.BudgetingCurrency))`
### FinishDateTime

> The date and time when the task is planned to finish. [Required] [Default(Now)] [Filter(eq;ge;le)]

_Type_: **datetime**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **CurrentDateTime**  

### Notes

> Notes for this ProjectTask.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### PlannedDurationHours

> Planned duration of the task in hours. The hours are allocated in the time interval between Start Date Time and Finish Date Time. [Required] [Default(0)]

_Type_: **decimal**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### ProjectTaskNo

> Consecutive task number, unique within the project. [Required]

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### StartDateTime

> The date and time when the task is planned to start. [Required] [Default(Now)] [Filter(eq;ge;le)]

_Type_: **datetime**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **CurrentDateTime**  

### TaskName

> The short name of the task. It is best practice to contain the target of the task. [Required] [Filter(multi eq;like)]

_Type_: **string**  
_Supported Filters_: **Equals, Like, EqualsIn**  
_Supports Order By_: **False**  


## Reference Details

### Activity

> The Id of the Cm_Activity created for this task. null means that activity is still not created. [Filter(multi eq)]

_Type_: **[General.Contacts.Activities](General.Contacts.Activities.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Project

> The project, to which this task belongs. [Required] [Filter(multi eq)]

_Type_: **[Projects.Projects](Projects.Projects.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### ProjectWorkElement

> The work element under which the task is filed. [Required] [Filter(multi eq)]

_Type_: **[Projects.ProjectWorkElements](Projects.ProjectWorkElements.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Resource

> The resource, which is required for the task. null means - do not plan any resource. [Filter(multi eq)]

_Type_: **[Projects.Resources](Projects.Resources.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### ResponsibleParty

> The responsible party. Usually a person and usually one of the project participants. null means that responsible is not yet determined. [Filter(multi eq)]

_Type_: **[General.Contacts.Parties](General.Contacts.Parties.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### TaskType

> The type of the task. Determines the work type of the tasks, default billing rules, etc. [Required] [Filter(multi eq)]

_Type_: **[Projects.TaskTypes](Projects.TaskTypes.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### WorkType

> Type of work to be done. null means that type of work is undetermined yet. [Filter(multi eq)]

_Type_: **[Projects.TypeWorkTypes](Projects.TypeWorkTypes.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Projects.ProjectTasks erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Projects.ProjectTasks erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Projects.ProjectTasks erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Projects_ProjectTasks?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Projects_ProjectTasks?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Prj_Project_Tasks?$top=10>

