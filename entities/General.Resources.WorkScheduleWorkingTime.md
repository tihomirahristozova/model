---
uid: General.Resources.WorkScheduleWorkingTime
---
# General.Resources.WorkScheduleWorkingTime Entity

**Namespace:** [General.Resources](General.Resources.md)  

Contains the different working time periods within the work schedule. Entity: Gen_Work_Schedule_Working_Time

## Default Visualization
Default Display Text Format:  
_{WorkSchedule.Name:T}_  
Default Search Member:  
_WorkSchedule.Name_  

## Aggregate
  @aggregates  
Aggregate Parent:  
[General.Resources.WorkSchedules](General.Resources.WorkSchedules.md)  
Aggregate Root:  
[General.Resources.WorkSchedules](General.Resources.WorkSchedules.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [DayNo](General.Resources.WorkScheduleWorkingTime.md#dayno) | int32 | Consequtive day in the work schedule recurrence, starting at 1. [Required] 
| [EndTime](General.Resources.WorkScheduleWorkingTime.md#endtime) | time | End of working time period. [Required] 
| [Id](General.Resources.WorkScheduleWorkingTime.md#id) | guid |  
| [StartTime](General.Resources.WorkScheduleWorkingTime.md#starttime) | time | Start of working time period on the day, specified by Day_No. [Required] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [WorkSchedule](General.Resources.WorkScheduleWorkingTime.md#workschedule) | [WorkSchedules](General.Resources.WorkSchedules.md) | The [WorkSchedule](General.Resources.WorkScheduleWorkingTime.md#workschedule) to which this WorkScheduleWorkingTime belongs. [Required] [Filter(multi eq)] [Owner] |


## Attribute Details

### DayNo

Consequtive day in the work schedule recurrence, starting at 1. [Required]

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### EndTime

End of working time period. [Required]

_Type_: **time**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### StartTime

Start of working time period on the day, specified by Day_No. [Required]

_Type_: **time**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### WorkSchedule

The [WorkSchedule](General.Resources.WorkScheduleWorkingTime.md#workschedule) to which this WorkScheduleWorkingTime belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[WorkSchedules](General.Resources.WorkSchedules.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=General.Resources.WorkScheduleWorkingTime erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.Resources.WorkScheduleWorkingTime erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_Resources_WorkScheduleWorkingTime?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_Resources_WorkScheduleWorkingTime?$top=10>

