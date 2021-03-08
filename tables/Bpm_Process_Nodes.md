# Table Bpm_Process_Nodes

Contains the flow Nodes of the process model. Entity: Bpm_Process_Nodes

# Aggregate Hierarchy

* [Bpm_Processes](Bpm_Processes.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Process_Node_Id|`Guid`|`PK`, Readonly||
|Process_Node_Code|`String`||Node code, unique within the process. Used as ID for XML serialization purposes. `Required` `Filter(eq;like)` |
|Instructions_Html|`String`||Detailed instructions to the executor in HTML format. `Filter(eq;like)` |
|Process_Node_Name|`MultilanguageString`||Multilanguage process name. `Required` `Filter(eq;like)` |
|Node_Type|`NodeType`|Allowed: `A`, `E`, `G`, `C`|Type of the node. A=Text Annotation; E=Event; G=Gateway; T=Task; P=Sub-Process. `Required` `Filter(eq;like)` |
