# Table Sys_User_Business_Rule_Events

Represents event registration of a business rule. Entity: Sys_User_Business_Rule_Events

## Owner Tables Hierarchy

* [Sys_User_Business_Rules](Sys_User_Business_Rules.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Event_Type](#event_type)|`nvarchar(64)` Allowed: `AGGREGATECLIENTCOMMIT`, `ATTRIBUTECHANGED`, `ATTRIBUTECHANGING`, `CLIENTCOMMIT`, `COMMIT`, `STATECHANGED`, `STATECHANGING`, `VOIDING`|The event for which to register the business rule.|
|[Event_Parameter](#event_parameter)|`nvarchar(128)` |Registration parameter. The meaning is determined by the event. Usually - attribute name, document state, etc.|
|[Execution_Priority](#execution_priority)|`int` Allowed: `30`, `50`, `70`|Execution priority. Lower values indicate earlier priorities. Possible values - 30-Early, 50-Normal, 70-Late.|
|[User_Business_Rule_Event_Id](#user_business_rule_event_id)|`uniqueidentifier` `PK`||
|[User_Business_Rule_Id](#user_business_rule_id)|`uniqueidentifier` |The rule, which will be registered for the event.|
|[Layer](#layer)|`nvarchar(3)` Allowed: `FTE`, `BKE`|Specifies the layer on which to register the event. Allowed values = FTE-FrontEnd, BKE-BackEnd.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Event_Type

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### Event_Parameter

| Property | Value |
| - | - |
|Type|nvarchar(128)|

### Execution_Priority

| Property | Value |
| - | - |
|Type|int|

### User_Business_Rule_Event_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### User_Business_Rule_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Layer

| Property | Value |
| - | - |
|Type|nvarchar(3)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


