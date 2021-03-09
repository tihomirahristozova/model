# Query Sys_User_Business_Rule_Events_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[User_Business_Rule_Event_Id](#user_business_rule_event_id)|`uniqueidentifier` `PK`||
|[User_Business_Rule_Id](#user_business_rule_id)|`uniqueidentifier` |The rule, which will be registered for the event.|
|[Layer](#layer)|`nvarchar` Allowed: `FTE`, `BKE`|Specifies the layer on which to register the event. Allowed values = FTE-FrontEnd, BKE-BackEnd.|
|[Event_Type](#event_type)|`nvarchar` Allowed: `AGGREGATECLIENTCOMMIT`, `ATTRIBUTECHANGED`, `ATTRIBUTECHANGING`, `CLIENTCOMMIT`, `COMMIT`, `STATECHANGED`, `STATECHANGING`, `VOIDING`|The event for which to register the business rule.|
|[Event_Parameter](#event_parameter)|`nvarchar` ||
|[Execution_Priority](#execution_priority)|`int` Allowed: `30`, `50`, `70`||
|[Row_Version](#row_version)|`timestamp` ||

## Columns

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
|Type|nvarchar|

### Event_Type

| Property | Value |
| - | - |
|Type|nvarchar|

### Event_Parameter

| Property | Value |
| - | - |
|Type|nvarchar|

### Execution_Priority

| Property | Value |
| - | - |
|Type|int|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


