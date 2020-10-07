# Production.Resources.WorkgroupShifts

Contains the working shifts of the wrokgroups. Entity: Prd_Workgroup_Shifts

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Production.Resources.WorkgroupShifts.md#Id) | guid |  
| [EfficiencyFactorPercent](Production.Resources.WorkgroupShifts.md#EfficiencyFactorPercent) | decimal | Efficiency factor of the routing steps for this shift, expressed as percentage. [Required] [Default(1)] 
| [EstablishmentDate](Production.Resources.WorkgroupShifts.md#EstablishmentDate) | datetime | When the workgroup shift was established. Used as minimum date when generating calendar. [Required] [Default(Today)] [Filter(ge;le)] 
| [ShiftName](Production.Resources.WorkgroupShifts.md#ShiftName) | string | The name of the workgroup shift. [Required] [Filter(like)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [WorkSchedule](Production.Resources.WorkgroupShifts.md#WorkSchedule) | [General.Resources.WorkSchedules](General.Resources.WorkSchedules.md) | The work schedule used to calculate the working time for the shift. [Required] [Filter(multi eq)] |
| [Workgroup](Production.Resources.WorkgroupShifts.md#Workgroup) | [Production.Resources.Workgroups](Production.Resources.Workgroups.md) | The [Workgroup](Production.Resources.WorkgroupShifts.md#Workgroup) to which this WorkgroupShift belongs. [Required] [Filter(multi eq)] [Owner] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### EfficiencyFactorPercent

> Efficiency factor of the routing steps for this shift, expressed as percentage. [Required] [Default(1)]

_Type_: **decimal**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **1**  

### EstablishmentDate

> When the workgroup shift was established. Used as minimum date when generating calendar. [Required] [Default(Today)] [Filter(ge;le)]

_Type_: **datetime**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **CurrentDate**  

### ShiftName

> The name of the workgroup shift. [Required] [Filter(like)]

_Type_: **string**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  


## Reference Details

### WorkSchedule

> The work schedule used to calculate the working time for the shift. [Required] [Filter(multi eq)]

_Type_: **[General.Resources.WorkSchedules](General.Resources.WorkSchedules.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Workgroup

> The [Workgroup](Production.Resources.WorkgroupShifts.md#Workgroup) to which this WorkgroupShift belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Production.Resources.Workgroups](Production.Resources.Workgroups.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Production.Resources.WorkgroupShifts erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Production.Resources.WorkgroupShifts erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Production.Resources.WorkgroupShifts erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Production_Resources_WorkgroupShifts?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Production_Resources_WorkgroupShifts?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Prd_Workgroup_Shifts?$top=10>

