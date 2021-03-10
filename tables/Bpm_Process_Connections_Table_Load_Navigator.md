# Query Bpm_Process_Connections_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Process_Connection_Id](#process_connection_id)|`uniqueidentifier` `PK`||
|[Process_Id](#process_id)|`uniqueidentifier` |The process version to which this connection belongs.|
|[Process_Connection_Code](#process_connection_code)|`nvarchar` |Connection code, unique within the process. Used as ID for XML serialization purposes.|
|[Process_Connection_Name](#process_connection_name)|`nvarchar` `ML`|Multilanguage connection name.|
|[Source_Process_Node_Id](#source_process_node_id)|`uniqueidentifier` |The element, from which the connection starts. The element should be in the same process as the connection.|
|[Target_Process_Node_Id](#target_process_node_id)|`uniqueidentifier` |The element, at which the connection ends. The element should be in the same process as the connection.|
|[Condition_Filter_Xml](#condition_filter_xml)|`nvarchar` |When not NULL, specifies that the flow will be followed only if the condition is matched by the current values in the process instance.|
|[Is_Default](#is_default)|`bit` |Denotes this flow as the default sequence flow. It is taken only when all other flows are not valid. For example, gateways usually are followed by several conditional flows and one default flow.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Process_Connection_Id


Process_Connection_Id

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
|Derived From|[Bpm_Process_Connections](Bpm_Process_Connections.md).[Process_Connection_Id](Bpm_Process_Connections.md#process_connection_id)|
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

### Process_Id


Process_Id


The process version to which this connection belongs.


The process version to which this connection belongs.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Bpm_Processes](Bpm_Processes.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Bpm_Process_Connections](Bpm_Process_Connections.md).[Process_Id](Bpm_Process_Connections.md#process_id)|
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
|Order|1|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Process_Connection_Code


Process_Connection_Code


Connection code, unique within the process. Used as ID for XML serialization purposes.


Connection code, unique within the process. Used as ID for XML serialization purposes.

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
|Default Value|NewGuid|
|Derived From|[Bpm_Process_Connections](Bpm_Process_Connections.md).[Process_Connection_Code](Bpm_Process_Connections.md#process_connection_code)|
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
|Order|2|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|
|Like|None|no|no|

### Process_Connection_Name


Process_Connection_Name


Multilanguage connection name.


Multilanguage connection name.

| Property | Value |
| - | - |
|Type|nvarchar|
|Is Mulitlanguage|yes|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Bpm_Process_Connections](Bpm_Process_Connections.md).[Process_Connection_Name](Bpm_Process_Connections.md#process_connection_name)|
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

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|
|Like|None|no|no|

### Source_Process_Node_Id


Source_Process_Node_Id


The element, from which the connection starts. The element should be in the same process as the connection.


The element, from which the connection starts. The element should be in the same process as the connection.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Bpm_Process_Nodes](Bpm_Process_Nodes.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Bpm_Process_Connections](Bpm_Process_Connections.md).[Source_Process_Node_Id](Bpm_Process_Connections.md#source_process_node_id)|
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
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Target_Process_Node_Id


Target_Process_Node_Id


The element, at which the connection ends. The element should be in the same process as the connection.


The element, at which the connection ends. The element should be in the same process as the connection.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Bpm_Process_Nodes](Bpm_Process_Nodes.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Bpm_Process_Connections](Bpm_Process_Connections.md).[Target_Process_Node_Id](Bpm_Process_Connections.md#target_process_node_id)|
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
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Condition_Filter_Xml


Condition_Filter_Xml


When not NULL, specifies that the flow will be followed only if the condition is matched by the current values in the process instance.


When not NULL, specifies that the flow will be followed only if the condition is matched by the current values in the process instance.

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
|Derived From|[Bpm_Process_Connections](Bpm_Process_Connections.md).[Condition_Filter_Xml](Bpm_Process_Connections.md#condition_filter_xml)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|yes|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|6|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|
|Like|None|no|no|

### Is_Default


Is_Default


Denotes this flow as the default sequence flow. It is taken only when all other flows are not valid. For example, gateways usually are followed by several conditional flows and one default flow.


Denotes this flow as the default sequence flow. It is taken only when all other flows are not valid. For example, gateways usually are followed by several conditional flows and one default flow.

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
|Derived From|[Bpm_Process_Connections](Bpm_Process_Connections.md).[Is_Default](Bpm_Process_Connections.md#is_default)|
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
|Order|7|
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
|Derived From|[Bpm_Process_Connections](Bpm_Process_Connections.md).[Row_Version](Bpm_Process_Connections.md#row_version)|
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
|Order|8|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|


