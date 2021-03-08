# Table Log_Logistic_Unit_Specifications

Specification of a logistic unit. The database can contain any kind of specification, but most client applications and integrated methods process GS1 specifications (application codes). Entity: Log_Logistic_Unit_Specifications (Introduced in version 21.1.0.77)

# Aggregate Hierarchy

* [Log_Logistic_Units](Log_Logistic_Units.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Logistic_Unit_Specification_Id|`Guid`|`PK`, Readonly||
|Code|`String`||The code of the specification, unique within the logistic unit. It can contain only alphanumeric characters and cannot contain spaces. `Required` `Filter(multi eq;like)` |
|Name|`MultilanguageString`||Multi-language name of the specification. For some processing purposes, the name might be contained within the client implementation and not saved to the database (null). `Filter(eq;like)` |
|Notes|`String`||Notes for this LogisticUnitSpecification. |
|Value|`String`||Text value of the specification. If this is GS1 specification, it can contain only numbers and letters and cannot contain spaces. `Filter(eq;like)` |
