# Table Bpm_Process_Node_Events

Abstract root of all process node events. Currently - not used. Entity: Bpm_Process_Node_Events

## Summary

| Name | Type | Description |
| - | - | --- |
|[Process_Node_Event_Id](#process_node_event_id)|`uniqueidentifier` `PK`||
|[Process_Node_Id](#process_node_id)|`uniqueidentifier` |The node of this node event.|
|[Event_Type](#event_type)|`nvarchar(1)` |Event type. S=Start, T=Intermediate Throw, C=Intermediate Catch, B=Boundary, E=End.|
|[Is_Message](#is_message)|`bit` |True if this is message event.|
|[Is_Timer](#is_timer)|`bit` |True if this is timer event.|
|[Is_Signal](#is_signal)|`bit` |True if this is signal event.|
|[Is_Escalation](#is_escalation)|`bit` |True if this is escalation event.|
|[Is_Error](#is_error)|`bit` |True if this is error event.|
|[Is_Cancel](#is_cancel)|`bit` |True if this is cancel event.|
|[Is_Compensation](#is_compensation)|`bit` |True if this is compensation event.|
|[Event_Key](#event_key)|`nvarchar(128)` |The unique event key, which is thrown or caught.|
|[Boundary_Of_Process_Node_Id](#boundary_of_process_node_id)|`uniqueidentifier` |When the event is boundary, contains the node to which the event is bound. Otherwise contains NULL.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Process_Node_Event_Id


Process_Node_Event_Id

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
|Derived From|[Bpm_Process_Node_Events](Bpm_Process_Node_Events.md).[Process_Node_Event_Id](Bpm_Process_Node_Events.md#process_node_event_id)|
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
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Process_Node_Id


Process_Node_Id


The node of this node event.


The node of this node event.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Bpm_Process_Node_Events](Bpm_Process_Node_Events.md).[Process_Node_Id](Bpm_Process_Node_Events.md#process_node_id)|
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
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Event_Type


Event_Type


Event type. S=Start, T=Intermediate Throw, C=Intermediate Catch, B=Boundary, E=End.


Event type. S=Start, T=Intermediate Throw, C=Intermediate Catch, B=Boundary, E=End.

| Property | Value |
| - | - |
|Type|nvarchar(1)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Bpm_Process_Node_Events](Bpm_Process_Node_Events.md).[Event_Type](Bpm_Process_Node_Events.md#event_type)|
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
|Max Length|1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Is_Message


Is_Message


True if this is message event.


True if this is message event.

| Property | Value |
| - | - |
|Type|bit|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Bpm_Process_Node_Events](Bpm_Process_Node_Events.md).[Is_Message](Bpm_Process_Node_Events.md#is_message)|
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
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Is_Timer


Is_Timer


True if this is timer event.


True if this is timer event.

| Property | Value |
| - | - |
|Type|bit|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Bpm_Process_Node_Events](Bpm_Process_Node_Events.md).[Is_Timer](Bpm_Process_Node_Events.md#is_timer)|
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
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Is_Signal


Is_Signal


True if this is signal event.


True if this is signal event.

| Property | Value |
| - | - |
|Type|bit|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Bpm_Process_Node_Events](Bpm_Process_Node_Events.md).[Is_Signal](Bpm_Process_Node_Events.md#is_signal)|
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
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Is_Escalation


Is_Escalation


True if this is escalation event.


True if this is escalation event.

| Property | Value |
| - | - |
|Type|bit|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Bpm_Process_Node_Events](Bpm_Process_Node_Events.md).[Is_Escalation](Bpm_Process_Node_Events.md#is_escalation)|
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
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Is_Error


Is_Error


True if this is error event.


True if this is error event.

| Property | Value |
| - | - |
|Type|bit|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Bpm_Process_Node_Events](Bpm_Process_Node_Events.md).[Is_Error](Bpm_Process_Node_Events.md#is_error)|
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
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Is_Cancel


Is_Cancel


True if this is cancel event.


True if this is cancel event.

| Property | Value |
| - | - |
|Type|bit|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Bpm_Process_Node_Events](Bpm_Process_Node_Events.md).[Is_Cancel](Bpm_Process_Node_Events.md#is_cancel)|
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
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Is_Compensation


Is_Compensation


True if this is compensation event.


True if this is compensation event.

| Property | Value |
| - | - |
|Type|bit|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Bpm_Process_Node_Events](Bpm_Process_Node_Events.md).[Is_Compensation](Bpm_Process_Node_Events.md#is_compensation)|
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
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Event_Key


Event_Key


The unique event key, which is thrown or caught.


The unique event key, which is thrown or caught.

| Property | Value |
| - | - |
|Type|nvarchar(128)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Bpm_Process_Node_Events](Bpm_Process_Node_Events.md).[Event_Key](Bpm_Process_Node_Events.md#event_key)|
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
|Max Length|128|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Boundary_Of_Process_Node_Id


Boundary_Of_Process_Node_Id


When the event is boundary, contains the node to which the event is bound. Otherwise contains NULL.


When the event is boundary, contains the node to which the event is bound. Otherwise contains NULL.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Bpm_Process_Node_Events](Bpm_Process_Node_Events.md).[Boundary_Of_Process_Node_Id](Bpm_Process_Node_Events.md#boundary_of_process_node_id)|
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
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

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
|Derived From|[Bpm_Process_Node_Events](Bpm_Process_Node_Events.md).[Row_Version](Bpm_Process_Node_Events.md#row_version)|
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
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|


