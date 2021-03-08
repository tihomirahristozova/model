# Table Cm_Reminders

Reminders for activities. The reminders are alarms, which can be turned off. Each activity can have multiple reminders. Entity: Cm_Reminders

# Aggregate Hierarchy

* [Cm_Activities](Cm_Activities.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Reminder_Id|`Guid`|`PK`, Readonly||
|Is_Default|`Boolean`||True when this is the defult reminder for a task. The default reminder is controlled through the task, while non-default reminders are manipulated through separate form. `Required` `Default(false)` `Filter(eq)` |
|Is_Dismissed|`Boolean`||When true the reminder was dismissed by the user; the initial value is false. `Required` `Default(false)` `Filter(eq)` |
|Notes|`String`||Notes that describe this specific reminder for the task. |
|Reminder_Time|`DateTime`||The time when the alarm should snooze to the user. `Required` `Filter(ge;le)` |
