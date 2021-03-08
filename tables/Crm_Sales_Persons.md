# Table Crm_Sales_Persons

Sales persons (or representatives) are sellers inside the enterprise company who sell the products to customers. Entity: Crm_Sales_Persons

# Aggregate Hierarchy

* [Cm_Persons](Cm_Persons.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Sales_Person_Id|`Guid`|`PK`, Readonly||
|Commission_Percent|`Decimal?`||The percentage (0..1) of commission percent. null means that there is no commission percent. |
|Commission_Policy_Id|`Guid?`||Current commission policy for the sales person. null means there is no commission policy. `Filter(multi eq)` |
|Contract_End_Date|`DateTime?`||The ending date of the contract with the sales person. null when the sales person is still active. `Filter(ge;le)` |
|Contract_Start_Date|`DateTime?`||The starting date of the contract with the sales person. null when it is unknown. `Filter(ge;le)` |
|Is_Active|`Boolean`||Specifies whether the sales person is active and should be included in the list when choosing sales person through drop-downs, lists, etc. `Required` `Default(true)` `Filter(eq)` |
