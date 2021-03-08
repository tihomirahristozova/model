# Table Nat_BG_VAT_Declaring_Persons

National data: Contains the persons, which are authorized to issue and sign VAT declarations. Entity: Nat_BG_VAT_Declaring_Persons

# Aggregate Hierarchy

* [Gen_Enterprise_Companies](Gen_Enterprise_Companies.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Declaring_Person_Id|`Guid`|`PK`, Readonly||
|Declarer_Type|`DeclarerType`|Allowed: `A`, `R`|Type of the declaring person. A=Attorney, R=Representative. `Required` `Filter(eq)` |
|Declaring_Person_Address|`String`||Address for correspondation of the declaring person. `Required` |
|Declaring_Person_City|`String`||City from the address for correspondation of the declaring person. `Required` |
|Declaring_Person_Position|`String`||Position of the declaring person in the enterprise company. |
|Declaring_Person_Postcode|`String`||Postcode from the address for correspondation of the declaring person. `Required` |
|Is_Default|`Boolean`||True if this is the default person, which issues VAT declarations for this Enterprise Company. `Required` `Default(true)` |
