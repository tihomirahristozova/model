# Table Bpm_Process_Nodes

Contains the flow Nodes of the process model. Entity: Bpm_Process_Nodes

## Owner Tables Hierarchy

* [Bpm_Processes](Bpm_Processes.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Process_Node_Id](#process_node_id)|`uniqueidentifier` `PK`||
|[Process_Id](#process_id)|`uniqueidentifier` |The process, to which this Node belongs.|
|[Process_Lane_Id](#process_lane_id)|`uniqueidentifier` |The process lane to which this Node belongs.|
|[Process_Node_Code](#process_node_code)|`nvarchar(16)` |Node code, unique within the process. Used as ID for XML serialization purposes.|
|[Process_Node_Name](#process_node_name)|`nvarchar(512)` `ML`|Multilanguage process name.|
|[Node_Type](#node_type)|`nvarchar(1)` Allowed: `A`, `E`, `G`, `C`|Type of the node. A=Text Annotation; E=Event; G=Gateway; T=Task; P=Sub-Process.|
|[Instructions_Html](#instructions_html)|`nvarchar(2147483647)` |Detailed instructions to the executor in HTML format.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Process_Node_Id


Process_Node_Id

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
|Derived From|[Bpm_Process_Nodes](Bpm_Process_Nodes.md).[Process_Node_Id](Bpm_Process_Nodes.md#process_node_id)|
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
|Equals|NULL|no|no|

### Process_Id


Process_Id


The process, to which this Node belongs.


The process, to which this Node belongs.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|yes|
|Referenced Table|[Bpm_Processes](Bpm_Processes.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Bpm_Process_Nodes](Bpm_Process_Nodes.md).[Process_Id](Bpm_Process_Nodes.md#process_id)|
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

### Process_Lane_Id


Process_Lane_Id


The process lane to which this Node belongs.


The process lane to which this Node belongs.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Bpm_Process_Lanes](Bpm_Process_Lanes.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Bpm_Process_Nodes](Bpm_Process_Nodes.md).[Process_Lane_Id](Bpm_Process_Nodes.md#process_lane_id)|
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

### Process_Node_Code


Process_Node_Code


Node code, unique within the process. Used as ID for XML serialization purposes.


Node code, unique within the process. Used as ID for XML serialization purposes.

| Property | Value |
| - | - |
|Type|nvarchar(16)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Bpm_Process_Nodes](Bpm_Process_Nodes.md).[Process_Node_Code](Bpm_Process_Nodes.md#process_node_code)|
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
|Max Length|16|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|
|Like|None|no|no|

### Process_Node_Name


Process_Node_Name


Multilanguage process name.


Multilanguage process name.

| Property | Value |
| - | - |
|Type|nvarchar(512)|
|Is Mulitlanguage|yes|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Bpm_Process_Nodes](Bpm_Process_Nodes.md).[Process_Node_Name](Bpm_Process_Nodes.md#process_node_name)|
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
|Max Length|512|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|
|Like|None|no|no|

### Node_Type


Node_Type


Type of the node. A=Text Annotation; E=Event; G=Gateway; T=Task; P=Sub-Process.


Type of the node. A=Text Annotation; E=Event; G=Gateway; T=Task; P=Sub-Process.

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
|Allowed Values|`A`, `E`, `G`, `C`|
|Default Value|None|
|Derived From|[Bpm_Process_Nodes](Bpm_Process_Nodes.md).[Node_Type](Bpm_Process_Nodes.md#node_type)|
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

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|
|Like|None|no|no|

### Instructions_Html


Instructions_Html


Detailed instructions to the executor in HTML format.


Detailed instructions to the executor in HTML format.

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Bpm_Process_Nodes](Bpm_Process_Nodes.md).[Instructions_Html](Bpm_Process_Nodes.md#instructions_html)|
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
|Max Length|2147483647|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|
|Like|None|no|no|

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
|Derived From|[Bpm_Process_Nodes](Bpm_Process_Nodes.md).[Row_Version](Bpm_Process_Nodes.md#row_version)|
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


