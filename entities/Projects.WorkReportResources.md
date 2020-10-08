---
uid: Projects.WorkReportResources
---
# Projects.WorkReportResources

Each record contains usage of resource, reported by the related Work Report. Entity: Prj_Work_Report_Resources

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Projects.WorkReportResources.md#Id) | guid |  
| [ActualEndTime](Projects.WorkReportResources.md#ActualEndTime) | datetime (nullable) | Optionally, specifies the actual date and time when the resource usage ended. [Filter(eq;like)] 
| [ActualStartTime](Projects.WorkReportResources.md#ActualStartTime) | datetime (nullable) | Optionally, specifies the actual date and time when the resource usage began. [Filter(eq;like)] 
| [TotalResourceUsageHours](Projects.WorkReportResources.md#TotalResourceUsageHours) | decimal | The total number of resource-hours, which are actually consumed. Equals to the duration of the task, multiplied by the average resource usage. [Required] [Default(0)] [Filter(eq;like)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [ProjectTask](Projects.WorkReportResources.md#ProjectTask) | [Projects.ProjectTasks](Projects.ProjectTasks.md) | The project task for which the work is reported. [Required] [Filter(multi eq)] |
| [Resource](Projects.WorkReportResources.md#Resource) | [General.Resources.Resources](General.Resources.Resources.md) | The resource, for which usage is reported. [Required] [Filter(multi eq)] |
| [ResourceInstance](Projects.WorkReportResources.md#ResourceInstance) | [General.Resources.ResourceInstances](General.Resources.ResourceInstances.md) (nullable) | The concrete resource instance used. null when no concrete resource was used or there is no data whether concrete resource was used. [Filter(multi eq;like)] |
| [WorkReport](Projects.WorkReportResources.md#WorkReport) | [Projects.WorkReports](Projects.WorkReports.md) | The [WorkReport](Projects.WorkReportResources.md#WorkReport) to which this WorkReportResource belongs. [Required] [Filter(multi eq)] [Owner] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### ActualEndTime

> Optionally, specifies the actual date and time when the resource usage ended. [Filter(eq;like)]

_Type_: **datetime (nullable)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### ActualStartTime

> Optionally, specifies the actual date and time when the resource usage began. [Filter(eq;like)]

_Type_: **datetime (nullable)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### TotalResourceUsageHours

> The total number of resource-hours, which are actually consumed. Equals to the duration of the task, multiplied by the average resource usage. [Required] [Default(0)] [Filter(eq;like)]

_Type_: **decimal**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  
_Default Value_: **0**  


## Reference Details

### ProjectTask

> The project task for which the work is reported. [Required] [Filter(multi eq)]

_Type_: **[Projects.ProjectTasks](Projects.ProjectTasks.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`obj.WorkReport.ProjectTask`

_Front-End Recalc Expressions:_  
`obj.WorkReport.ProjectTask`
### Resource

> The resource, for which usage is reported. [Required] [Filter(multi eq)]

_Type_: **[General.Resources.Resources](General.Resources.Resources.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### ResourceInstance

> The concrete resource instance used. null when no concrete resource was used or there is no data whether concrete resource was used. [Filter(multi eq;like)]

_Type_: **[General.Resources.ResourceInstances](General.Resources.ResourceInstances.md) (nullable)**  
_Supported Filters_: **Equals, Like, EqualsIn**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`IIF(((obj.ResourceInstance != null) AndAlso (obj.ResourceInstance.Resource != obj.Resource)), null, obj.ResourceInstance)`
### WorkReport

> The [WorkReport](Projects.WorkReportResources.md#WorkReport) to which this WorkReportResource belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Projects.WorkReports](Projects.WorkReports.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Projects.WorkReportResources erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Projects.WorkReportResources erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Projects.WorkReportResources erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Projects_WorkReportResources?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Projects_WorkReportResources?$top=10>

