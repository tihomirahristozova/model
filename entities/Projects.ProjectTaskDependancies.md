# Projects.ProjectTaskDependancies

Represents dependancy between project tasks. Entity: Prj_Project_Task_Dependancies

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Projects.ProjectTaskDependancies.md#Id) | guid |  
| [DependancyType](Projects.ProjectTaskDependancies.md#DependancyType) | [Projects.ProjectTaskDependanciesRepository.DependancyType](Projects.ProjectTaskDependancies.md#DependancyType) | FS=Finish-to-Start;SS=Start-to-Start;FF=Finish-to-Finish;SF=Start-to-Finish;SY=Sync (all types in the same time). [Required] [Default("FS")] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [DependsOnTask](Projects.ProjectTaskDependancies.md#DependsOnTask) | [Projects.ProjectTasks](Projects.ProjectTasks.md) | The task on which Project_Task depends. [Required] [Filter(multi eq)] |
| [ProjectTask](Projects.ProjectTaskDependancies.md#ProjectTask) | [Projects.ProjectTasks](Projects.ProjectTasks.md) | The task which depends on another task. [Required] [Filter(multi eq)] [Owner] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### DependancyType

> FS=Finish-to-Start;SS=Start-to-Start;FF=Finish-to-Finish;SF=Start-to-Finish;SY=Sync (all types in the same time). [Required] [Default("FS")]

_Type_: **[Projects.ProjectTaskDependanciesRepository.DependancyType](Projects.ProjectTaskDependancies.md#DependancyType)**  
Allowed values for the [DependancyType](Projects.ProjectTaskDependancies.md#DependancyType) data attribute  
_Allowed Values (Enum Members)_  

| Value | Description |
| ---- | --- |
| FinishToStart | FinishToStart value. Stored as 'FS'. <br /> _Database Value:_ 'FS' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'FinishToStart' |
| StartToStart | StartToStart value. Stored as 'SS'. <br /> _Database Value:_ 'SS' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'StartToStart' |
| FinishToFinish | FinishToFinish value. Stored as 'FF'. <br /> _Database Value:_ 'FF' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'FinishToFinish' |
| StartToFinish | StartToFinish value. Stored as 'SF'. <br /> _Database Value:_ 'SF' <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'StartToFinish' |
| SyncAllTypesInTheSameTime | SyncAllTypesInTheSameTime value. Stored as 'SY'. <br /> _Database Value:_ 'SY' <br /> _Model Value:_ 4 <br /> _Domain API Value:_ 'SyncAllTypesInTheSameTime' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **FinishToStart**  


## Reference Details

### DependsOnTask

> The task on which Project_Task depends. [Required] [Filter(multi eq)]

_Type_: **[Projects.ProjectTasks](Projects.ProjectTasks.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### ProjectTask

> The task which depends on another task. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Projects.ProjectTasks](Projects.ProjectTasks.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Projects.ProjectTaskDependancies erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Projects.ProjectTaskDependancies erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Projects.ProjectTaskDependancies erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Projects_ProjectTaskDependancies?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Projects_ProjectTaskDependancies?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Prj_Project_Task_Dependancies?$top=10>

