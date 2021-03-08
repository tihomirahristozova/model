# Table Bpm_Processes

Represents one business process version. All process model elements and execution instances are bound to specfic process version. Entity: Bpm_Processes

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Process_Id|`Guid`|`PK`, Readonly||
|Process_Code|`String`||Unique process code. `Required` `Filter(multi eq)` `ORD` |
|Description|`String`||The description of this Process. `Filter(eq;like)` |
|Is_Executable|`Boolean`||Specifies whether the process is executable. In order to be executable, a process must contain enough execution details. Note, that some processes are only for documentation purposes and are not intended to be executed. `Required` `Default(false)` `Filter(eq)` |
|Is_Published|`Boolean`||Specifies whether the process is currently published for new instances. `Required` `Default(false)` `Filter(eq)` |
|Locality|`Locality`|Allowed: `P`, `L`, `C`, `I`|Process execution locality. Represents where the execution takes place and influences the selection of possible executors. For example, when L, the execution is private to the location, where the process originated. P=Same as parent; L=Location; C=Company; I=Intra-company. `Required` `Default("L")` `Filter(like)` |
|Process_Name|`String`||The name of this Process. `Required` `Filter(eq;like)` |
