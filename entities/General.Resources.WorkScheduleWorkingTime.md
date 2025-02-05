---
uid: General.Resources.WorkScheduleWorkingTime
---
# General.Resources.WorkScheduleWorkingTime Entity

**Namespace:** [General.Resources](General.Resources.md)  

Contains the different working time periods within the work schedule. Entity: Gen_Work_Schedule_Working_Time

## Default Visualization
Default Display Text Format:  
_{WorkSchedule.Name}_  
Default Search Members:  
_WorkSchedule.Name_  
Name Data Member:  
_WorkSchedule.Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[General.Resources.WorkSchedules](General.Resources.WorkSchedules.md)  
Aggregate Root:  
[General.Resources.WorkSchedules](General.Resources.WorkSchedules.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [DayNo](General.Resources.WorkScheduleWorkingTime.md#dayno) | int32 | Consequtive day in the work schedule recurrence, starting at 1. `Required` 
| [DisplayText](General.Resources.WorkScheduleWorkingTime.md#displaytext) | string | Uses the repository DisplayTextFormat to build the display text from the attributes and references of current object. 
| [EndTime](General.Resources.WorkScheduleWorkingTime.md#endtime) | time | End of working time period. `Required` 
| [Id](General.Resources.WorkScheduleWorkingTime.md#id) | guid |  
| [ObjectVersion](General.Resources.WorkScheduleWorkingTime.md#objectversion) | int32 | The latest version of the extensible data object for the aggregate root for the time the object is loaded from the database. Can be used for optimistic locking. 
| [StartTime](General.Resources.WorkScheduleWorkingTime.md#starttime) | time | Start of working time period on the day, specified by Day_No. `Required` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [WorkSchedule](General.Resources.WorkScheduleWorkingTime.md#workschedule) | [WorkSchedules](General.Resources.WorkSchedules.md) | The <see cref="WorkSchedule"/> to which this WorkScheduleWorkingTime belongs. `Required` `Filter(multi eq)` `Owner` |


## Attribute Details

### DayNo

Consequtive day in the work schedule recurrence, starting at 1. `Required`

_Type_: **int32**  
_Category_: **System**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### DisplayText

Uses the repository DisplayTextFormat to build the display text from the attributes and references of current object.

_Type_: **string**  
_Category_: **Calculated Attributes**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  

### EndTime

End of working time period. `Required`

_Type_: **time**  
_Category_: **System**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Category_: **System**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### ObjectVersion

The latest version of the extensible data object for the aggregate root for the time the object is loaded from the database. Can be used for optimistic locking.

_Type_: **int32**  
_Category_: **Extensible Data Object**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  

### StartTime

Start of working time period on the day, specified by Day_No. `Required`

_Type_: **time**  
_Category_: **System**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### WorkSchedule

The <see cref="WorkSchedule"/> to which this WorkScheduleWorkingTime belongs. `Required` `Filter(multi eq)` `Owner`

_Type_: **[WorkSchedules](General.Resources.WorkSchedules.md)**  
_Indexed_: **True**  
_Category_: **System**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  


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


### CreateNotification

Creates a notification a sends a real time event to the user.  
_Return Type_: **void**  
_Declaring Type_: **EntityObject**  
_Domain API Request_: **POST**  

**Parameters**  
  * **user**  
    The user.  
    _Type_: [Users](Systems.Security.Users.md)  

  * **notificationClass**  
    The notification class.  
    _Type_: string  

  * **subject**  
    The subject.  
    _Type_: string  


### CreateCopy

Duplicates the object and its child objects belonging to the same aggregate.              The duplicated objects are not saved to the data source but remain in the same transaction as the original object.  
_Return Type_: **EntityObject**  
_Declaring Type_: **EntityObject**  
_Domain API Request_: **POST**  


## Business Rules

[!list limit=1000 erp.entity=General.Resources.WorkScheduleWorkingTime erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=General.Resources.WorkScheduleWorkingTime erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_Resources_WorkScheduleWorkingTime?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_Resources_WorkScheduleWorkingTime?$top=10>

