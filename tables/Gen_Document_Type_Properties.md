# Table Gen_Document_Type_Properties

Default user-defined properties, which should be added to new documents. Entity: Gen_Document_Type_Properties

# Aggregate Hierarchy

* [Gen_Document_Types](Gen_Document_Types.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|User_Property_Id|`Guid`|`PK`, Readonly||
|Default_Property_Value|`String`||The default value of the property when creating new documents. |
|Default_Property_Value_Description|`MultilanguageString`||Default description value of the property when creating new documents. |
|Default_Value_Id|`Guid?`||Internal Id of the default value of the property. `Filter(multi eq)` |
|Line_No|`Int32`||Line number, unique within the document type. `Required` `Filter(ge;le)` `ORD` |
|Required|`Boolean`||True if the property is required when creating documents of this type. `Required` `Default(false)` `Filter(eq)` |
|Required_From_Date|`DateTime?`||When not null, specifies a date, after which the property becomes required for the current document type. The date is compared against the document date. `Filter(ge;le)` |
|Required_Thru_Date|`DateTime?`||When not null, specifies a date, up to which the property is required for the current document type. The date is compared against the document date. `Filter(ge;le)` |
