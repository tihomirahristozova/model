# Table Scm_Suppliers

Contains supplier conditions (contracts). Entity: Scm_Suppliers

# Aggregate Hierarchy

* [Gen_Parties](Gen_Parties.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Supplier_Id|`Guid`|`PK`, Readonly||
|Creation_Time|`DateTime?`|Readonly|Date and time when the Supplier was created. `Filter(ge;le)` `ReadOnly` |
|Creation_User|`String`|Readonly|Login name of the user, who created the Supplier. `Filter(like)` `ReadOnly` |
|Default_Delivery_Term_Days|`Int32`||Default term in days for goods delivery, starting at the day of sending the purchase order. `Required` `Default(0)` |
|Default_Payment_Start_Days|`Int32`||Default number of days until the payment becomes executable. 0 means that the payment is executable at all times. `Required` `Default(0)` |
|Default_Payment_Term_Days|`Int32`||Default payment term in days, starting from the date of receiving the invoice. `Required` `Default(0)` |
|From_Date|`DateTime?`||The date on which this party became a supplier or the date, when the supplier contract was signed. `Filter(ge;le)` |
|Is_Active|`Boolean`||Indicates whether the current supplier is active. `Required` `Default(true)` `Filter(eq)` |
|Supplier_Number|`String`||The unique supplier number. `Filter(eq)` `ORD` |
|Thru_Date|`DateTime?`||The date (inclusive) on which this party ceased to be a supplier. `Filter(ge;le)` |
|Update_Time|`DateTime?`|Readonly|Date and time when the Supplier was last updated. `Filter(ge;le)` `ReadOnly` |
|Update_User|`String`|Readonly|Login name of the user, who last updated the Supplier. `Filter(like)` `ReadOnly` |
