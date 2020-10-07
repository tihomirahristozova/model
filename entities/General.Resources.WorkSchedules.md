# General.Resources.WorkSchedules

Represents the different working schedules, used by the employees and resources. Entity: Gen_Work_Schedules

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](General.Resources.WorkSchedules.md#Id) | guid |  
| [NumberOfDays](General.Resources.WorkSchedules.md#NumberOfDays) | int16 (nullable) | Number of days in a recurring period. Valid only when Recurrence_Type=D. 
| [RecurrenceType](General.Resources.WorkSchedules.md#RecurrenceType) | [General.Resources.WorkSchedulesRepository.RecurrenceType](General.Resources.WorkSchedules.md#RecurrenceType) | D=recurring each X days; W=recurring each week; M=recurring each month. [Required] [Filter(multi eq)] 
| [Name](General.Resources.WorkSchedules.md#Name) | string | The name of this WorkSchedule. [Required] [Filter(like)] 

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| WorkingTime | [General.Resources.WorkScheduleWorkingTime](General.Resources.WorkScheduleWorkingTime.md) | List of [WorkScheduleWorkingTime](General.Resources.WorkScheduleWorkingTime.md) child objects, based on the [General.Resources.WorkScheduleWorkingTime.WorkSchedule](General.Resources.WorkScheduleWorkingTime.md#WorkSchedule) back reference 


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### NumberOfDays

> Number of days in a recurring period. Valid only when Recurrence_Type=D.

_Type_: **int16 (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### RecurrenceType

> D=recurring each X days; W=recurring each week; M=recurring each month. [Required] [Filter(multi eq)]

_Type_: **[General.Resources.WorkSchedulesRepository.RecurrenceType](General.Resources.WorkSchedules.md#RecurrenceType)**  
Allowed values for the [RecurrenceType](General.Resources.WorkSchedules.md#RecurrenceType) data attribute  
_Allowed Values (Enum Members)_  

| Value | Description |
| ---- | --- |
| RecurringEachXDays | RecurringEachXDays value. Stored as 'D'. <br /> _Database Value:_ 'D' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'RecurringEachXDays' |
| RecurringEachMonth | RecurringEachMonth value. Stored as 'M'. <br /> _Database Value:_ 'M' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'RecurringEachMonth' |
| RecurringEachWeek | RecurringEachWeek value. Stored as 'W'. <br /> _Database Value:_ 'W' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'RecurringEachWeek' |

_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Name

> The name of this WorkSchedule. [Required] [Filter(like)]

_Type_: **string**  
_Supported Filters_: **Like**  
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

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Gen_Work_Schedules?$top=10>

