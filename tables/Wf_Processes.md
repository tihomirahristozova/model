# Table Wf_Processes

Contains the business process diagrams. Entity: Wf_Processes

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Process_Id|`Guid`|`PK`, Readonly||
|Creation_Time|`DateTime?`|Readonly|Date and time when the Process was created. `ReadOnly` |
|Creation_User|`String`|Readonly|Login name of the user, who created the Process. `ReadOnly` |
|Is_Landscape|`Boolean`||Specifies whether the process diagram is intended to be viewed in landscape mode. `Required` `Default(true)` |
|Process_Name|`MultilanguageString`||The name of this Process. `Required` `Filter(eq;like)` |
|Notes|`String`||Notes for this Process. |
|Schema_Format|`String`||Application specific format of the Schema Layout. `Required` `Default("D")` |
|Schema_Layout|`String`||Contains the actual presentation layout of the business process. The layout is stored in the format, specified by Schema Format. `Required` |
|Start_Event|`String`||USR=User created; EML=Email receive (still not supported). null means that there is no starting event for this process. |
|Start_Role_Id|`Guid?`||When Start_Event='USR' then specifies the role which the user must play in order to start the process. null when Start_Event<>'USR'. `Filter(multi eq)` |
|Thumbnail|`Byte[]`|`BLOB`|Contains the visual thumbnail of the presentation of the business process. It is stored in bitmap (BMP) format. |
|Update_Time|`DateTime?`|Readonly|Date and time when the Process was last updated. `ReadOnly` |
|Update_User|`String`|Readonly|Login name of the user, who last updated the Process. `ReadOnly` |
