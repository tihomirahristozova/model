# Table Cm_Company_Employees

Contains the company employee contracts. Entity: Cm_Company_Employees

# Aggregate Hierarchy

* [Cm_Persons](Cm_Persons.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Company_Employee_Id|`Guid`|`PK`, Readonly||
|Contract_Code|`String`||Contract number or code, unique within the company. One employee can have more than one contract. `Filter(eq)` |
|Contract_End_Date|`DateTime?`||End date of the employee contract, null if the contract is still valid. `Filter(ge;le)` |
|Contract_Start_Date|`DateTime?`||Start date of the employee contract. Null if it is unkown. `Filter(ge;le)` |
|Notes|`String`||Notes for this CompanyEmployee. |
