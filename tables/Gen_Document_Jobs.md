# Table Gen_Document_Jobs

Represents jobs, which change state of documents. Entity: Gen_Document_Jobs (Introduced in version 20.1)

# Inheritance

* [Sys_Jobs](Sys_Jobs.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Document_Job_Id|`Guid`|`PK`, Readonly||
|Filter_Xml|`DataAccessFilter`||Specifies the documents, whose state will be changed. `Required` |
|Is_Active|`Boolean`|||
|Job_Type|`JobType`|Allowed: `DOC`, `POS`, `DNT`, `DPI`||
|Job_Name|`String`|||
|New_State|`DocumentState`|Allowed: `0`, `5`, `10`, `20`, `30`, `40`, `50`|Specifies the state, which should be set to the documents, matching the filter. `Required` |
|Notes|`String`|||
|Run_On_Idle|`Boolean`|||
