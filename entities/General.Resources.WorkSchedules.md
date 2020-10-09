---
uid: General.Resources.WorkSchedules
---
# General.Resources.WorkSchedules Entity

Represents the different working schedules, used by the employees and resources. Entity: Gen_Work_Schedules

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](General.Resources.WorkSchedules.md#id) | guid |  
| [Name](General.Resources.WorkSchedules.md#name) | string | The name of this WorkSchedule. [Required] [Filter(like)] 
| [NumberOfDays](General.Resources.WorkSchedules.md#numberofdays) | int16 (nullable) | Number of days in a recurring period. Valid only when Recurrence_Type=D. 
| [RecurrenceType](General.Resources.WorkSchedules.md#recurrencetype) | [RecurrenceType](General.Resources.WorkSchedules.md#recurrencetype) | D=recurring each X days; W=recurring each week; M=recurring each month. [Required] [Filter(multi eq)] 

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| WorkingTime | [WorkScheduleWorkingTime](General.Resources.WorkScheduleWorkingTime.md) | List of [WorkScheduleWorkingTime](General.Resources.WorkScheduleWorkingTime.md) child objects, based on the [General.Resources.WorkScheduleWorkingTime.WorkSchedule](General.Resources.WorkScheduleWorkingTime.md#workschedule) back reference 


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

> The name of this WorkSchedule. [Required] [Filter(like)]

_Type_: **string**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### NumberOfDays

> Number of days in a recurring period. Valid only when Recurrence_Type=D.

_Type_: **int16 (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### RecurrenceType

> D=recurring each X days; W=recurring each week; M=recurring each month. [Required] [Filter(multi eq)]

_Type_: **[RecurrenceType](General.Resources.WorkSchedules.md#recurrencetype)**  
Allowed values for the [RecurrenceType](General.Resources.WorkSchedules.md#recurrencetype) data attribute  
_Allowed Values (General.Resources.WorkSchedulesRepository.RecurrenceType Enum Members)_  

| Value | Description |
| ---- | --- |
| RecurringEachXDays | RecurringEachXDays value. Stored as 'D'. <br /> _Database Value:_ 'D' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'RecurringEachXDays' |
| RecurringEachMonth | RecurringEachMonth value. Stored as 'M'. <br /> _Database Value:_ 'M' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'RecurringEachMonth' |
| RecurringEachWeek | RecurringEachWeek value. Stored as 'W'. <br /> _Database Value:_ 'W' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'RecurringEachWeek' |

_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=General.Resources.WorkSchedules erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.Resources.WorkSchedules erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=General.Resources.WorkSchedules erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_Resources_WorkSchedules?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_Resources_WorkSchedules?$top=10>

