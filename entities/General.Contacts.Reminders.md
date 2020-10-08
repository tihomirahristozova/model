---
uid: General.Contacts.Reminders
---
# General.Contacts.Reminders

Reminders for activities. The reminders are alarms, which can be turned off. Each activity can have multiple reminders. Entity: Cm_Reminders

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](General.Contacts.Reminders.md#id) | guid |  
| [IsDefault](General.Contacts.Reminders.md#isdefault) | boolean | True when this is the defult reminder for a task. The default reminder is controlled through the task, while non-default reminders are manipulated through separate form. [Required] [Default(false)] [Filter(eq)] 
| [IsDismissed](General.Contacts.Reminders.md#isdismissed) | boolean | When true the reminder was dismissed by the user; the initial value is false. [Required] [Default(false)] [Filter(eq)] 
| [Notes](General.Contacts.Reminders.md#notes) | string (nullable) | Notes that describe this specific reminder for the task. 
| [ReminderTime](General.Contacts.Reminders.md#remindertime) | datetime | The time when the alarm should snooze to the user. [Required] [Filter(ge;le)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Activity](General.Contacts.Reminders.md#activity) | [General.Contacts.Activities](General.Contacts.Activities.md) | The activity to which this reminder is attached. [Required] [Filter(multi eq)] [Owner] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### IsDefault

> True when this is the defult reminder for a task. The default reminder is controlled through the task, while non-default reminders are manipulated through separate form. [Required] [Default(false)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### IsDismissed

> When true the reminder was dismissed by the user; the initial value is false. [Required] [Default(false)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### Notes

> Notes that describe this specific reminder for the task.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ReminderTime

> The time when the alarm should snooze to the user. [Required] [Filter(ge;le)]

_Type_: **datetime**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  


## Reference Details

### Activity

> The activity to which this reminder is attached. [Required] [Filter(multi eq)] [Owner]

_Type_: **[General.Contacts.Activities](General.Contacts.Activities.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=General.Contacts.Reminders erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.Contacts.Reminders erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=General.Contacts.Reminders erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_Contacts_Reminders?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_Contacts_Reminders?$top=10>

