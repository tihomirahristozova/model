# Table Gen_Currencies

List of user-defined currencies. Entity: Gen_Currencies

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Currency_Id|`Guid`|`PK`, Readonly||
|Currency_Sign|`String`||The international currency designator, as defined in ISO 4217. For example euro is represented as 'EUR'. `Required` `Filter(eq;like)` `ORD` |
|Currency_Name|`String`||The name of this Currency. `Required` `Filter(like)` |
|Show_Order|`Int32`||The order in which to show the currency in combo boxes, etc. `Required` `Default(0)` |
