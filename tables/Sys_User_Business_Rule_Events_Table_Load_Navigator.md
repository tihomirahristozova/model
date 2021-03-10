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


User_Business_Rule_Event_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|yes|
|Order in Primary Key|1|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|NewGuid|
|Derived From|[Sys_User_Business_Rule_Events](Sys_User_Business_Rule_Events.md).[User_Business_Rule_Event_Id](Sys_User_Business_Rule_Events.md#user_business_rule_event_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|0|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### User_Business_Rule_Id


User_Business_Rule_Id


The rule, which will be registered for the event.


The rule, which will be registered for the event.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Sys_User_Business_Rules](Sys_User_Business_Rules.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sys_User_Business_Rule_Events](Sys_User_Business_Rule_Events.md).[User_Business_Rule_Id](Sys_User_Business_Rule_Events.md#user_business_rule_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|1|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Layer


Layer


Specifies the layer on which to register the event. Allowed values = FTE-FrontEnd, BKE-BackEnd.


Specifies the layer on which to register the event. Allowed values = FTE-FrontEnd, BKE-BackEnd.

| Property | Value |
| - | - |
|Type|nvarchar|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Allowed Values|`FTE`, `BKE`|
|Default Value|BKE|
|Derived From|[Sys_User_Business_Rule_Events](Sys_User_Business_Rule_Events.md).[Layer](Sys_User_Business_Rule_Events.md#layer)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|2|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Event_Type


Event_Type


The event for which to register the business rule.


The event for which to register the business rule.

| Property | Value |
| - | - |
|Type|nvarchar|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Allowed Values|`AGGREGATECLIENTCOMMIT`, `ATTRIBUTECHANGED`, `ATTRIBUTECHANGING`, `CLIENTCOMMIT`, `COMMIT`, `STATECHANGED`, `STATECHANGING`, `VOIDING`|
|Default Value|None|
|Derived From|[Sys_User_Business_Rule_Events](Sys_User_Business_Rule_Events.md).[Event_Type](Sys_User_Business_Rule_Events.md#event_type)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|3|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Event_Parameter


Event_Parameter

| Property | Value |
| - | - |
|Type|nvarchar|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sys_User_Business_Rule_Events](Sys_User_Business_Rule_Events.md).[Event_Parameter](Sys_User_Business_Rule_Events.md#event_parameter)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|4|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Execution_Priority


Execution_Priority

| Property | Value |
| - | - |
|Type|int|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Allowed Values|`30`, `50`, `70`|
|Default Value|50|
|Derived From|[Sys_User_Business_Rule_Events](Sys_User_Business_Rule_Events.md).[Execution_Priority](Sys_User_Business_Rule_Events.md#execution_priority)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|5|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Row_Version


Row_Version

| Property | Value |
| - | - |
|Type|timestamp|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sys_User_Business_Rule_Events](Sys_User_Business_Rule_Events.md).[Row_Version](Sys_User_Business_Rule_Events.md#row_version)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|6|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|


