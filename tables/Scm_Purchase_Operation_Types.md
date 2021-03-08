# Table Scm_Purchase_Operation_Types

User-defined categorization of the purchase operations. Used to group the purchase control data. Entity: Scm_Purchase_Operation_Types (Introduced in version 18.2)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Purchase_Operation_Type_Id|`Guid`|`PK`, Readonly||
|Code|`String`||Unique code of the purchase operation type. `Required` `Filter(multi eq;like)` |
|Name|`MultilanguageString`||Name of the purchase operation type (multilanguage). `Required` `Filter(multi eq;like)` |
|Notes|`String`||Notes for this PurchaseOperationType. `Filter(eq;like)` |
