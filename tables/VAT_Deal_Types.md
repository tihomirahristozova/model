# Table VAT_Deal_Types

Contains deal types supported by the system as well as user-defined types. Entity: VAT_Deal_Types

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Deal_Type_Id|`Guid`|`PK`, Readonly||
|Entry_Type|`EntryType`|Allowed: `P`, `S`|Type of the VAT entries, which are made for this deal type. S=Sales, P=Purchases. `Required` `Filter(eq)` |
|Is_System|`Boolean`|Readonly|Is_System is True for those deal types that are managed by the system via update procedures and cannot be edited by the user. `Required` `Default(false)` `Filter(eq)` `ReadOnly` |
|Deal_Type_Name|`String`||Description of the deal type. `Required` `Filter(eq;like)` |
