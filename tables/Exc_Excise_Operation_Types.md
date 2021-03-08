# Table Exc_Excise_Operation_Types

Types of excise operations. Used by general documents to specify the operation type according to the excise classifications. Entity: Exc_Excise_Operation_Types (Introduced in version 21.1.1.59)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Excise_Operation_Type_Id|`Guid`|`PK`, Readonly||
|Code|`String`||The unique code of the ExciseOperationType. `Required` `Filter(multi eq;like)` |
|Name|`String`||The name of this ExciseOperationType. `Required` `Filter(multi eq;like)` |
|Notes|`String`||Notes for this ExciseOperationType. |
