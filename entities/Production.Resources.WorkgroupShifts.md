---
uid: Production.Resources.WorkgroupShifts
---
# Production.Resources.WorkgroupShifts Entity

**Namespace:** [Production.Resources](Production.Resources.md)  

Contains the working shifts of the wrokgroups. Entity: Prd_Workgroup_Shifts

## Default Visualization
Default Display Text Format:  
_{ShiftName}_  
Default Search Members:  
_ShiftName_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[Production.Resources.Workgroups](Production.Resources.Workgroups.md)  
Aggregate Root:  
[Production.Resources.Workgroups](Production.Resources.Workgroups.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [EfficiencyFactorPercent](Production.Resources.WorkgroupShifts.md#efficiencyfactorpercent) | decimal (3, 2) | Efficiency factor of the routing steps for this shift, expressed as percentage. `Required` `Default(1)` 
| [EstablishmentDate](Production.Resources.WorkgroupShifts.md#establishmentdate) | datetime | When the workgroup shift was established. Used as minimum date when generating calendar. `Required` `Default(Today)` `Filter(ge;le)` 
| [Id](Production.Resources.WorkgroupShifts.md#id) | guid |  
| [ObjectVersion](Production.Resources.WorkgroupShifts.md#objectversion) | int32 |  
| [ShiftName](Production.Resources.WorkgroupShifts.md#shiftname) | string (254) | The name of the workgroup shift. `Required` `Filter(like)` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Workgroup](Production.Resources.WorkgroupShifts.md#workgroup) | [Workgroups](Production.Resources.Workgroups.md) | The <see cref="Workgroup"/> to which this WorkgroupShift belongs. `Required` `Filter(multi eq)` `Owner` |
| [WorkSchedule](Production.Resources.WorkgroupShifts.md#workschedule) | [WorkSchedules](General.Resources.WorkSchedules.md) | The work schedule used to calculate the working time for the shift. `Required` `Filter(multi eq)` |


## Attribute Details

### EfficiencyFactorPercent

Efficiency factor of the routing steps for this shift, expressed as percentage. `Required` `Default(1)`

_Type_: **decimal (3, 2)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **1**  

### EstablishmentDate

When the workgroup shift was established. Used as minimum date when generating calendar. `Required` `Default(Today)` `Filter(ge;le)`

_Type_: **datetime**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **CurrentDate**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### ObjectVersion

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  

### ShiftName

The name of the workgroup shift. `Required` `Filter(like)`

_Type_: **string (254)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  


## Reference Details

### Workgroup

The <see cref="Workgroup"/> to which this WorkgroupShift belongs. `Required` `Filter(multi eq)` `Owner`

_Type_: **[Workgroups](Production.Resources.Workgroups.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  

### WorkSchedule

The work schedule used to calculate the working time for the shift. `Required` `Filter(multi eq)`

_Type_: **[WorkSchedules](General.Resources.WorkSchedules.md)**  
_Supported Filters_: **Equals, EqualsIn**  


## API Methods

Methods that can be invoked in public APIs.

### GetAllowedCustomPropertyValues

Gets the allowed values for the specified custom property for this entity object.              If supported the result is ordered by property value. Some property value sources do not support ordering - in that case the result is not ordered.  
_Return Type_: **Collection Of [CustomPropertyValue](../data-types.md#general.custompropertyvalue)**  
_Declaring Type_: **EntityObject**  
_Domain API Request_: **GET**  

**Parameters**  
  * **customPropertyCode**  
    The code of the custom property  
    _Type_: string  

  * **search**  
    The search text - searches by value or description. Can contain wildcard character %.  
    _Type_: string  
     _Optional_: True  
    _Default Value_: null  

  * **exactMatch**  
    If true the search text should be equal to the property value  
    _Type_: boolean  
     _Optional_: True  
    _Default Value_: False  

  * **orderByDescription**  
    If true the result is ordered by Description instead of Value. Note that ordering is not always possible.  
    _Type_: boolean  
     _Optional_: True  
    _Default Value_: False  

  * **top**  
    The top clause - default is 10  
    _Type_: int32  
     _Optional_: True  
    _Default Value_: 10  

  * **skip**  
    The skip clause - default is 0  
    _Type_: int32  
     _Optional_: True  
    _Default Value_: 0  



## Business Rules

[!list limit=1000 erp.entity=Production.Resources.WorkgroupShifts erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Production.Resources.WorkgroupShifts erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Production_Resources_WorkgroupShifts?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Production_Resources_WorkgroupShifts?$top=10>

