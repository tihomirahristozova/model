---
uid: Production.Resources.WorkgroupShifts
---
# Production.Resources.WorkgroupShifts Entity

Contains the working shifts of the wrokgroups. Entity: Prd_Workgroup_Shifts

Default Display Text Format:  
_{ShiftName:T}_  
Default Search Member:  
_ShiftName_  

[Aggregate](xref:aggregates) Parent:  
[Production.Resources.Workgroups](Production.Resources.Workgroups.md)  
[Aggregate](xref:aggregates) Root:  
[Production.Resources.Workgroups](Production.Resources.Workgroups.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [EfficiencyFactorPercent](Production.Resources.WorkgroupShifts.md#efficiencyfactorpercent) | decimal | Efficiency factor of the routing steps for this shift, expressed as percentage. [Required] [Default(1)] 
| [EstablishmentDate](Production.Resources.WorkgroupShifts.md#establishmentdate) | datetime | When the workgroup shift was established. Used as minimum date when generating calendar. [Required] [Default(Today)] [Filter(ge;le)] 
| [Id](Production.Resources.WorkgroupShifts.md#id) | guid |  
| [ShiftName](Production.Resources.WorkgroupShifts.md#shiftname) | string | The name of the workgroup shift. [Required] [Filter(like)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Workgroup](Production.Resources.WorkgroupShifts.md#workgroup) | [Workgroups](Production.Resources.Workgroups.md) | The [Workgroup](Production.Resources.WorkgroupShifts.md#workgroup) to which this WorkgroupShift belongs. [Required] [Filter(multi eq)] [Owner] |
| [WorkSchedule](Production.Resources.WorkgroupShifts.md#workschedule) | [WorkSchedules](General.Resources.WorkSchedules.md) | The work schedule used to calculate the working time for the shift. [Required] [Filter(multi eq)] |


## Attribute Details

### EfficiencyFactorPercent

Efficiency factor of the routing steps for this shift, expressed as percentage. [Required] [Default(1)]

_Type_: **decimal**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **1**  

### EstablishmentDate

When the workgroup shift was established. Used as minimum date when generating calendar. [Required] [Default(Today)] [Filter(ge;le)]

_Type_: **datetime**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **CurrentDate**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### ShiftName

The name of the workgroup shift. [Required] [Filter(like)]

_Type_: **string**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  


## Reference Details

### Workgroup

The [Workgroup](Production.Resources.WorkgroupShifts.md#workgroup) to which this WorkgroupShift belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Workgroups](Production.Resources.Workgroups.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### WorkSchedule

The work schedule used to calculate the working time for the shift. [Required] [Filter(multi eq)]

_Type_: **[WorkSchedules](General.Resources.WorkSchedules.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Production.Resources.WorkgroupShifts erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Production.Resources.WorkgroupShifts erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Production_Resources_WorkgroupShifts?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Production_Resources_WorkgroupShifts?$top=10>

