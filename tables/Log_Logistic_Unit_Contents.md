# Table Log_Logistic_Unit_Contents

Theoretical or actual content of a logistic unit. Entity: Log_Logistic_Unit_Contents (Introduced in version 21.1.0.77)

# Aggregate Hierarchy

* [Log_Logistic_Units](Log_Logistic_Units.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Logistic_Unit_Content_Id|`Guid`|`PK`, Readonly||
|Base_Quantity|`Decimal`||The quantity, expressed in the base measurement category of the product. `Required` `Filter(eq;ge;le)` |
|Expiration_Date|`DateTime?`||Expiration date of the goods. null means unknown or N/A. `Filter(multi eq;ge;le)` |
|Gross_Weight|`Decimal?`||Gross weight in kilograms (kg). null means unknown. `Filter(eq;ge;le)` |
|Line_No|`Int32`||Consecutive position within the logistic unit. `Required` `Filter(multi eq)` |
|Lot_Number|`String`||The production lot number. null means unknown. `Filter(multi eq;like)` |
|Notes|`String`||Notes for this LogisticUnitContent. |
|Quantity|`Decimal`||Quantity of the product in the logistic unit. Expressed in the specified measurement unit. `Required` `Filter(multi eq;ge;le)` |
|Standard_Quantity|`Decimal`||The quantity, expessed in the standard measurement unit of the product. `Required` `Filter(eq;ge;le)` |
