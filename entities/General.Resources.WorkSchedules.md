---
uid: General.Resources.WorkSchedules
---
# General.Resources.WorkSchedules Entity

**Namespace:** [General.Resources](General.Resources.md)  

Represents the different working schedules, used by the employees and resources. Entity: Gen_Work_Schedules

## Default Visualization
Default Display Text Format:  
_{Name}_  
Default Search Members:  
_Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [General.Resources.WorkSchedules](General.Resources.WorkSchedules.md)  
  * [General.Resources.WorkScheduleWorkingTime](General.Resources.WorkScheduleWorkingTime.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](General.Resources.WorkSchedules.md#id) | guid |  
| [Name](General.Resources.WorkSchedules.md#name) | string (64) | The name of this WorkSchedule. `Required` `Filter(like)` 
| [NumberOfDays](General.Resources.WorkSchedules.md#numberofdays) | int16 __nullable__ | Number of days in a recurring period. Valid only when Recurrence_Type=D. 
| [ObjectVersion](General.Resources.WorkSchedules.md#objectversion) | int32 |  
| [RecurrenceType](General.Resources.WorkSchedules.md#recurrencetype) | [RecurrenceType](General.Resources.WorkSchedules.md#recurrencetype) | D=recurring each X days; W=recurring each week; M=recurring each month. `Required` `Filter(multi eq)` 

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| WorkingTime | [WorkScheduleWorkingTime](General.Resources.WorkScheduleWorkingTime.md) | List of `WorkScheduleWorkingTime`(General.Resources.WorkScheduleWorkingTime.md) child objects, based on the `General.Resources.WorkScheduleWorkingTime.WorkSchedule`(General.Resources.WorkScheduleWorkingTime.md#workschedule) back reference 


## Attribute Details

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

The name of this WorkSchedule. `Required` `Filter(like)`

_Type_: **string (64)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  
_Maximum Length_: **64**  

### NumberOfDays

Number of days in a recurring period. Valid only when Recurrence_Type=D.

_Type_: **int16 __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ObjectVersion

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  

### RecurrenceType

D=recurring each X days; W=recurring each week; M=recurring each month. `Required` `Filter(multi eq)`

_Type_: **[RecurrenceType](General.Resources.WorkSchedules.md#recurrencetype)**  
Allowed values for the `RecurrenceType`(General.Resources.WorkSchedules.md#recurrencetype) data attribute  
_Allowed Values (General.Resources.WorkSchedulesRepository.RecurrenceType Enum Members)_  

| Value | Description |
| ---- | --- |
| RecurringEachXDays | RecurringEachXDays value. Stored as 'D'. <br /> _Database Value:_ 'D' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'RecurringEachXDays' |
| RecurringEachMonth | RecurringEachMonth value. Stored as 'M'. <br /> _Database Value:_ 'M' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'RecurringEachMonth' |
| RecurringEachWeek | RecurringEachWeek value. Stored as 'W'. <br /> _Database Value:_ 'W' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'RecurringEachWeek' |

_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  


## API Methods

Methods that can be invoked in public APIs.

### GetAllowedCustomPropertyValues

Gets the allowed values for the specified custom property for this entity object.              If supported the result is ordered by property value. Some property value sources does not support ordering.  
_Return Type_: **Collection Of [CustomPropertyValue](../data-types.md#general.custompropertyvalue)**  
_Declaring Type_: **EntityObject**  
_Domain API Request_: **GET**  

**Parameters**  
  * **customPropertyCode**  
    The code of the custom property  
    _Type_: string  

  * **search**  
    The search text - searches by value or description  
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

[!list limit=1000 erp.entity=General.Resources.WorkSchedules erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=General.Resources.WorkSchedules erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_Resources_WorkSchedules?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_Resources_WorkSchedules?$top=10>

