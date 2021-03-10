# Table Gen_Scheduled_Document_Events

Contains postponed events, which will be executed later. Usually these are large number of recalculation events, resulting from other events. For example, releasing a cost correction, publishes postponed events for all affected documents. Entity: Gen_Scheduled_Document_Events

## Summary

| Name | Type | Description |
| - | - | --- |
|[Scheduled_Document_Event_Id](#scheduled_document_event_id)|`uniqueidentifier` `PK`||
|[Source_Document_Id](#source_document_id)|`uniqueidentifier` Readonly|The document that has caused this event to be scheduled|
|[Document_Event](#document_event)|`nvarchar(254)` Readonly|The type of the document event that is scheduled to be processed|
|[Document_Id](#document_id)|`uniqueidentifier` Readonly|The document for which the event will be processed|
|[State](#state)|`smallint` Allowed: `0`, `5`, `10`, `20`, `30`, `40`, `50`, Readonly|The state of the document for which the event will be processed|
|[Processed](#processed)|`bit` Readonly|Indicates wheather the event is already processed or not|
|[Last_Process_Time](#last_process_time)|`datetime` Readonly|The time of the last attempt to process the event|
|[Last_Process_Status](#last_process_status)|`nvarchar(2147483647)` Readonly|Status/information of the last attemp to process the event. Usually shows the cause in case of failure.|
|[Creation_Time](#creation_time)|`datetime` Readonly||
|[Cancelled](#cancelled)|`bit` |When true, specifies that this document event has been cancelled (either manually or in respect to another event) and will not be executed.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Scheduled_Document_Event_Id


Scheduled_Document_Event_Id

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
|Derived From|[Gen_Scheduled_Document_Events](Gen_Scheduled_Document_Events.md).[Scheduled_Document_Event_Id](Gen_Scheduled_Document_Events.md#scheduled_document_event_id)|
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
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|yes|

### Source_Document_Id


Source_Document_Id


The document that has caused this event to be scheduled


The document that has caused this event to be scheduled

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Documents](Gen_Documents.md)|
|Readonly|yes|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Scheduled_Document_Events](Gen_Scheduled_Document_Events.md).[Source_Document_Id](Gen_Scheduled_Document_Events.md#source_document_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
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

### Document_Event


Document_Event


The type of the document event that is scheduled to be processed


The type of the document event that is scheduled to be processed

| Property | Value |
| - | - |
|Type|nvarchar(254)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|yes|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Scheduled_Document_Events](Gen_Scheduled_Document_Events.md).[Document_Event](Gen_Scheduled_Document_Events.md#document_event)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|254|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Document_Id


Document_Id


The document for which the event will be processed


The document for which the event will be processed

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Documents](Gen_Documents.md)|
|Readonly|yes|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Scheduled_Document_Events](Gen_Scheduled_Document_Events.md).[Document_Id](Gen_Scheduled_Document_Events.md#document_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
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

### State


State


The state of the document for which the event will be processed


The state of the document for which the event will be processed

| Property | Value |
| - | - |
|Type|smallint|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|yes|
|Sortable|no|
|Attributes|None|
|Allowed Values|`0`, `5`, `10`, `20`, `30`, `40`, `50`|
|Default Value|None|
|Derived From|[Gen_Scheduled_Document_Events](Gen_Scheduled_Document_Events.md).[State](Gen_Scheduled_Document_Events.md#state)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
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

### Processed


Processed


Indicates wheather the event is already processed or not


Indicates wheather the event is already processed or not

| Property | Value |
| - | - |
|Type|bit|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|yes|
|Sortable|no|
|Attributes|None|
|Default Value|False|
|Derived From|[Gen_Scheduled_Document_Events](Gen_Scheduled_Document_Events.md).[Processed](Gen_Scheduled_Document_Events.md#processed)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
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
|UI Width|Short|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Last_Process_Time


Last_Process_Time


The time of the last attempt to process the event


The time of the last attempt to process the event

| Property | Value |
| - | - |
|Type|datetime|
|DateTime Format|DateTime|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|yes|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Scheduled_Document_Events](Gen_Scheduled_Document_Events.md).[Last_Process_Time](Gen_Scheduled_Document_Events.md#last_process_time)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
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

### Last_Process_Status


Last_Process_Status


Status/information of the last attemp to process the event. Usually shows the cause in case of failure.


Status/information of the last attemp to process the event. Usually shows the cause in case of failure.

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|yes|
|Sortable|no|
|Attributes|None, IsLongString|
|Default Value|None|
|Derived From|[Gen_Scheduled_Document_Events](Gen_Scheduled_Document_Events.md).[Last_Process_Status](Gen_Scheduled_Document_Events.md#last_process_status)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|2147483647|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Long|
|Supports EQUALS_IN|no|

### Creation_Time


Creation_Time

| Property | Value |
| - | - |
|Type|datetime|
|DateTime Format|DateTime|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|yes|
|Sortable|no|
|Attributes|None|
|Default Value|CurrentDateTime|
|Derived From|[Gen_Scheduled_Document_Events](Gen_Scheduled_Document_Events.md).[Creation_Time](Gen_Scheduled_Document_Events.md#creation_time)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
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

### Cancelled


Cancelled


When true, specifies that this document event has been cancelled (either manually or in respect to another event) and will not be executed.


When true, specifies that this document event has been cancelled (either manually or in respect to another event) and will not be executed.

| Property | Value |
| - | - |
|Type|bit|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|False|
|Derived From|[Gen_Scheduled_Document_Events](Gen_Scheduled_Document_Events.md).[Cancelled](Gen_Scheduled_Document_Events.md#cancelled)|
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

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

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
|Derived From|[Gen_Scheduled_Document_Events](Gen_Scheduled_Document_Events.md).[Row_Version](Gen_Scheduled_Document_Events.md#row_version)|
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


