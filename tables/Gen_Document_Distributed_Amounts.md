# Table Gen_Document_Distributed_Amounts

Contains the amounts which are distributed by the system over the document lines as a result of additional amount calculations. Entity: Gen_Document_Distributed_Amounts

# Aggregate Hierarchy

* [Gen_Documents](Gen_Documents.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Distributed_Amount_Id|`Guid`|`PK`, Readonly||
|Document_Line_Id|`Guid?`||The Id of the line over which the amount is distributed. `Filter(multi eq)` |
