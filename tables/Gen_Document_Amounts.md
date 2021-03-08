# Table Gen_Document_Amounts

Contains a specific instance of an additional amount for a specific document. Entity: Gen_Document_Amounts

# Aggregate Hierarchy

* [Gen_Documents](Gen_Documents.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Document_Amount_Id|`Guid`|`PK`, Readonly||
|Input_Percent|`Decimal?`||When not null, specifies that the amount for this document will be calculated as percent of the base amounts (which are defined in the amount type). `Filter(ge;le)` |
|User_Can_Change_Input|`Boolean`||True if the user, entering the document is allowed to change the default input percent. `Required` `Default(true)` |
