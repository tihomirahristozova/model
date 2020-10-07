# General.Resources.WorkScheduleWorkingTime

Contains the different working time periods within the work schedule. Entity: Gen_Work_Schedule_Working_Time

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](General.Resources.WorkScheduleWorkingTime.md#Id) | guid |  
| [DayNo](General.Resources.WorkScheduleWorkingTime.md#DayNo) | int32 | Consequtive day in the work schedule recurrence, starting at 1. [Required] 
| [EndTime](General.Resources.WorkScheduleWorkingTime.md#EndTime) | time | End of working time period. [Required] 
| [StartTime](General.Resources.WorkScheduleWorkingTime.md#StartTime) | time | Start of working time period on the day, specified by Day_No. [Required] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [WorkSchedule](General.Resources.WorkScheduleWorkingTime.md#WorkSchedule) | [General.Resources.WorkSchedules](General.Resources.WorkSchedules.md) | The [WorkSchedule](General.Resources.WorkScheduleWorkingTime.md#WorkSchedule) to which this WorkScheduleWorkingTime belongs. [Required] [Filter(multi eq)] [Owner] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### DayNo

> Consequtive day in the work schedule recurrence, starting at 1. [Required]

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### EndTime

> End of working time period. [Required]

_Type_: **time**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### StartTime

> Start of working time period on the day, specified by Day_No. [Required]

_Type_: **time**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### WorkSchedule

> The [WorkSchedule](General.Resources.WorkScheduleWorkingTime.md#WorkSchedule) to which this WorkScheduleWorkingTime belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[General.Resources.WorkSchedules](General.Resources.WorkSchedules.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=General.Resources.WorkScheduleWorkingTime erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.Resources.WorkScheduleWorkingTime erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=General.Resources.WorkScheduleWorkingTime erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_Resources_WorkScheduleWorkingTime?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_Resources_WorkScheduleWorkingTime?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Gen_Work_Schedule_Working_Time?$top=10>

