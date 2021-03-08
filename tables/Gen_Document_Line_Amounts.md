# Table Gen_Document_Line_Amounts

Specifies user-defined distribution pattern of additonal amount for specific document. Entity: Gen_Document_Line_Amounts

# Aggregate Hierarchy

* [Gen_Documents](Gen_Documents.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Document_Line_Amount_Id|`Guid`|`PK`, Readonly||
|Document_Line_Id|`Guid`||The line for which the distribution pattern is specified. `Required` `Filter(multi eq)` |
|Line_Percent|`Decimal`||The percent of the additional amount which should be distributed over the current line. `Required` `Default(0)` |
