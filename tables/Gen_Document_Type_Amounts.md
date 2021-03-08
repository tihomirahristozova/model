# Table Gen_Document_Type_Amounts

Specifies amount types, that should be automatically added to documents of a given type. Entity: Gen_Document_Type_Amounts

# Aggregate Hierarchy

* [Gen_Document_Types](Gen_Document_Types.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Document_Type_Amount_Id|`Guid`|`PK`, Readonly||
|Default_Percent|`Decimal?`||Default input percent. Valid only for amount types, supporting percent and takes precedence over Default_Percent in the definition of the amount type. |
|Required_From_Date|`DateTime?`||When not null, specifies a date, after which the amount becomes required for the current document type. The date is compared against the document date. `Filter(ge;le)` |
|Required_Thru_Date|`DateTime?`||When not null, specifies a date, up to which the amount is required for the current document type. The date is compared against the document date. `Filter(ge;le)` |
|User_Can_Change_Input|`Boolean`||True if the user, entering the document is allowed to change the default input percent. `Required` `Default(true)` |
