---
uid: Projects.Projects
---
# Projects.Projects

Contains the planned, running and completed projects of the enterprises. Entity: Prj_Projects

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Projects.Projects.md#Id) | guid |  
| [FinishDate](Projects.Projects.md#FinishDate) | date (nullable) | The drop dead date of the project, e.g. the date when the project should be finished. null means that the finish date is unknown. [Filter(eq)] 
| [Notes](Projects.Projects.md#Notes) | string (nullable) | Notes for this Project. 
| [Code](Projects.Projects.md#Code) | string | Short code for identification of projects. [Required] [Filter(eq;like)] [ORD] 
| [Name](Projects.Projects.md#Name) | string | The name of this Project. [Required] [Filter(eq;like)] 
| [ProjectStatus](Projects.Projects.md#ProjectStatus) | [Projects.ProjectsRepository.ProjectStatus](Projects.Projects.md#ProjectStatus) | Current project status. 0=New/Structuring, 10=Budgeting, 20=Panning, 30=Started, 40=Resolved(Completed), 45=Resolved(Cancelled), 50=Closed(Completed), 55=Closed(Cancelled). [Required] [Default(0)] [Filter(multi eq)] 
| [StartDate](Projects.Projects.md#StartDate) | date (nullable) | Expected date, when the execution of the tasks will start. null means that the start date is still unknown. [Filter(eq)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [BudgetingCurrency](Projects.Projects.md#BudgetingCurrency) | [General.Currencies](General.Currencies.md) (nullable) | The currency in which the project budget is calculated. [Filter(multi eq)] |
| [ClientParty](Projects.Projects.md#ClientParty) | [General.Contacts.Parties](General.Contacts.Parties.md) (nullable) | The external or internal client of the project. [Filter(multi eq)] |
| [EnterpriseCompany](Projects.Projects.md#EnterpriseCompany) | [General.EnterpriseCompanies](General.EnterpriseCompanies.md) (nullable) | The Enterprise Company to which this Project applies, or null if it is for all enterprise companies. [Filter(multi eq)] |
| [ProjectManagerPerson](Projects.Projects.md#ProjectManagerPerson) | [General.Contacts.Persons](General.Contacts.Persons.md) (nullable) | The project manager. [Filter(multi eq)] |
| [ProjectType](Projects.Projects.md#ProjectType) | [Projects.ProjectTypes](Projects.ProjectTypes.md) | The project type defines the basic WBS and default tasks, etc. It is also used as baseline WBS, when combining reports for many projects. [Required] [Filter(multi eq)] |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Participants | [Projects.ProjectParticipants](Projects.ProjectParticipants.md) | List of [ProjectParticipant](Projects.ProjectParticipants.md) child objects, based on the [Projects.ProjectParticipant.Project](Projects.ProjectParticipants.md#Project) back reference 
| Risks | [Projects.ProjectRisks](Projects.ProjectRisks.md) | List of [ProjectRisk](Projects.ProjectRisks.md) child objects, based on the [Projects.ProjectRisk.Project](Projects.ProjectRisks.md#Project) back reference 
| WorkElements | [Projects.ProjectWorkElements](Projects.ProjectWorkElements.md) | List of [ProjectWorkElement](Projects.ProjectWorkElements.md) child objects, based on the [Projects.ProjectWorkElement.Project](Projects.ProjectWorkElements.md#Project) back reference 


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### FinishDate

> The drop dead date of the project, e.g. the date when the project should be finished. null means that the finish date is unknown. [Filter(eq)]

_Type_: **date (nullable)**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

### Notes

> Notes for this Project.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Code

> Short code for identification of projects. [Required] [Filter(eq;like)] [ORD]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  

### Name

> The name of this Project. [Required] [Filter(eq;like)]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### ProjectStatus

> Current project status. 0=New/Structuring, 10=Budgeting, 20=Panning, 30=Started, 40=Resolved(Completed), 45=Resolved(Cancelled), 50=Closed(Completed), 55=Closed(Cancelled). [Required] [Default(0)] [Filter(multi eq)]

_Type_: **[Projects.ProjectsRepository.ProjectStatus](Projects.Projects.md#ProjectStatus)**  
Allowed values for the [ProjectStatus](Projects.Projects.md#ProjectStatus) data attribute  
_Allowed Values (Enum Members)_  

| Value | Description |
| ---- | --- |
| NewOrStructuring | NewOrStructuring value. Stored as 0. <br /> _Database Value:_ 0 <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'NewOrStructuring' |
| Budgeting | Budgeting value. Stored as 10. <br /> _Database Value:_ 10 <br /> _Model Value:_ 10 <br /> _Domain API Value:_ 'Budgeting' |
| Planning | Planning value. Stored as 20. <br /> _Database Value:_ 20 <br /> _Model Value:_ 20 <br /> _Domain API Value:_ 'Planning' |
| Started | Started value. Stored as 30. <br /> _Database Value:_ 30 <br /> _Model Value:_ 30 <br /> _Domain API Value:_ 'Started' |
| ResolvedCompleted | ResolvedCompleted value. Stored as 40. <br /> _Database Value:_ 40 <br /> _Model Value:_ 40 <br /> _Domain API Value:_ 'ResolvedCompleted' |
| ResolvedCancelled | ResolvedCancelled value. Stored as 45. <br /> _Database Value:_ 45 <br /> _Model Value:_ 45 <br /> _Domain API Value:_ 'ResolvedCancelled' |
| ClosedCompleted | ClosedCompleted value. Stored as 50. <br /> _Database Value:_ 50 <br /> _Model Value:_ 50 <br /> _Domain API Value:_ 'ClosedCompleted' |
| ClosedCanceled | ClosedCanceled value. Stored as 55. <br /> _Database Value:_ 55 <br /> _Model Value:_ 55 <br /> _Domain API Value:_ 'ClosedCanceled' |

_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### StartDate

> Expected date, when the execution of the tasks will start. null means that the start date is still unknown. [Filter(eq)]

_Type_: **date (nullable)**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  


## Reference Details

### BudgetingCurrency

> The currency in which the project budget is calculated. [Filter(multi eq)]

_Type_: **[General.Currencies](General.Currencies.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### ClientParty

> The external or internal client of the project. [Filter(multi eq)]

_Type_: **[General.Contacts.Parties](General.Contacts.Parties.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### EnterpriseCompany

> The Enterprise Company to which this Project applies, or null if it is for all enterprise companies. [Filter(multi eq)]

_Type_: **[General.EnterpriseCompanies](General.EnterpriseCompanies.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### ProjectManagerPerson

> The project manager. [Filter(multi eq)]

_Type_: **[General.Contacts.Persons](General.Contacts.Persons.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### ProjectType

> The project type defines the basic WBS and default tasks, etc. It is also used as baseline WBS, when combining reports for many projects. [Required] [Filter(multi eq)]

_Type_: **[Projects.ProjectTypes](Projects.ProjectTypes.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Projects.Projects erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Projects.Projects erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Projects.Projects erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Projects_Projects?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Projects_Projects?$top=10>

