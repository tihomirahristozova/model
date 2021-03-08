# Table Sys_Object_Versions

Contains history of saved version of the managed objects. Entity: Sys_Object_Versions

# Aggregate Hierarchy

* [Sys_Objects](Sys_Objects.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Object_Version_Id|`Guid`|`PK`, Readonly||
|Object_Contents|`Byte[]`|`BLOB`|The compressed contents of the object. `Required` |
|Server_Version|`String`||The version of the EnterpriseOne server, which created the version. The version should be in the form (9.9.9.9). null means the version is unknown. |
|Version|`Int32`||The version number of the version, stored in the current row, starting from 1. `Required` `Filter(multi eq;ge;le)` |
|Version_Time|`DateTime`||The timestamp when the version was saved. `Required` `Filter(ge;le)` |
|Version_Type|`VersionType`|Allowed: `C`, `U`|Specifies the action, which occurred on the actual object, referred by the system object.  'C' means that with this version the object was created. 'U' means that this is an update to an existing object. `Required` |
